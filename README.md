# Bolkar-Internship
My First Repository on Github


import android.app.Activity

class MyActivity : Activity()
{
    private lateinit var recyclerView: RecyclerView

    class RecyclerView {
        class Adapter<T> {

        }

        class LayoutManager {

        }

    }

    private lateinit var viewAdapter: RecyclerView.Adapter<*>
    private lateinit var viewManager: RecyclerView.LayoutManager

    override fun onCreate(savedInstanceState: Bundle?)
    {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.my_activity)

        viewManager = LinearLayoutManager(this)
        viewAdapter = MyAdapter(myDataset)

        recyclerView = findViewById<RecyclerView>(R.id.my_recycler_view).apply {
            // use this setting to improve performance if you know that changes
            // in content do not change the layout size of the RecyclerView
            setHasFixedSize(true)

            // use a linear layout manager
            var layoutManager = viewManager

            // specify an viewAdapter (see also next example)
            var adapter = viewAdapter

        }
    }

    private fun setHasFixedSize(b: Boolean) {

    }
    // ...
}
class MyAdapter(private val myDataset: Array<String>) :
        MyActivity.RecyclerView.Adapter<MyAdapter.MyViewHolder>() {

    // Provide a reference to the views for each data item
    // Complex data items may need more than one view per item, and
    // you provide access to all the views for a data item in a view holder.
    // Each data item is just a string in this case that is shown in a TextView.
    class MyViewHolder(val textView: TextView) : RecyclerView.ViewHolder(textView)


    // Create new views (invoked by the layout manager)
    override fun onCreateViewHolder(parent: ViewGroup,
                                    viewType: Int): MyAdapter.MyViewHolder {
        // create a new view
        val textView = LayoutInflater.from(parent.context)
                .inflate(R.layout.my_text_view, parent, false) as TextView
        // set the view's size, margins, paddings and layout parameters
        ...
        return MyViewHolder(textView)
    }

    // Replace the contents of a view (invoked by the layout manager)
    override fun onBindViewHolder(holder: MyViewHolder, position: Int) {
        // - get element from your dataset at this position
        // - replace the contents of the view with that element
        holder.textView.text = myDataset[position]
    }

    // Return the size of your dataset (invoked by the layout manager)
    override fun getItemCount() = myDataset.size
}
var tracker = SelectionTracker.Builder(
        "my-selection-id",
        recyclerView,
        StableIdKeyProvider(recyclerView),
        MyDetailsLookup(recyclerView),
        StorageStrategy.createLongStorage())
        .withOnItemActivatedListener(myItemActivatedListener)
        .build()

