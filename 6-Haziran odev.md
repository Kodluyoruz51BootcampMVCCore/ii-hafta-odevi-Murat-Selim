## Github vs Bitbucket ##

Bitbucket, Git veya Mercurial gibi VCS(Version Control System) kullanan projeler için bir web depolama servisidir. Bitbucket fiyat açısından githuba göre daha ucuzdur. Github kullanıcı sayısında 3 milyon ile, bitbucketı geçmektedir. Bitbucket 1 milyon kullanıcıya sahiptir. Bitbucket  hem Git’i hem de Mercurial’i desteklemektedir. Github ise sadece Git’i desteklemektedir.

## Github vs Svn (Subversion) ##

Github merkezi olmayan, dagıtık bir yapıya sahip, Svn de ise aksi durum sözkonusu. Github ta  merge ve branch islemleri hızlı oluyor. Github çevrimdışı olarak ta çalışabiliyor. SVN'nin ise ayrı bir sunucusu ve istemcisi vardır. Yalnızca bir geliştiricinin uzerinde calıştığı dosyalar yerel makinede tutulur ve geliştiricinin sunucu ile çalışarak çevrimiçi olması gerekir. Kullanıcılar dosyaları teslim alır ve sunucuda değişiklik yapar.

## Git and Github with Briana Swift ##

 - **1.bölüm  - Github Workflow**
   
   branch Commit, pull request, merge 
   
 - **2.bölüm  -  Working Locally**
   
   git clone - copies repo, All branches, All history
   git remote -v -original remote, other remotes forks upstream 
   
 - **3.bölüm  - Git Status**
   
   Head pointer, working directory, staging area, compare remote, tracking branch, suggestions
   
 - **4.bölüm  - Saved Changes**
   
   git add - working area
   git commit - staging area
   git log - remote repos
   
 - **5.bölüm  - Git pull vs Git puss**
   
   git pull - update local, git fetch, git merge
   git push - update remote, current branch
   
 - **6.bölüm  - Git reset**
   
   git reset --soft, git reset, git  reset --hard
   
 - **7.bölüm  - Merge Strategies**
   
   fast forward merge - rebase, no new commıts, on master, no merge commit, linear history
   recursive merge - no-ff, new commits, merge, commit created, commit - 2parent
   
 - **8.bölüm  - Organizasion Teams**
   
   Organize takım halinde çalışma ortamı

 - **9.bölüm  - Migrate to Github**
   
   Code History, İntagration, QA process, code review -- keep-change
   
 - **10.bölüm  - İntegrations**
   
   Project Management, Monitoring, C.I, Deploy
   
 - **11.bölüm - Changing History**
   
   Parent/Child
   Safe, .Git revert 
   Possiply Dangerous - git reset, git rebase, git commit -- amend, git cherry pick

**Merge** - Merging en basit anlamda herhangi bir branch'te yaptığımız değişiklikleri master branch'imiz ile birleştirme veya master branch'e entegre etme işlemidir.

**Pull Request** - Ben projede değişiklikleri yaptım, sen de bu bu değişiklikleri onayla ve projene merge et, ben de katkı sağlamış olayım demek.

**Create a Merge Commit** - Github'da birleştirme isteği ister ve bunları bir birleştirme taahhüdünde yeni bir taahhütle ana mastere ekler.

**Squase and Merge** - Squash ve birleştirme tüm özellik dalı taahhütlerini tek bir taahhütte gruplandıracak, sonra ana dalın önüne ekleyecek.

**Rebase and Merge** - Yeniden oluşturur ve birleştirir. Özellik dalının tüm taahhüt tarihini ana dalın önüne ekler.

**issue ve #pull request de id ler neden artıyor farklı sekmeler olmasına rağmen?** https://developer.github.com/v3/issues/

**Ramp up on Git and GitHub: Başlandı** https://lab.github.com/githubtraining/introduction-to-github

## Aspnetboilerplate ve yan ürünler araştırması ##

   **Abp-Template vs AspNet Zero**
    
   ASP.NET Boilerplate is an open-source web application framework which is also developed by 
   the same team who develops ASP.NET Zero. ASP.NET Boilerplate also provides free startup templates. 
   Here you can see the differences between ASP.NET Boilerplate's free templates and ASP.NET Zero.
   https://docs.aspnetzero.com/en/common/latest/Abp-Template-vs-AspNet-Zero
    
   **DNTFrameworkCore vs ABP Framework**
    
   ABP is one of most popular and well documented frameworks with high level abstraction that
   I learned a lot from it. It has many other features that I don’t list them in this post,
   because, DNTFrameworkCore has not them actually. Behind of ABP, there is a team. 
   It has 123 contributors in GitHub. Also, all of features have related unit-tests. 
   https://medium.com/@rabbal/dntframeworkcore-vs-abp-framework-b48f5b7f8a24

Hackerrank başlandı: https://www.hackerrank.com/domains/tutorials/30-days-of-code?filters%5Bstatus%5D%5B%5D=unsolved&badge_type=30-days-of-code
