---
description: La tabella directory specifica il layout di directory per il prodotto. Ogni riga della tabella indica una directory sia nell'origine che nella destinazione.
ms.assetid: eaca30cb-fec1-49ca-8b23-5e54c583e3e2
title: Tabella directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273445aef67e3f166255321d0ac0ccf1aee37515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967810"
---
# <a name="directory-table"></a>Tabella directory

La tabella directory specifica il layout di directory per il prodotto. Ogni riga della tabella indica una directory sia nell'origine che nella destinazione.

La tabella di directory contiene le colonne seguenti.



| Colonna            | Tipo                         | Chiave | Nullable |
|-------------------|------------------------------|-----|----------|
| Directory         | [Identificatore](identifier.md) | S   | N        |
| \_Padre directory | [Identificatore](identifier.md) | N   | S        |
| DefaultDir        | [DefaultDir](defaultdir.md) | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Directory"></span><span id="directory"></span><span id="DIRECTORY"></span>Directory
</dt> <dd>

La colonna directory contiene un identificatore univoco per una directory o un percorso di directory. Questa colonna può contenere il nome di una proprietà impostata sul percorso completo di una directory di destinazione. Se questa colonna contiene una proprietà, la directory di destinazione acquisisce il nome specificato nella colonna DefaultDir e acquisisce la directory padre specificata nella \_ colonna padre della directory.

La directory di origine accetta sempre il nome specificato nella colonna DefaultDir e accetta la directory padre specificata nella \_ colonna padre della directory.

Se la \_ colonna padre della directory è null o uguale al valore della colonna directory, la colonna directory rappresenta una directory di destinazione radice. Nella tabella directory è possibile specificare una sola directory radice.

</dd> <dt>

<span id="Directory_Parent"></span><span id="directory_parent"></span><span id="DIRECTORY_PARENT"></span>\_Padre directory
</dt> <dd>

Questa colonna è un riferimento alla directory padre della directory. Un record con una \_ colonna padre della directory uguale a null o uguale alla colonna di directory rappresenta una directory radice. Il percorso completo della directory padre viene risolto per riferimento nella \_ colonna padre della directory è una chiave esterna nella colonna directory. Se, ad esempio, in una cartella è presente una directory padre denominata PDIR, la directory padre di PDIR viene specificata nella \_ colonna padre della directory della riga con PDIR nella colonna directory.

</dd> <dt>

<span id="DefaultDir"></span><span id="defaultdir"></span><span id="DEFAULTDIR"></span>DefaultDir
</dt> <dd>

La colonna DefaultDir contiene il nome della directory (localizzabile) nella directory padre. Per impostazione predefinita, si tratta del nome delle directory di destinazione e di origine. Per specificare nomi di directory di origine e di destinazione diversi, separare i nomi di destinazione e di origine con i due punti, come indicato di seguito: \[ TargetName \] : \[ SourceName \] .

Se il valore della \_ colonna padre della directory è null o è uguale alla colonna di directory, la colonna DefaultDir specifica il nome di una directory di origine radice.

Per una directory di origine non radice, un punto (.) immesso nella colonna DefaultDir per il nome della directory di origine o il nome della directory di destinazione indica che la directory deve trovarsi nella directory padre senza una sottodirectory.

I nomi di directory in questa colonna possono essere formattati come coppie nome file breve nomefile \| lungo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Ogni record della tabella rappresenta una directory nelle immagini di origine e di destinazione. La tabella directory deve specificare una singola directory radice con un valore di colonna di directory uguale alla proprietà [**targetdir**](targetdir.md) .

Per un' [installazione amministrativa](administrative-installation.md), installare l'immagine amministrativa nella directory radice denominata TARGETDIR e usare i nomi delle directory di origine per risolvere le directory di destinazione.

Si noti che il programma di installazione imposta una serie di [Proprietà](properties.md) standard sui percorsi di cartella di sistema. Per un elenco delle proprietà impostate sulle cartelle di sistema, vedere il [riferimento alla proprietà](property-reference.md) .

La risoluzione della directory viene eseguita durante l' [azione CostFinalize secondo](costfinalize-action.md) e viene eseguita nel modo seguente:

### <a name="root-destination-directory"></a>Directory di destinazione radice

Può essere presente una sola directory di destinazione radice. Per specificare la directory di destinazione radice, impostare la colonna della directory sulla proprietà [**targetdir**](targetdir.md) e la colonna DefaultDir sulla proprietà [**SourceDir**](sourcedir.md) . Se la proprietà **targetdir** è definita, la directory di destinazione viene risolta nel valore della proprietà. Se la proprietà **targetdir** è indefinita, per risolvere il percorso viene utilizzata la proprietà [**ROOTDRIVE**](rootdrive.md) .

### <a name="root-source-directory"></a>Directory di origine radice

Il valore della colonna DefaultDir per la voce della directory radice deve essere impostato sulla proprietà [**SourceDir**](sourcedir.md) .

### <a name="non-root-destination-directories"></a>Directory di destinazione non radice

Il valore della directory per una directory non radice viene anche interpretato come il nome di una proprietà che definisce la posizione della destinazione. Se la proprietà è definita, la directory di destinazione viene risolta nel valore della proprietà. Se la proprietà non è definita, la directory di destinazione viene risolta in una sottodirectory sotto la directory di destinazione risolta per la \_ voce padre della directory. Il valore DefaultDir definisce il nome della sottodirectory.

### <a name="non-root-source-directories"></a>Directory di origine non radice

La directory di origine per una directory non radice viene risolta in una sottodirectory della directory di origine risolta per la \_ voce padre della directory. Anche in questo caso, il valore di DefaultDir definisce il nome della sottodirectory.

### <a name="short-or-long-file-names"></a>Nomi di file brevi o lunghi

Quando si risolvono le directory di destinazione, i nomi di file brevi specificati nella colonna DefaultDir vengono utilizzati se la proprietà [**SHORTFILENAMES**](shortfilenames.md) è impostata o se il volume in cui si trova la directory non supporta nomi di file lunghi. In caso contrario, viene utilizzato il nome file lungo.

Si noti che quando le directory vengono risolte durante l'azione CostFinalize secondo, le chiavi della tabella directory diventano [Proprietà](properties.md) impostate sui percorsi di directory.

[Tabella CreateFolder](createfolder-table.md)

Per la creazione di cartelle vuote durante un'installazione, vedere [tabella CreateFolder](createfolder-table.md).

[Uso della tabella di directory](using-the-directory-table.md)

Per ulteriori informazioni sulla tabella di directory, inclusi gli esempi, vedere [utilizzo della tabella directory](using-the-directory-table.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE07](ice07.md)  
[ICE30](ice30.md)  
[ICE32](ice32.md)  
[ICE38](ice38.md)  
[ICE46](ice46.md)  
[ICE48](ice48.md)  
[ICE56](ice56.md)  
[ICE57](ice57.md)  
[ICE64](ice64.md)  
[ICE88](ice88.md)  
[ICE90](ice90.md)  
[ICE91](ice91.md)  
[ICE99](ice99.md)  
</dl>

 

 



