# wheel-of-pes-clubs

pes clubs to json script:

```
let data = []
for (var i = 0; i < leagues.length; i++) {
    const leagueName = leagues[i].getElementsByClassName('league-name')?.[0]?.innerHTML;
    // console.log(leagueName)
    const clubList = leagues[i].getElementsByClassName('club-list')?.[0]?.getElementsByTagName('li')
    let teamNames = []
    for (var j = 0; j < clubList.length; j++) {
        const clubName = clubList[j].innerText
        // console.log('#', clubName)
        teamNames.push({name: clubName})
    }
    data.push({leagueName, teams: teamNames})
}
console.log(JSON.stringify(data))
```