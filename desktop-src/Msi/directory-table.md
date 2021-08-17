---
description: La tabella Directory specifica il layout della directory per il prodotto. Ogni riga della tabella indica una directory sia nell'origine che nella destinazione.
ms.assetid: eaca30cb-fec1-49ca-8b23-5e54c583e3e2
title: Tabella directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f19e9b5994062ac55564799854fc36016fc6ddb9887bc36aa9a94652ef31aeb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947345"
---
# <a name="directory-table"></a>Tabella directory

La tabella Directory specifica il layout della directory per il prodotto. Ogni riga della tabella indica una directory sia nell'origine che nella destinazione.

La tabella Directory include le colonne seguenti.



| Colonna            | Tipo                         | Chiave | Nullable |
|-------------------|------------------------------|-----|----------|
| Directory         | [Identificatore](identifier.md) | S   | N        |
| Padre \_ della directory | [Identificatore](identifier.md) | N   | S        |
| DefaultDir        | [DefaultDir](defaultdir.md) | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Directory"></span><span id="directory"></span><span id="DIRECTORY"></span>Directory
</dt> <dd>

La colonna Directory contiene un identificatore univoco per una directory o un percorso di directory. Questa colonna può contenere il nome di una proprietà impostata sul percorso completo di una directory di destinazione. Se questa colonna contiene una proprietà, la directory di destinazione accetta il nome specificato nella colonna DefaultDir e accetta la directory padre specificata nella colonna Directory \_ padre.

La directory di origine accetta sempre il nome specificato nella colonna DefaultDir e accetta la directory padre specificata nella colonna Directory \_ padre.

Se la colonna Padre directory è null o uguale al valore della colonna Directory, la \_ colonna Directory rappresenta una directory di destinazione radice. Nella tabella Directory può essere specificata una sola directory radice.

</dd> <dt>

<span id="Directory_Parent"></span><span id="directory_parent"></span><span id="DIRECTORY_PARENT"></span>Padre \_ della directory
</dt> <dd>

Questa colonna è un riferimento alla directory padre della directory. Un record con una colonna Padre directory uguale a Null o \_ uguale alla colonna Directory rappresenta una directory radice. Il percorso completo della directory padre viene risolto per riferimento nella colonna Directory \_ padre è una chiave esterna nella colonna Directory. Ad esempio, se una cartella ha una directory padre denominata PDIR, la directory padre di PDIR viene specificata nella colonna Directory padre della riga con PDIR nella \_ colonna Directory.

</dd> <dt>

<span id="DefaultDir"></span><span id="defaultdir"></span><span id="DEFAULTDIR"></span>DefaultDir
</dt> <dd>

La colonna DefaultDir contiene il nome della directory (localizzabile) nella directory padre. Per impostazione predefinita, si tratta del nome delle directory di destinazione e di origine. Per specificare nomi di directory di origine e di destinazione diversi, separare i nomi di destinazione e di origine con i due punti come indicato di seguito: \[ targetname \] : \[ sourcename \] .

Se il valore della colonna Padre directory è Null o è uguale alla colonna Directory, la colonna DefaultDir specifica il nome \_ di una directory di origine radice.

Per una directory di origine non radice, un punto (.) immesso nella colonna DefaultDir per il nome della directory di origine o il nome della directory di destinazione indica che la directory deve trovarsi nella directory padre senza una sottodirectory.

I nomi di directory in questa colonna possono essere formattati come coppie di nomi di file \| brevi di tipo long.

</dd> </dl>

## <a name="remarks"></a>Commenti

Ogni record nella tabella rappresenta una directory nelle immagini di origine e di destinazione. La tabella Directory deve specificare una singola directory radice con un valore di colonna Directory uguale alla [**proprietà TARGETDIR.**](targetdir.md)

Per [un'installazione amministrativa,](administrative-installation.md)installare l'immagine amministrativa nella directory radice denominata TARGETDIR e usare i nomi delle directory di origine per risolvere le directory di destinazione.

Si noti che il programma di installazione imposta una serie di proprietà standard [nei](properties.md) percorsi delle cartelle di sistema. Per un [elenco delle](property-reference.md) proprietà impostate su cartelle di sistema, vedere Informazioni di riferimento sulla proprietà.

La risoluzione della directory viene eseguita [durante l'azione CostFinalize](costfinalize-action.md) e viene eseguita come segue:

### <a name="root-destination-directory"></a>Directory di destinazione radice

Può essere presente una sola directory di destinazione radice. Per specificare la directory di destinazione radice, impostare la colonna Directory sulla [**proprietà TARGETDIR**](targetdir.md) e la colonna DefaultDir sulla [**proprietà SourceDir.**](sourcedir.md) Se la **proprietà TARGETDIR** è definita, la directory di destinazione viene risolta nel valore della proprietà. Se la **proprietà TARGETDIR** non è definita, la [**proprietà ROOTDRIVE**](rootdrive.md) viene usata per risolvere il percorso.

### <a name="root-source-directory"></a>Directory di origine radice

Il valore della colonna DefaultDir per la voce della directory radice deve essere impostato sulla [**proprietà SourceDir.**](sourcedir.md)

### <a name="non-root-destination-directories"></a>Directory di destinazione non radice

Il valore Directory per una directory non radice viene interpretato anche come il nome di una proprietà che definisce il percorso della destinazione. Se la proprietà è definita, la directory di destinazione viene risolta nel valore della proprietà. Se la proprietà non è definita, la directory di destinazione viene risolta in una sottodirectory sotto la directory di destinazione risolta per la voce Directory \_ padre. Il valore DefaultDir definisce il nome della sottodirectory.

### <a name="non-root-source-directories"></a>Directory di origine non radice

La directory di origine per una directory non radice viene risolta in una sottodirectory della directory di origine risolta per la voce Directory \_ padre. Anche in questo caso, il valore DefaultDir definisce il nome della sottodirectory.

### <a name="short-or-long-file-names"></a>Nomi di file brevi o lunghi

Durante la risoluzione delle directory di destinazione, i nomi di file brevi specificati nella colonna DefaultDir vengono usati se è impostata la proprietà [**SHORTFILENAMES**](shortfilenames.md) o se il volume in cui si trova la directory non supporta nomi di file lunghi. In caso contrario, viene usato il nome file lungo.

Si noti che quando le directory vengono risolte durante l'azione CostFinalize, le chiavi nella tabella Directory diventano [proprietà](properties.md) impostate su percorsi di directory.

[Tabella CreateFolder](createfolder-table.md)

Per la creazione di cartelle vuote durante un'installazione, vedere [CreateFolder Table](createfolder-table.md).

[Uso della tabella directory](using-the-directory-table.md)

Per altre informazioni sulla tabella Directory, inclusi gli esempi, vedere [Uso della tabella directory](using-the-directory-table.md).

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

 

 



