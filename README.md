# 🚀 Content Multiplier

**Turn 1 Video Into 50+ Pieces of Content Automatically**

Automated content repurposing pipeline built for content creators. Upload one long-form video, get back clips, frames, GIFs, blog posts, social media hooks, and more - all automatically generated and optimized for each platform.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.11+](https://img.shields.io/badge/python-3.11+-blue.svg)](https://www.python.org/downloads/)

---

## ✨ What It Does

**Input:** 1 long-form video (10-30 minutes)

**Automated Output:**
- 📹 **5 short clips** for Twitter/X (vertical format, different timestamps)
- - 📸 **10 still frames** for photo posts
  - - 🎞️ **3 teaser GIFs** (looping animations)
    - - ✍️ **25 social media hooks** (5 variations per clip)
      - - 📝 **SEO blog post** with embedded content
        - - 📧 **Email template** for subscribers
          - - 📄 **Video transcript** for SEO
           
            - **Total:** 50+ pieces of content from 1 source video!
           
            - ---

            ## 🎯 Perfect For

            - 🎥 Content creators (YouTube, OnlyFans, JustForFans)
            - - 📱 Social media managers
              - - 🎬 Video producers
                - - 💼 Personal brands
                  - - 🚀 Anyone creating long-form video content
                   
                    - ---

                    ## 🛠️ Tech Stack

                    - **FFmpeg** - Video processing & splitting
                    - - **Claude AI API** - Content generation & hooks
                      - - **Cloudflare Stream** - Video hosting (optional)
                        - - **Make.com/Zapier** - Automation orchestration
                          - - **Python 3.11+** - Core processing
                            - - **Node.js** - API server
                             
                              - ---

                              ## ⚡ Quick Start

                              ### 1. Clone Repository

                              ```bash
                              git clone https://github.com/aabiro/content-multiplier.git
                              cd content-multiplier
                              chmod +x scripts/*.sh
                              ```

                              ### 2. Run Installation

                              ```bash
                              ./scripts/install.sh
                              ```

                              This will:
                              - ✅ Check dependencies (FFmpeg, Python, Node.js)
                              - - ✅ Install Python packages
                                - - ✅ Install Node modules
                                  - - ✅ Create directory structure
                                    - - ✅ Generate `.env` template
                                     
                                      - ### 3. Configure API Keys
                                     
                                      - ```bash
                                        cp .env.example .env
                                        nano .env  # Add your API keys
                                        ```

                                        Required keys:
                                        - `ANTHROPIC_API_KEY` - Get from https://console.anthropic.com
                                        - - `CF_ACCOUNT_ID` & `CF_API_TOKEN` - Get from Cloudflare (optional)
                                         
                                          - ### 4. Process Your First Video
                                         
                                          - ```bash
                                            ./scripts/master_repurpose.sh "your-video.mp4" "Video Title" "Description"
                                            ```

                                            That's it! Check the `output_*/` folder for all generated content.

                                            ---

                                            ## 📂 What You Get

                                            ```
                                            output_20250930_120000/
                                            ├── clips/
                                            │   ├── clip_1_twitter.mp4  (30-60s vertical clips)
                                            │   ├── clip_2_twitter.mp4
                                            │   ├── clip_3_twitter.mp4
                                            │   ├── clip_4_twitter.mp4
                                            │   └── clip_5_twitter.mp4
                                            ├── frames/
                                            │   ├── frame_1.jpg  (1920x1080 high-quality stills)
                                            │   ├── frame_2.jpg
                                            │   └── ... (10 total)
                                            ├── gifs/
                                            │   ├── teaser_1.gif  (3-4 second loops)
                                            │   ├── teaser_2.gif
                                            │   └── teaser_3.gif
                                            ├── copy/
                                            │   ├── clip_1_hooks.json  (5 hook variations)
                                            │   ├── clip_2_hooks.json
                                            │   ├── clip_3_hooks.json
                                            │   ├── clip_4_hooks.json
                                            │   ├── clip_5_hooks.json
                                            │   ├── blog_post.md
                                            │   └── email_template.html
                                            ├── cloudflare_links.json  (hosted video URLs)
                                            ├── transcript.txt  (full video transcript)
                                            └── manifest.json  (metadata)
                                            ```

                                            ---

                                            ## 🎨 Example Hooks Generated

                                            For a garage scene video, Claude AI generates variations like:

                                            **Teasing:**
                                            > "What happens when the garage door closes? 🔧 New footage just dropped..."
                                            >
                                            > **Direct:**
                                            > > "Raw. Unfiltered. 20 minutes of exactly what you've been asking for 👀"
                                            > >
                                            > > **Playful:**
                                            > > > "POV: You're helping me 'organize' the garage 😏 Full vid on OF"
                                            > > >
                                            > > > **Exclusive:**
                                            > > > > "Subscribers saw this first. Now it's your turn... [Preview]"
                                            > > > >
                                            > > > > **BTS:**
                                            > > > > > "Behind the scenes of my most requested location 🏠"
                                            > > > > >
                                            > > > > > All hooks are under 280 characters, platform-optimized, and ready to post!
                                            > > > > >
                                            > > > > > ---
                                            > > > > >
                                            > > > > > ## 🔧 Advanced Configuration
                                            > > > > >
                                            > > > > > ### Custom Timestamps
                                            > > > > >
                                            > > > > > Edit `config/timestamp_markers.json`:
                                            > > > > >
                                            > > > > > ```json
                                            > > > > > {
                                            > > > > >   "clips": [
                                            > > > > >     {"start": "00:02:15", "duration": 45},
                                            > > > > >     {"start": "00:05:30", "duration": 50},
                                            > > > > >     {"start": "00:10:45", "duration": 60}
                                            > > > > >   ],
                                            > > > > >   "frames": ["00:01:30", "00:03:45", "00:06:20"],
                                            > > > > >   "gifs": [
                                            > > > > >     {"start": "00:03:00", "duration": 3, "fps": 15}
                                            > > > > >   ]
                                            > > > > > }
                                            > > > > > ```
                                            > > > > >
                                            > > > > > ### Platform Specs
                                            > > > > >
                                            > > > > > Modify `config/platform_specs.json` for different platforms:
                                            > > > > >
                                            > > > > > ```json
                                            > > > > > {
                                            > > > > >   "twitter": {
                                            > > > > >     "video": {"width": 720, "height": 1280, "max_size_mb": 512},
                                            > > > > >     "image": {"width": 1200, "height": 675}
                                            > > > > >   },
                                            > > > > >   "instagram": {
                                            > > > > >     "reel": {"width": 1080, "height": 1920},
                                            > > > > >     "post": {"width": 1080, "height": 1080}
                                            > > > > >   }
                                            > > > > > }
                                            > > > > > ```
                                            > > > > >
                                            > > > > > ---
                                            > > > > >
                                            > > > > > ## 🤖 Automation with Make.com
                                            > > > > >
                                            > > > > > 1. Import `make-scenario.json` to your Make.com account
                                            > > > > > 2. 2. Connect your Dropbox, Twitter, email services
                                            > > > > >    3. 3. Upload videos to `/Content/Raw/` folder
                                            > > > > >       4. 4. Everything processes automatically!
                                            > > > > >         
                                            > > > > >          5. **Workflow:**
                                            > > > > >          6. ```
                                            > > > > >             Dropbox Upload → Process Video → Upload to Cloudflare
                                            > > > > >             → Generate AI Copy → Post to Twitter → Send Email
                                            > > > > >             → Publish Blog → Notification
                                            > > > > >             ```
                                            > > > > >
                                            > > > > > ---
                                            > > > > >
                                            > > > > > ## 💰 Cost Breakdown
                                            > > > > >
                                            > > > > > | Service | Monthly Cost |
                                            > > > > > |---------|-------------|
                                            > > > > > | Claude API (500k tokens) | $7-15 |
                                            > > > > > | Cloudflare Stream (1000 min) | $1-5 |
                                            > > > > > | Make.com (10k operations) | $9-29 |
                                            > > > > > | FFmpeg (self-hosted) | Free |
                                            > > > > > | **Total** | **$17-49/month** |
                                            > > > > >
                                            > > > > > ---
                                            > > > > >
                                            > > > > > ## 📖 Documentation
                                            > > > > >
                                            > > > > > - [Complete Setup Guide](docs/SETUP_GUIDE.md)
                                            > > > > > - - [API Reference](docs/API_REFERENCE.md)
                                            > > > > >   - - [Customization Guide](docs/CUSTOMIZATION.md)
                                            > > > > >     - - [Troubleshooting](docs/TROUBLESHOOTING.md)
                                            > > > > >      
                                            > > > > >       - ---
                                            > > > > >
                                            > > > > > ## 🎯 Use Cases
                                            > > > > >
                                            > > > > > ### For Adult Content Creators
                                            > > > > > - Repurpose OnlyFans/JustForFans content across Twitter/X
                                            > > > > > - - Generate teaser clips with various hooks
                                            > > > > >   - - Maintain consistent posting schedule
                                            > > > > >     - - SEO-optimized blog posts for discoverability
                                            > > > > >      
                                            > > > > >       - ### For YouTubers
                                            > > > > >       - - Create shorts from long-form content
                                            > > > > >         - - Generate thumbnails automatically
                                            > > > > >           - - Multi-platform distribution
                                            > > > > >             - - Email list engagement
                                            > > > > >              
                                            > > > > >               - ### For Educators
                                            > > > > >               - - Break lectures into topic-specific clips
                                            > > > > >                 - - Create study materials (frames + transcripts)
                                            > > > > >                   - - Social media promotion
                                            > > > > >                     - - Student email updates
                                            > > > > >                      
                                            > > > > >                       - ---
                                            > > > > >
                                            > > > > > ## 🤝 Contributing
                                            > > > > >
                                            > > > > > Contributions welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) first.
                                            > > > > >
                                            > > > > > 1. Fork the repository
                                            > > > > > 2. 2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
                                            > > > > >    3. 3. Commit changes (`git commit -m 'Add AmazingFeature'`)
                                            > > > > >       4. 4. Push to branch (`git push origin feature/AmazingFeature`)
                                            > > > > >          5. 5. Open a Pull Request
                                            > > > > >            
                                            > > > > >             6. ---
                                            > > > > >            
                                            > > > > >             7. ## 📄 License
                                            > > > > >            
                                            > > > > >             8. MIT License - see [LICENSE](LICENSE) file for details.
                                            > > > > > 
                                            ---

                                            ## 🙏 Acknowledgments

                                            - Built with [Claude AI](https://anthropic.com) for content generation
                                            - - [FFmpeg](https://ffmpeg.org) for video processing
                                              - - [Cloudflare Stream](https://cloudflare.com/products/cloudflare-stream/) for video hosting
                                               
                                                - ---

                                                ## 📞 Support

                                                - 🐛 **Issues:** [GitHub Issues](https://github.com/aabiro/content-multiplier/issues)
                                                - - 💬 **Discussions:** [GitHub Discussions](https://github.com/aabiro/content-multiplier/discussions)
                                                  - - 📧 **Email:** [Create an issue](https://github.com/aabiro/content-multiplier/issues/new)
                                                   
                                                    - ---

                                                    ## ⭐ Star History

                                                    If this project helps you, please star it! ⭐

                                                    ---

                                                    **Made with** ❤️ **by content creators, for content creators**
