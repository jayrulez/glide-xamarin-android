Glide
=====


Glide is a fast and efficient open source media management and image loading framework for Android that wraps media
decoding, memory and disk caching, and resource pooling into a simple and easy to use interface.

Android resource: https://github.com/bumptech/glide

Version : 3.7.0

Download : Available on Nuget Gallery ( https://www.nuget.org/packages/Glide.Xamarin/ )

How do I use Glide?
-------------------

Simple use cases :

```cs
// Default :
Glide.With(this).Load("Url").Into(propertyPrimaryImageView);

// Placeholder :
Glide.With(this).Load("Url")
			     .Placeholder(Resource.Drawable.placeholder)
			     .Into(propertyPrimaryImageView);

// Thumbnail & DontAnimate			     
Glide.With(this).Load("Url")
			     .Placeholder(Resource.Drawable.placeholder)
			     .Thumbnail(0.1f)
			     .DontAnimate()
			     .Into(propertyPrimaryImageView);			     

// SkipMemoryCache & DiskCacheStrategy
Glide.With(this).Load("Url")
				 .Placeholder(Resource.Drawable.placeholder)
				 .SkipMemoryCache(true)
				 .DiskCacheStrategy(DiskCacheStrategy.All)
			     .Into(propertyPrimaryImageView);
```

Using in RecyclerView | ListView Adapter :
```cs

// Placeholder : 
Glide.With(context).Load("Url")
				 .Placeholder(Resource.Drawable.placeholder)
				 .Into(viewHolder.propertyImageView);
```

Gif support : 
```cs
Glide.With(context).Load("GifUrl")
					 .Placeholder(Resource.Drawable.placeholder)
				     .DiskCacheStrategy(DiskCacheStrategy.Source)
					 .Into(viewHolder.propertyImageView);
```

Fast Loading from Cache :

![alt tag](http://g.recordit.co/JShY8Oe64y.gif)

Combine Gif with Image

![alt tag](http://g.recordit.co/p2oEN2bLIn.gif)

Author
------
Beray Bentesen -  @BerayBentesen on Twitter