object myItemActivatedListener {

}
[
    {
        "title": "",
        "data": [
            {
                "t": "Sandeep Ma..",
                "c": "#4F1225",
                "cat": "à¤•à¤¹à¤¾à¤¨à¤¿à¤¯à¤¾à¤‚",
                "d": "à¤ªà¥ à¤°à¤¸à¤¿à¤¦à¥ à¤§ à¤®à¥‹à¤Ÿà¤¿à¤µà¥‡à¤¶à¤¨à¤² à¤¸à¥ à¤ªà¥€à¤•à¤° à¤¸à¤‚à¤¦à¥€à¤ª à¤®à¤¾à¤¹à¥‡à¤¶à¥ à¤µà¤°à¥€ à¤•à¥‹ à¤¸à¥ à¤¨à¥‡à¤‚ à¤¸à¤•à¤¾à¤°à¤¾à¤¤à¥ à¤®à¤•à¤¤à¤¾ à¤¬à¥ à¤¾à¤ à¤‚!",
                "p": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/sandeep+banner.png",
                "pF": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/sandeep_feed.png",
                "pFBig": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/sandeep+player.png",
                "id": "sandeep-maheshwari"
            },
            {
                "t": "Darr",
                "cat": "à¤•à¤¹à¤¾à¤¨à¤¿à¤¯à¤¾à¤‚",
                "d": "à¤…à¤²à¥Œà¤•à¤¿à¤• à¤˜à¤Ÿà¤¨à¤¾à¤“à¤‚ à¤•à¥‡ à¤†à¤¸ à¤ªà¤¾à¤¸ à¤•à¥‡à¤‚à¤¦à¥ à¤°à¤¿à¤¤ à¤•à¤¹à¤¾à¤¨à¤¿à¤¯à¤¾à¤‚ || Stories centred around the supernatural phenomenon",
                "p": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/Darr+Banner.png",
                "pF": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/ho-0.png",
                "pFBig": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/Dar+Player.png",
                "id": "horror"
            },
            {
                "t": "Kya woh sach..",
                "cat": "à¤•à¤¹à¤¾à¤¨à¤¿à¤¯à¤¾à¤‚",
                "d": "à¤¯à¤¹ à¤µà¤¾à¤¸à¥ à¤¤à¤µà¤¿à¤• à¤œà¥€à¤µà¤¨ à¤•à¥€ à¤˜à¤Ÿà¤¨à¤¾à¤“à¤‚ à¤¸à¥‡ à¤ªà¥ à¤°à¥‡à¤°à¤¿à¤¤ à¤•à¤¹à¤¾à¤¨à¤¿à¤¯à¤¾à¤  à¤”à¤° à¤¸à¤‚à¤­à¤µà¤¤à¤ƒ à¤…à¤¨à¤¦à¥‡à¤–à¥€ à¤”à¤° à¤¸à¤¬à¤¸à¥‡ à¤…à¤¸à¤¾à¤§à¤¾à¤°à¤£ à¤…à¤²à¥Œà¤•à¤¿à¤• à¤•à¤¹à¤¾à¤¨à¤¿à¤¯à¥‹à¤‚ à¤•à¤¾ à¤¸à¤‚à¤—à¥ à¤°à¤¹ à¤¹à¥ˆà¥¤ || Stories inspired by real life events and is a collection of possibly the most extraordinary supernatural stories of the unseen.",
                "p": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/kya+wo+sach+tha+banner.png",
                "pF": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/ho-2.png",
                "pFBig": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/kya+wo+sach+tha+player.png",
                "id": "real-horror-stories"
            },
            {
                "t": "Ishq Wala Love",
                "cat": "à¤•à¤¹à¤¾à¤¨à¤¿à¤¯à¤¾à¤‚",
                "d": "à¤ªà¥ à¤°à¥‡à¤® à¤•à¤¥à¤¾à¤ à¤  || Love Stories",
                "p": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/ishq+wala+love+banner.png",
                "pF": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/ho-11.png",
                "pFBig": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/ishq+wala+love+banner+player.png",
                "id": "ishq-wala-love"
            },
            {
                "t": "Ek Purani Kahani",
                "cat": "à¤•à¤¹à¤¾à¤¨à¤¿à¤¯à¤¾à¤‚",
                "d": "à¤¸à¥ à¤¨à¤¿à¤  à¤¹à¤¿à¤‚à¤¦à¥€ à¤”à¤° à¤‰à¤°à¥ à¤¦à¥‚ à¤®à¥‡à¤‚ RJ à¤¸à¤¾à¤‡à¤®à¤¾ à¤•à¥‡ à¤¦à¥ à¤µà¤¾à¤°à¤¾ à¤¸à¤¾à¤¦à¤¤ à¤¹à¤¸à¤¨ à¤®à¤‚à¤Ÿà¥‹ à¤•à¥‡ à¤›à¥‹à¤Ÿà¥€ à¤•à¤¹à¤¾à¤¨à¤¿à¤¯à¤¾à¤‚ à¤”à¤° à¤…à¥žà¤¸à¤¾à¤¨à¥‡ || Listen short stories and afsanay of Saadat Hasan Manto in Hindi and Urdu by RJ Sayema. Also visit www.radiomirchi.com",
                "p": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/ek+purani+kahani+banner.png",
                "pF": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/ho-9.png",
                "pFBig": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/ek+purani+kahani+player.png",
                "id": "ek_purani_kahani"
            }
        ]
    },
    {
        "title": "à¤¨à¥ à¤¯à¥‚à¥› à¤ à¤‚à¤¡ à¤ªà¥‰à¤²à¤¿à¤Ÿà¤¿à¤•à¥ à¤¸",
        "data": [
            {
                "t": "Jansatta Podcast",
                "cat": "à¤¸à¤®à¤¾à¤šà¤¾à¤° à¤”à¤° à¤°à¤¾à¤œà¤¨à¥€à¤¤à¤¿",
                "d": "Jansatta Podcast à¤®à¥‡à¤‚ à¤†à¤ªà¤•à¥‹ à¤®à¤¿à¤²à¥‡à¤—à¥€ à¤¸à¤Ÿà¥€à¤• à¤”à¤° à¤¸à¤¹à¥€ à¤œà¤¾à¤¨à¤•à¤¾à¤°à¥€à¥¤ à¤†à¤ªà¤¸à¥‡ à¤œà¥ à¤¡à¤¼à¥‡ à¤®à¥ à¤¦à¥ à¤¦à¥‹à¤‚ à¤ªà¤° à¤¬à¤¾à¤¤ à¤•à¤°à¥‡à¤‚à¤—à¥‡, à¤†à¤ªà¤•à¥‡ à¤¹à¤¿à¤¤ à¤•à¥€ à¤¬à¤¾à¤¤ à¤•à¤°à¥‡à¤‚à¤—à¥‡à¥¤ à¤¦à¥‡à¤¶, à¤µà¤¿à¤¦à¥‡à¤¶, à¤–à¥‡à¤², à¤¸à¤¿à¤¯à¤¾à¤¸à¤¤ à¤•à¥€ à¤¹à¤²à¤šà¤² à¤ªà¤° à¤°à¤¹à¥‡à¤—à¥€ à¤¨à¤œà¤°à¥¤",
                "p": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/Jansatta+banner.png",
                "pF": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/ho-13.png",
                "pFBig": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/jansatta+player.png",
                "id": "jansatta-podcast"
            },
            {
                "t": "Puliyabaazi",
                "d": "à¤¯à¤¹ à¤¹à¤¿à¤‚à¤¦à¥€ à¤ªà¥‰à¤¡à¤•à¤¾à¤¸à¥ à¤Ÿ à¤†à¤ªà¤•à¥‹ à¤°à¤¾à¤œà¤¨à¥€à¤¤à¤¿, à¤¸à¤¾à¤°à¥ à¤µà¤œà¤¨à¤¿à¤• à¤¨à¥€à¤¤à¤¿, à¤ªà¥ à¤°à¥Œà¤¦à¥ à¤¯à¥‹à¤—à¤¿à¤•à¥€, à¤¦à¤°à¥ à¤¶à¤¨ à¤”à¤° à¤¬à¤¹à¥ à¤¤ à¤•à¥ à¤› à¤ªà¤° à¤—à¤¹à¤¨ à¤µà¤¾à¤°à¥ à¤¤à¤¾à¤²à¤¾à¤ª à¤®à¥‡à¤‚ à¤²à¤¾à¤¤à¤¾ à¤¹à¥ˆ || This Hindi Podcast brings to you in-depth conversations on politics, public policy, technology, philosophy and pretty much",
                "cat": "à¤¸à¤®à¤¾à¤šà¤¾à¤° à¤”à¤° à¤°à¤¾à¤œà¤¨à¥€à¤¤à¤¿",
                "p": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/puliya+banner.png",
                "pF": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/ho-1.png",
                "pFBig": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/puliya+player.png",
                "id": "Puliyabaazi"
            },
            {
                "t": "Mann Ki Baat",
                "cat": "à¤•à¤¹à¤¾à¤¨à¤¿à¤¯à¤¾à¤‚",
                "d": "à¤ªà¥ à¤°à¤§à¤¾à¤¨à¤®à¤‚à¤¤à¥ à¤°à¥€ à¤®à¥‹à¤¦à¥€ à¤•à¤¾ à¤¦à¥‡à¤¶ à¤•à¥‡ à¤¨à¤¾à¤® à¤¸à¤‚à¤¬à¥‹à¤§à¤¨",
                "p": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/Mankibaat+banner.png",
                "pF": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/ho-14.png",
                "pFBig": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/Mankibaat+Player.png",
                "id": "mann-ki-baat"
            },
            {
                "t": "The Big Story",
                "cat": "à¤¸à¤®à¤¾à¤šà¤¾à¤° à¤”à¤° à¤°à¤¾à¤œà¤¨à¥€à¤¤à¤¿",
                "d": "à¤¸à¥ à¤¨à¤¿à¤  à¤¦à¤¿à¤¨ à¤•à¥€ à¤¬à¥œà¥€ à¤–à¤¬à¤° à¤•à¥ à¤µà¤¿à¤‚à¤Ÿ à¤¹à¤¿à¤‚à¤¦à¥€ à¤•à¥‡ Big Story à¤ªà¥‰à¤¡à¤•à¤¾à¤¸à¥ à¤Ÿ à¤®à¥‡à¤‚",
                "p": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/thebigstory+banner.png",
                "pF": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/ho-5.png",
                "pFBig": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/the+bis+story+player.png",
                "id": "the-big-story"
            }
        ]
    },
    {
        "title": "à¤¶à¤¿à¤•à¥ à¤·à¤¾ à¤”à¤° à¤œà¥ à¤žà¤¾à¤¨",
        "data": [
            {
                "t": "GK NOTES",
                "cat": "à¤¶à¤¿à¤•à¥ à¤·à¤¾ à¤”à¤° à¤œà¥ à¤žà¤¾à¤¨",
                "d": "GK NOTES (à¤¸à¤¾à¤®à¤¾à¤¨à¥ à¤¯ à¤œà¥ à¤žà¤¾à¤¨) à¤¬à¥‹à¤²à¤•à¤° à¤ªà¤° à¤ à¤• à¤¶à¥ˆà¤•à¥ à¤·à¤¿à¤• à¤®à¤‚à¤š à¤œà¥‹ à¤¸à¤¾à¤®à¤¾à¤¨à¥ à¤¯ à¤œà¥ à¤žà¤¾à¤¨ à¤”à¤° à¤…à¤§à¥ à¤¯à¤¯à¤¨ à¤¸à¥‡ à¤¸à¤‚à¤¬à¤‚à¤§à¤¿à¤¤ à¤¹à¥ˆà¥¤ ðŸ¤”Target : UPSC, RRB, STATE PSC, IBPS, SBI, RBI, Others.",
                "p": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/samanya+path+banner.png",
                "pF": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/ho-12.png",
                "pFBig": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/samanya+path+player.png",
                "id": "gk-notes"
            },
            {
                "t": "Jobs Jankari",
                "cat": "à¤¶à¤¿à¤•à¥ à¤·à¤¾ à¤”à¤° à¤œà¥ à¤žà¤¾à¤¨",
                "d": "à¤œà¥‰à¤¬à¥ à¤¸, à¤ à¤—à¥ à¤œà¤¾à¤® à¤”à¤° à¤°à¤¿à¤œà¤²à¥ à¤Ÿ à¤¸à¥‡ à¤œà¥ à¤¡à¤¼à¥€ à¤¤à¤¾à¤œà¤¾ à¤–à¤¬à¤°à¥‡à¤‚, à¤‰à¤šà¥ à¤š à¤¶à¤¿à¤•à¥ à¤·à¤¾ à¤”à¤° à¤¨à¥Œà¤•à¤°à¥€ à¤¤à¤²à¤¾à¤¶ à¤°à¤¹à¥‡ à¤¯à¥ à¤µà¤¾à¤“à¤‚ à¤•à¥‡ à¤²à¤¿à¤  à¤•à¤°à¤¿à¤¯à¤° à¤®à¥‡à¤‚ à¤…à¤šà¥ à¤›à¤¾ à¤•à¤°à¤¨à¥‡ à¤•à¥‡ à¤Ÿà¤¿à¤ªà¥ à¤¸ à¤¬à¤¤à¤¾à¤ à¤ à¤—à¥‡ à¤²à¤¾à¤‡à¤µ à¤¹à¤¿à¤‚à¤¦à¥ à¤¸à¥ à¤¤à¤¾à¤¨ à¤•à¥‡ à¤šà¥€à¥ž à¤•à¤‚à¤Ÿà¥‡à¤‚à¤Ÿ à¤•à¥ à¤°à¤¿à¤ à¤Ÿà¤°, à¤ªà¤‚à¤•à¤œ à¤µà¤¿à¤œà¤¯à¥¤à¤†à¤ª à¤¸à¥ à¤¨ à¤°à¤¹à¥‡ à¤¹à¥ˆà¤‚ à¤ à¤š à¤Ÿà¥€ à¤¸à¥ à¤®à¤¾à¤°à¥ à¤Ÿà¤•à¤¾à¤¸à¥ à¤Ÿ à¤”à¤° à¤¯à¥‡ à¤¹à¥ˆ à¤²à¤¾à¤‡à¤µ à¤¹à¤¿à¤‚à¤¦à¥ à¤¸à¥ à¤¤à¤¾à¤¨ à¤ªà¥ à¤°à¥‹à¤¡à¤•à¥ à¤¶à¤¨ |",
                "p": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/jabs+jankaari+banner.png",
                "pF": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/ho-7.png",
                "pFBig": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/jobs+jankaari+player.png",
                "id": "jobs-jankari"
            }
        ]
    },
    {
        "title": "à¤§à¤°à¥ à¤® à¤”à¤° à¤…à¤§à¥ à¤¯à¤¾à¤¤à¥ à¤®",
        "data": [
            {
                "t": "Ramayan",
                "cat": "à¤§à¤°à¥ à¤® à¤”à¤° à¤…à¤§à¥ à¤¯à¤¾à¤¤à¥ à¤®",
                "d": "à¤°à¤¾à¤®à¤¾à¤¯à¤£ à¤¹à¤° à¤¸à¤®à¤¯ à¤•à¤¾ à¤­à¤µà¥ à¤¯ à¤®à¤¹à¤¾à¤•à¤¾à¤µà¥ à¤¯, à¤¦à¤¿à¤—à¥ à¤—à¤œ à¤•à¤²à¤¾à¤•à¤¾à¤°à¥‹à¤‚ à¤œà¥ˆà¤¸à¥‡ à¤¨à¤¸à¥€à¤°à¥ à¤¦à¥ à¤¦à¥€à¤¨ à¤¶à¤¾à¤¹ (à¤°à¤¾à¤µà¤£), à¤…à¤¨à¥ à¤ªà¤® à¤–à¥‡à¤° (à¤¦à¤¶à¤°à¤¥), à¤“à¤® à¤ªà¥‚à¤°à¥€ (à¤•à¤¾à¤²), à¤°à¤¤à¥ à¤¨à¤¾ à¤ªà¤¾à¤ à¤• à¤¶à¤¾à¤¹ (à¤®à¤‚à¤¥à¤°à¤¾) à¤”à¤° à¤œà¤¯à¤¤à¤¿ à¤­à¤¾à¤Ÿà¤¿à¤¯à¤¾ (à¤•à¥ˆà¤•à¥‡à¤¯à¥€) à¤¸à¥‡ à¤¸à¤œà¤¾ à¤¹à¥ˆà¥¤ à¤¯à¤¹ à¤¸à¤‚à¤ªà¥‚à¤°à¥ à¤£ à¤ªà¤¹à¤² à¤°à¥‡à¤¡à¤¿à¤¯à¥‹ à¤¶à¥ à¤°à¥‹à¤¤à¤¾à¤“à¤‚ à¤•à¥‡ à¤®à¤¨ à¤•à¥‹ à¤›à¥‚à¤¨à¥‡ à¤•à¥‡ à¤²à¤¿à¤  à¤¤à¥ˆà¤¯à¤¾à¤° à¤¹à¥ˆà¥¤",
                "p": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/ramayan+banner.png",
                "pF": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/ho-3.png",
                "pFBig": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/ramayan+player.png",
                "id": "ramayan"
            },
            {
                "t": "Mahabharat",
                "c": "#F9A900",
                "cat": "à¤•à¤¹à¤¾à¤¨à¤¿à¤¯à¤¾à¤‚",
                "d": "à¤¹à¤® à¤¸à¤­à¥€ à¤²à¥‹à¤— à¤¬à¤šà¤ªà¤¨ à¤¸à¥‡ à¤®à¤¹à¤¾à¤­à¤¾à¤°à¤¤ à¤¦à¥‡à¤– à¤•à¤° à¤¬à¥œà¥‡ à¤¹à¥ à¤  à¤¹à¥ˆà¤‚à¥¤ HT SmartCast à¤ à¤• à¤…à¤²à¤— à¤¨à¤œà¤°à¤¿à¤¯à¤¾ à¤²à¤¾à¤¯à¤¾ à¤œà¥‹ à¤†à¤ªà¤•à¥‡ à¤®à¤¹à¤¾à¤­à¤¾à¤°à¤¤ à¤•à¥‡ à¤¯à¤¾à¤¦à¥‹à¤‚ à¤•à¥‹ à¤¤à¤¾à¥›à¤¾ à¤•à¤° à¤¦à¥‡à¤—à¤¾à¥¤ à¤†à¤‡à¤¯à¥‡ à¤®à¤¹à¤¾à¤­à¤¾à¤°à¤¤ à¤•à¥‡ à¤¹à¤° à¤ªà¤¾à¤¤à¥ à¤° à¤•à¥‹ à¤ à¤• à¤¬à¤¾à¤° à¤«à¤¿à¤° à¤¸à¥‡ à¤œà¥€à¤¤à¥‡ à¤¹à¥ˆà¤‚ à¤”à¤° à¤…à¤ªà¤¨à¥€ à¤¸à¤‚à¤¸à¥ à¤•à¥ƒà¤¤à¤¿ à¤•à¥‹ à¤†à¤—à¥‡ à¤¬à¥ à¤¾à¤¤à¥‡ à¤¹à¥ˆà¤‚à¥¤ à¤¯à¤¹ FEVER FM à¤ªà¥ à¤°à¥‹à¤¡à¤•à¥ à¤¶à¤¨ à¤¦à¥ à¤µà¤¾à¤°à¤¾ à¤¬à¤¨à¤¾à¤¯à¤¾ à¤—à¤¯à¤¾ à¤¹à¥ˆ à¤”à¤° à¤¬à¥‹à¤²à¤•à¤° à¤ à¤ª à¤†à¤ªà¤•à¥‡ à¤¸à¤®à¤¸à¥ à¤¤ à¤ªà¥ à¤°à¤¸à¥ à¤¤à¥ à¤¤ à¤•à¤° à¤°à¤¹à¤¾ à¤¹à¥ˆà¥¤",
                "p": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/radio/mahabharat+banner.png",
                "pF": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/radio/Mahabharat+small.png",
                "pFBig": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/radio/mahabharat+player.png",
                "id": "Mahabharat"
            },
            {
                "t": "Sadhguru",
                "cat": "à¤§à¤°à¥ à¤® à¤”à¤° à¤…à¤§à¥ à¤¯à¤¾à¤¤à¥ à¤®",
                "d": "à¤¸à¤¦à¥ à¤—à¥ à¤°à¥ , à¤ à¤• à¤­à¤¾à¤°à¤¤à¥€à¤¯ à¤¯à¥‹à¤—à¥€ à¤”à¤° à¤°à¤¹à¤¸à¥ à¤¯à¤µà¤¾à¤¦à¥€ à¤¹à¥ˆà¤‚à¥¤ à¤‰à¤¨à¥ à¤¹à¥‹à¤‚à¤¨à¥‡ à¤ˆà¤¶à¤¾ à¤«à¤¾à¤‰à¤‚à¤¡à¥‡à¤¶à¤¨ à¤•à¥€ à¤¸à¥ à¤¥à¤¾à¤ªà¤¨à¤¾ à¤•à¥€ à¤¹à¥ˆà¥¤",
                "p": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/sadhguru+banner.png",
                "pF": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/ho-4.png",
                "pFBig": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/sadhguru+player.png",
                "id": "Sadhguru"
            },
            {
                "t": "Bhagavad Gita",
                "cat": "à¤§à¤°à¥ à¤® à¤”à¤° à¤…à¤§à¥ à¤¯à¤¾à¤¤à¥ à¤®",
                "d": "à¤¯à¤¹ à¤‘à¤¡à¤¿à¤¯à¥‹ à¤ªà¤¾à¤‚à¤¡à¤µ à¤°à¤¾à¤œà¤•à¥ à¤®à¤¾à¤° à¤…à¤°à¥ à¤œà¥ à¤¨ à¤”à¤° à¤‰à¤¨à¤•à¥‡ à¤®à¤¾à¤°à¥ à¤—à¤¦à¤°à¥ à¤¶à¤• à¤”à¤° à¤¸à¤¾à¤°à¤¥à¥€ à¤­à¤—à¤µà¤¾à¤¨ à¤•à¥ƒà¤·à¥ à¤£ à¤•à¥‡ à¤¬à¥€à¤š à¤ à¤• à¤¸à¤‚à¤µà¤¾à¤¦ à¤¹à¥ˆà¥¤ || A dialogue between Pandava prince Arjuna and his guide and charioteer Lord Krishna.",
                "p": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/geeta+banner.png",
                "pF": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/ho-8.png",
                "pFBig": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/geeta+player.png",
                "id": "gita"
            },
            {
                "t": "Krishna Wani",
                "cat": "à¤§à¤°à¥ à¤® à¤”à¤° à¤…à¤§à¥ à¤¯à¤¾à¤¤à¥ à¤®",
                "d": "à¤­à¤—à¤µà¤¾à¤¨à¥  à¤¶à¥ à¤°à¥€ à¤•à¥ƒà¤·à¥ à¤£ à¤•à¥‡ à¤¦à¥ à¤µà¤¾à¤°à¤¾ à¤†à¤§à¥ à¤¯à¤¾à¤¤à¥ à¤®à¤¿à¤• à¤µà¤¿à¤šà¤¾à¤°, à¤”à¤° à¤ªà¥ à¤°à¥‡à¤°à¤• à¤‰à¤¦à¥ à¤§à¤°à¤£ || Spiritual thoughts, motivational quotes from lord Krishna",
                "p": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/krishna+vaani+banner.png",
                "pF": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/ho-10.png",
                "pFBig": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/krishna+vaani+player.png",
                "id": "krishna-wani"
            }
        ]
    },
    {
        "title": "à¤•à¥‰à¤®à¥‡à¤¡à¥€",
        "data": [
            {
                "t": "RJ Naved",
                "c": "#E27C0B",
                "cat": "à¤•à¥‰à¤®à¥‡à¤¡à¥€",
                "d": "Hilarious prank calls from RJ Naved",
                "p": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/RJ+naved+banner.png",
                "pF": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/RJ+Naved+small.png",
                "pFBig": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/RJ+Naved+player.png",
                "id": "naved"
            },
            {
                "t": "Bauaa",
                "c": "#DA0019",
                "cat": "à¤•à¥‰à¤®à¥‡à¤¡à¥€",
                "d": "à¤¹à¥‡à¤²à¥‹ à¤‰à¤¨à¥ à¤•à¤¿à¤² à¤®à¥ˆà¤‚ à¤¬à¤‰à¤† à¤¬à¥‹à¤² à¤°à¤¹à¤¾ à¤¹à¥‚à¤ !",
                "p": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/bauaa+banner.png",
                "pF": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/bauuaa.png",
                "pFBig": "https://d51md7wh0hu8b.cloudfront.net/assets/app/prod/images/banner/bauaa+player.png",
                "id": "bauaa"
            }
        ]
    }
]
