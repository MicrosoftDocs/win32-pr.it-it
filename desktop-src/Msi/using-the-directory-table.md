---
description: La tabella Directory specifica il layout di un'installazione.
ms.assetid: 3f2e1cc2-6b36-4615-86e6-e78485edd2f7
title: Uso della tabella directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f550f32006df16db5811e0fbf5022253373a4b1551983ddda2db55655b4061f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141320"
---
# <a name="using-the-directory-table"></a>Uso della tabella directory

La [tabella Directory](directory-table.md) specifica il layout di un'installazione. Quando le directory vengono risolte durante [l'azione CostFinalize](costfinalize-action.md), le chiavi nella tabella Directory [diventano](properties.md) proprietà impostate su percorsi di directory. Si noti che il programma di installazione imposta una serie di proprietà standard [per](properties.md) i percorsi delle cartelle di sistema. Per un [elenco delle](property-reference.md) proprietà impostate su cartelle di sistema, vedere Informazioni di riferimento sulla proprietà.

Il modo migliore per specificare il percorso di destinazione per una directory è creare la tabella [Directory](directory-table.md) nel pacchetto di installazione per specificare il percorso corretto come descritto in questa sezione. Se è necessario modificare il percorso della directory al momento dell'installazione, vedere anche la sezione: Modifica del percorso [di destinazione per una directory](changing-the-target-location-for-a-directory.md)

Di seguito è riportato un esempio di tabella Directory.



| Directory     | Padre \_ della directory | DefaultDir |
|---------------|-------------------|------------|
| Targetdir     |                   | SourceDir  |
| EXEDIR        | Targetdir         | App        |
| DLLDIR        | EXEDIR            | Contenitore        |
| DesktopFolder | Targetdir         | Desktop    |



 

Ogni riga della tabella Directory indica una directory sia nell'origine che nella destinazione. Si supponga, ad esempio, che il pacchetto di installazione si trovi \\ \\ nell'origine \\ delle applicazioni \\ . Poiché il campo Padre directory della prima riga è Null, questo record indica le directory radice sia per \_ l'origine che per la destinazione. Per l'origine, il valore di questa directory viene specificato dal campo DefaultDir. Il valore predefinito della proprietà [**SourceDir**](sourcedir.md) è il percorso del pacchetto di installazione. Pertanto, a meno che **la proprietà SourceDir** non venga sottoposta a override, la directory di origine radice è \\ \\ l'origine \\ delle applicazioni \\ .

Il campo Directory del primo record indica il percorso della directory di destinazione radice. In questo caso, il valore della [**proprietà TARGETDIR**](targetdir.md) indica questa directory. In genere, il valore della **proprietà TARGETDIR** viene impostato nella riga di comando o tramite un'interfaccia utente. In questo caso, si supponga che la **proprietà TARGETDIR** sia impostata su C: \\ Programmi di destinazione \\ \\ .

Per il secondo record, il campo Padre \_ directory non è Null. Pertanto, questo record indica una directory non radice sia per l'origine che per la destinazione. Per una directory di origine non radice, la directory di origine indicata dal record descritto nel campo Padre directory \_ è la directory padre. Per il secondo record, il campo Padre \_ directory è TARGETDIR. Come illustrato in precedenza, la directory di origine indicata dal record TARGETDIR risolto \\ \\ nell'origine delle applicazioni \\ \\ . Di conseguenza, la directory di origine indicata dal secondo record è \\ \\ \\ l'applicazione di origine App \\ \\ .

Un processo simile funziona per la directory di destinazione. Il valore della directory padre per la directory di destinazione descritta nel secondo record è la directory di destinazione risolta dal campo Directory \_ padre. Anche in questo caso, \_ il campo Padre directory contiene il valore TARGETDIR. Indica il primo record che viene risolto in una directory di destinazione di C: \\ Programmi \\ di destinazione \\ . Il campo Directory contiene una proprietà definita dall'autore denominata EXEDIR. Se questa proprietà è impostata, il relativo valore fornisce il percorso completo della directory. Pertanto, se questa proprietà è impostata su C: Dati comuni , il valore della directory di destinazione indicata dal \\ \\ secondo record è \\ C: Dati comuni \\ \\ \\ . Se non è impostata, la directory di destinazione accetta il nome specificato dal campo DefaultDir. In questo caso, la directory di destinazione è C: \\ Programmi App di destinazione \\ \\ \\ .

Lo stesso processo funziona per il terzo record. Se EXEDIR e DLLDIR non sono impostati, la directory di destinazione è C: Program Files Target App Bin e la directory di origine è il Bin app \\ \\ di origine delle \\ \\ \\ \\ \\ \\ \\ \\ applicazioni.

Il quarto record usa la [**proprietà DesktopFolder.**](desktopfolder.md) Se il percorso del desktop dell'utente è C: Winnt Profiles User Desktop, la directory di destinazione viene risolta \\ \\ in \\ \\ \\ C: \\ Winnt Profiles User Desktop \\ \\ \\ \\ . La directory di origine viene risolta \\ \\ \\ nell'origine delle applicazioni Desktop \\ \\ .

Nella colonna DefaultDir della tabella Directory è possibile usare due funzionalità di sintassi aggiuntive. Per una directory di origine non radice, un punto (.) immesso nella colonna DefaultDir indica che la directory deve trovarsi nella directory padre senza una sottodirectory. Per specificare percorsi di directory di origine e di destinazione diversi, separare i percorsi di destinazione e di origine nella colonna DefaultDir con i due punti come indicato di seguito: \[ targetpath \] : \[ sourcepath \] . Queste funzionalità possono essere usate insieme per aggiungere livelli ai percorsi di origine o di destinazione per una singola directory. Vedere l'esempio seguente di una tabella Directory.



| Directory   | Padre \_ della directory | DefaultDir |
|-------------|-------------------|------------|
| Targetdir   |                   | SourceDir  |
| MyAppDir    | Targetdir         | Myapp      |
| BinDir      | MyAppDir          | Contenitore        |
| Binx86Dir   | BinDir            | .:x86      |
| BinAlphaDir | BinDir            | .:Alpha    |



 

I percorsi di origine e di destinazione vengono risolti per le righe MyAppDir, BinDir, Binx86Dir e BinAlphaDir come indicato di seguito.



| Registra       | Percorsi di destinazione            | Percorsi di origine                   |
|--------------|-------------------------|--------------------------------|
| MyAppDir:    | \[TARGETDIR \] MyApp      | \[SourceDir \] MyApp             |
| BinDir:      | \[TARGETDIR \] MyApp \\ Bin | \[SourceDir \] MyApp \\ Bin        |
| Binx86Dir:   | \[TARGETDIR \] MyApp \\ Bin | \[SourceDir \] MyApp \\ Bin \\ x86   |
| BinAlphaDir: | \[TARGETDIR \] MyApp \\ Bin | \[SourceDir \] MyApp \\ Bin \\ Alpha |



 

> [!Note]  
> La piattaforma Alpha non è supportata dal programma di Windows di installazione.

 

 

 



