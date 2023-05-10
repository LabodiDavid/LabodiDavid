![Intro GIF](intro.gif)
![Linkedin Badge](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white&link=https://www.linkedin.com/in/labodidavid/)
![Personal Website Badge](https://img.shields.io/badge/website-000000?style=for-the-badge&logo=About.me&logoColor=white&link=https://labodidavid.hu)
![Visitors Badge](https://visitor-badge.laobi.icu/badge?page_id=labodidavid.labodidavid)
<hr/>

## 🛠️ I'm familiar with..
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-239120?&style=for-the-badge&logo=css3&logoColor=white)
![SASS](https://img.shields.io/badge/Sass-CC6699?style=for-the-badge&logo=sass&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![NodeJS](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)
![JQuery](https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white)
![Wordpress](https://img.shields.io/badge/Wordpress-21759B?style=for-the-badge&logo=wordpress&logoColor=white)
<br/>
![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white)
<br/>
![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Shell](https://img.shields.io/badge/Shell_Script-121011?style=for-the-badge&logo=gnu-bash&logoColor=white)
<br/>
![Docker](https://img.shields.io/badge/-Docker-black?style=for-the-badge&logo=docker)
![Apache](https://img.shields.io/badge/apache-%23D42029.svg?style=for-the-badge&logo=apache&logoColor=white)
![Nginx](https://img.shields.io/badge/nginx-%23009639.svg?style=for-the-badge&logo=nginx&logoColor=white)
![Jenkins](https://img.shields.io/badge/jenkins-%232C5263.svg?style=for-the-badge&logo=jenkins&logoColor=white)
![Cisco](https://img.shields.io/badge/cisco-%23049fd9.svg?style=for-the-badge&logo=cisco&logoColor=black)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=for-the-badge&logo=Cloudflare&logoColor=white)
![Debian](https://img.shields.io/badge/Debian-A81D33?style=for-the-badge&logo=debian&logoColor=white)
![Microsoft](https://img.shields.io/badge/Microsoft-666666?style=for-the-badge&logo=microsoft&logoColor=white)
![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white)
![Windows Terminal](https://img.shields.io/badge/Windows%20Terminal-%234D4D4D.svg?style=for-the-badge&logo=windows-terminal&logoColor=white)
<br/>
![Gitea](https://img.shields.io/badge/Gitea-34495E?style=for-the-badge&logo=gitea&logoColor=5D9425)
![GitLab](https://img.shields.io/badge/gitlab-%23181717.svg?style=for-the-badge&logo=gitlab&logoColor=white)
<br/>
![After Effects](https://img.shields.io/badge/Adobe%20after%20affects-CF96FD?style=for-the-badge&logo=Adobe%20after%20effects&logoColor=393665)
![Premiere Pro](https://img.shields.io/badge/Adobe%20Premiere%20Pro-9999FF?style=for-the-badge&logo=Adobe%20Premiere%20Pro&logoColor=white)
<br/>
![PHPStorm](http://img.shields.io/badge/-PHPStorm-181717?style=for-the-badge&logo=phpstorm&logoColor=white)
![IntelliJ](https://img.shields.io/badge/IntelliJ_IDEA-000000.svg?style=for-the-badge&logo=intellij-idea&logoColor=white)
![Visual Studio](https://img.shields.io/badge/Visual_Studio-5C2D91?style=for-the-badge&logo=visual%20studio&logoColor=white)
![Notepad++](https://img.shields.io/badge/Notepad++-90E59A.svg?style=for-the-badge&logo=notepad%2b%2b&logoColor=black)
![Eclipse](https://img.shields.io/badge/Eclipse-2C2255?style=for-the-badge&logo=eclipse&logoColor=white)
![Atom](https://img.shields.io/badge/Atom-66595C?style=for-the-badge&logo=Atom&logoColor=white)
<br/>
![Udemy](https://img.shields.io/badge/Udemy-EC5252?style=for-the-badge&logo=Udemy&logoColor=white)
<hr/>

![codersrank.io - summary widget](https://cr-ss-service.azurewebsites.net/api/ScreenShot?widget=summary&username=labodidavid&branding=false)

<hr/>
<details><summary><strong>☕ Click here to see an introduce of myself in PHP laravel ☕</strong></summary>

```php
namespace World\Earth\Europe\Hungary;

use Illuminate\Database\Eloquent\Relations\BelongsToMany;
use App\Models\Question;
use App\Models\Solution;
use App\Models\Knowledge;
use Udemy;
use Google;
use StackOverFlow;
use GPT;

class Labodi_David extends People
{
use HasMotivation, HasGoals;

    protected $fillable = ['coffee', 'knowledge'];

    public function __construct()
    {
        $this->middleware(['PreventRequestsWithoutCoffee', 'IT_Administrator', 'Programmer']);
    }
    
    /**
     * Find the solution to a question.
     *
     * @param  Question  $question
     * @return Solution
     */
    public function findSolution(Question $question): Solution
    {
        if ($this->knowledge->contains($question)) {
            return $this->knowledge()->getSolution($question);
        }
        
        return $this->learn($question)->getSolution();
    }
    
    /**
     * Learn about a question and gather knowledge.
     *
     * @param  Question  $question
     * @return Knowledge
     * @throws CoffeeNotFoundException
     */
    private function learn(Question $question): Knowledge
    {
        $knowledge = new Knowledge();
        if ($this->hasDrankCoffee()) {
            while (!$knowledge->hasInformation()){
                $knowledge->collectInformation([
                    Google::search($question),
                    StackOverFlow::search($question),
                    GPT::ask($question)
                ]);
            }
            return $this->knowledge()->save($knowledge);
        } else {
            throw new CoffeeNotFoundException();
        }
    }
    
    /**
     * Get the knowledge relation.
     *
     * @return BelongsToMany
     */
    public function knowledge(): BelongsToMany
    {
        return $this->belongsToMany(Knowledge::class);
    }
    
    /**
     * Check if David has drank coffee.
     *
     * @return bool
     */
    private function hasDrankCoffee(): bool
    {
        return !empty($this->coffee);
    }
}

```

</details>

<hr/>

#### 🔥 Fancy stuffs I used in this profile README:

 - [Typing intro](https://codesandbox.io/s/readme-introgif-9fjo5) (𝚅𝚞𝚎 𝙿𝚊𝚛𝚝𝚒𝚌𝚕𝚎𝙹𝚜 𝚊𝚗𝚍 𝚅𝚞𝚎.𝚓𝚜) by [Raymo111](https://github.com/Raymo111)
 - [shields.io](https://shields.io/) badges
 - [visitor-badge](https://github.com/hehuapei/visitor-badge) by [hehuapei](https://github.com/hehuapei)
 - [Summary Widget](https://docs.codersrank.io/widgets/summary-widget) by [CodersRank.io](https://codersrank.io)