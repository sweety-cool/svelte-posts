<script>
    export let data;
</script>

<div class="post">
    <div class="header">
        <p>{data.username}</p>
    </div>
    <div class="image">
        <img src={data.image} alt="" />
    </div>
    <div class="footer">
        <p>{data.likes} Likes</p>
        <p>{data.comments} Comments</p>
    </div>
</div>

<style>
    .post {
        border: 1px solid #aaa;
        border-radius: 3px;
        margin-bottom: 2rem;
        background: #fff;
    }

    .header {
        padding: 0.5rem 2rem;
        border-bottom: 1px solid #aaa;
        font-weight: bold;
    }

    .image {
        border-bottom: 1px solid #aaa;
    }

    .footer {
        padding: 0.5rem 2rem;
    }
</style>
