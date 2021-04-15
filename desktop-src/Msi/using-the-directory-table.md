---
description: La tabella directory specifica il layout di un'installazione.
ms.assetid: 3f2e1cc2-6b36-4615-86e6-e78485edd2f7
title: Uso della tabella di directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7218fe6f6e2ca36bc0c52e74b564ad07d87053a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231852"
---
# <a name="using-the-directory-table"></a>Uso della tabella di directory

La [tabella directory](directory-table.md) specifica il layout di un'installazione. Quando le directory vengono risolte durante l' [azione CostFinalize secondo](costfinalize-action.md), le chiavi della tabella directory diventano [Proprietà](properties.md) impostate sui percorsi di directory. Si noti che il programma di installazione imposta una serie di [Proprietà](properties.md) standard sui percorsi di cartella di sistema. Per un elenco delle proprietà impostate sulle cartelle di sistema, vedere il [riferimento alla proprietà](property-reference.md) .

Il modo migliore per specificare il percorso di destinazione per una directory è la creazione della [tabella di directory](directory-table.md) nel pacchetto di installazione per fornire il percorso corretto, come descritto in questa sezione. Se è necessario modificare il percorso della directory al momento dell'installazione, vedere anche la sezione relativa alla [modifica del percorso di destinazione per una directory](changing-the-target-location-for-a-directory.md)

Di seguito è riportato un esempio di tabella di directory.



| Directory     | \_Padre directory | DefaultDir |
|---------------|-------------------|------------|
| TARGETDIR     |                   | SourceDir  |
| EXEDIR        | TARGETDIR         | App        |
| DLLDIR        | EXEDIR            | Contenitore        |
| Includevano | TARGETDIR         | Desktop    |



 

Ogni riga della tabella di directory indica una directory sia nell'origine che nella destinazione. Si supponga, ad esempio, che il pacchetto di installazione si trovi nell' \\ \\ \\ origine applicazioni \\ . Poiché il \_ campo padre della directory della prima riga è null, questo record indica le directory radice sia per l'origine che per la destinazione. Per l'origine, il valore di questa directory viene fornito dal campo DefaultDir. Per impostazione predefinita, la proprietà [**SourceDir**](sourcedir.md) viene impostata sul percorso del pacchetto di installazione. Pertanto, a meno che la proprietà **SourceDir** non venga sottoposta a override, la directory di origine radice è \\ \\ Applications \\ source \\ .

Il campo Directory del primo record indica il percorso della directory di destinazione radice. In questo caso, il valore della proprietà [**targetdir**](targetdir.md) indica questa directory. In genere, il valore della proprietà **targetdir** viene impostato dalla riga di comando o tramite un'interfaccia utente. In questo caso, si supponga che la proprietà **targetdir** sia impostata su C: \\ Program Files \\ target \\ .

Per il secondo record, il \_ campo padre della directory non è null. Questo record indica pertanto una directory non radice sia per l'origine che per la destinazione. Per una directory di origine non radice, la directory di origine indicata dal record descritto nel \_ campo padre della directory è la directory padre. Per il secondo record, il \_ campo padre della directory è TARGETDIR. Come illustrato in precedenza, la directory di origine indicata dal record TARGETDIR è stata risolta in \\ \\ Applications \\ source \\ . La directory di origine indicata dal secondo record è quindi \\ \\ app di \\ origine delle applicazioni \\ \\ .

Un processo simile funziona per la directory di destinazione. Il valore della directory padre per la directory di destinazione descritta nel secondo record è la directory di destinazione risolta dal \_ campo padre della directory. Anche in questo caso il \_ campo padre della directory contiene il valore TARGETDIR. Indica il primo record che viene risolto in una directory di destinazione della destinazione C: \\ Program Files \\ \\ . Il campo Directory contiene una proprietà definita dall'autore denominata EXEDIR. Se questa proprietà è impostata, il relativo valore fornisce il percorso completo della directory. Pertanto, se questa proprietà è impostata su C: \\ data \\ Common \\ , il valore della directory di destinazione indicata dal secondo record è C: \\ data \\ Common \\ . Se non è impostato, la directory di destinazione acquisisce il nome specificato dal campo DefaultDir. In questo caso, la directory di destinazione è C: \\ Program Files \\ target \\ app \\ .

Lo stesso processo funziona per il terzo record. Se EXEDIR e DLLDIR non sono impostati, la directory di destinazione è C: \\ Program Files \\ destinazione \\ app \\ bin e la directory di origine è \\ \\ Applications \\ source \\ bin app \\ \\ .

Il quarto record usa la proprietà [**includevano**](desktopfolder.md) . Se il percorso del desktop dell'utente è C: \\ WinNT \\ profili \\ utente \\ Desktop \\ , la directory di destinazione viene risolta in c: \\ WinNT \\ profili \\ utente \\ Desktop \\ . La directory di origine viene risolta nel \\ \\ desktop di origine dell'applicazione \\ \\ \\ .

Sono disponibili altre due funzionalità di sintassi che è possibile usare nella colonna DefaultDir della tabella directory. Per una directory di origine non radice, un punto (.) immesso nella colonna DefaultDir indica che la directory deve trovarsi nella directory padre senza una sottodirectory. Per specificare percorsi di directory di origine e di destinazione diversi, separare i percorsi di destinazione e di origine nella colonna DefaultDir con i due punti, come segue: \[ targetPath \] : \[ SourcePath \] . Queste funzionalità possono essere usate insieme per aggiungere livelli ai percorsi di origine o di destinazione per una singola directory. Vedere l'esempio seguente di una tabella di directory.



| Directory   | \_Padre directory | DefaultDir |
|-------------|-------------------|------------|
| TARGETDIR   |                   | SourceDir  |
| MyAppDir    | TARGETDIR         | MyApp      |
| BinDir      | MyAppDir          | Contenitore        |
| Binx86Dir   | BinDir            | .: x86      |
| BinAlphaDir | BinDir            | .: Alfa    |



 

I percorsi di origine e di destinazione vengono risolti per le righe MyAppDir, BinDir, Binx86Dir e BinAlphaDir come indicato di seguito.



| Registra       | Percorsi di destinazione            | Percorsi di origine                   |
|--------------|-------------------------|--------------------------------|
| MyAppDir:    | \[TARGETDIR \] MyApp      | \[SourceDir \] MyApp             |
| BINDIR      | \[TARGETDIR \] MyApp \\ bin | \[SourceDir \] MyApp \\ bin        |
| Binx86Dir:   | \[TARGETDIR \] MyApp \\ bin | \[SourceDir \] MyApp \\ bin \\ x86   |
| BinAlphaDir: | \[TARGETDIR \] MyApp \\ bin | \[SourceDir \] MyApp \\ bin \\ Alpha |



 

> [!Note]  
> La piattaforma Alpha non è supportata dal Windows Installer.

 

 

 



