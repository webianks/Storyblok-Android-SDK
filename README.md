# Storyblok-Android-SDK

This is the Storyblok Android client for easy access of the publishing api.

# More about Storyblok
- **WEBSITE** https://www.storyblok.com/
- **API DOC** https://www.storyblok.com/docs/Delivery-Api/introduction

# Include in your project
## Using Maven

```gradle
compile "com.mikepenz:storyblok-android-sdk:0.2.0@aar"
```

## How to use
### Init client

```java
Storyblok client = Storyblok.init("your-storyblok-token");
```

### Load a story
```java
client.getStory("fullSlug", new Storyblok.StoryblokCallback<Story>() {
    @Override
    public void onFailure(IOException exception, String response) {
        //on error
    }

    @Override
    public void onResponse(final Result<Story> result) {
        //on success
    }
});
```

### Load a list of stories
```java
client.getStories(startsWith, withTag, sortBy, perPage, page, new Storyblok.StoryblokCallback<List<Story>>() {
    @Override
    public void onFailure(IOException exception, String response) {
        //on error
    }

    @Override
    public void onResponse(final Result<List<Story>> result) {
        //on success
    }
});
```

### Load a list of tags
```java
client.getTags(startsWith, new Storyblok.StoryblokCallback<List<Tag>>() {
    @Override
    public void onFailure(IOException exception, String response) {
        //on error
    }

    @Override
    public void onResponse(final Result<List<Tag>> result) {
        //on success
    }
});
```

### Load a map of links
```java
client.getLinks(new Storyblok.StoryblokCallback<Map<String, Link>>() {
    @Override
    public void onFailure(IOException exception, String response) {
        //on error
    }

    @Override
    public void onResponse(final Result<Map<String, Link>> result) {
        //on success
    }
});
```

### Load a list of datasources
```java
client.getDatasource(datasource, new Storyblok.StoryblokCallback<List<Datasource>>() {
    @Override
    public void onFailure(IOException exception, String response) {
        //on error
    }

    @Override
    public void onResponse(final Result<List<Datasource>> result) {
        //on success
    }
});
```


## Libs used in sample app:
Mike Penz:
- FastAdapter https://github.com/mikepenz/FastAdapter
- AboutLibraries https://github.com/mikepenz/AboutLibraries
- Android-Iconics https://github.com/mikepenz/Android-Iconics
- MaterialDrawer https://github.com/mikepenz/MaterialDrawer

# Developed By

* Mike Penz 
  * [mikepenz.com](http://mikepenz.com) - <mikepenz@gmail.com>
  * [paypal.me/mikepenz](http://paypal.me/mikepenz)

# Contributors

This free, open source software was also made possible by a group of volunteers that put many hours of hard work into it. See the [CONTRIBUTORS.md](CONTRIBUTORS.md) file for details.

# License

    Copyright 2017 Mike Penz

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
