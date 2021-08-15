---
title: DocumentSummaryInformation e set di proprietà definiti dall'utente
description: Un set di proprietà DocumentSummaryInformation e UserDefined è un'estensione del set di proprietà Summary Information. Entrambi i set di proprietà possono esistere contemporaneamente.
ms.assetid: c6d4e2bc-f7f6-429d-aa91-432d833c69d1
keywords:
- DocumentSummaryInformation
- Set di proprietà definite dall'utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d76c679fd8b4059e821598bed37d68735c45f914e4685e43a1c514b832e199e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886837"
---
# <a name="the-documentsummaryinformation-and-userdefined-property-sets"></a>DocumentSummaryInformation e set di proprietà definiti dall'utente

Un **set di proprietà DocumentSummaryInformation** e **UserDefined** è un'estensione del set di proprietà [Summary Information](the-summary-information-property-set.md). Entrambi i set di proprietà possono esistere contemporaneamente.

Il nome del flusso che contiene il set **di proprietà DocumentSummaryInformation** è **" \\ 005DocumentSummaryInformation".** L'identificatore di formato (FMTID) per il set di proprietà **DocumentSummaryInformation** è **D5CDD502-2E9C-101B-9397-08002B2CF9AE**.

La dichiarazione per questo valore è disponibile nei file di intestazione **forniti come FMTID \_ DocSummaryInformation.** Per altre informazioni, vedere [Names in IStorage](names-in-istorage.md), [The Summary Information Property Set](the-summary-information-property-set.md), [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) e [Format Identifiers.](format-identifiers.md)

Questo flusso include anche una sezione separata per le proprietà definite dall'utente personalizzate, come nei set di proprietà **DocumentSummaryInformation** e **UserDefined.** Questa sezione viene visualizzata nell'interfaccia [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) come set di proprietà separato, con il seguente FMTID (disponibile come **FMTID \_ UserDefinedProperties**): **D5CDD505-2E9C-101B-9397-08002B2CF9AE**.

Questi due set di proprietà sono gli unici per i quali un singolo flusso può contenere più set di proprietà. Il fatto che questi due set di proprietà siano in un singolo flusso influisce sul comportamento **dell'interfaccia IPropertySetStorage.** Per altre informazioni, vedere [**IPropertySetStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)

La tabella seguente elenca le proprietà aggiunte al set **di proprietà DocumentSummaryInformation** e **UserDefined.** Come nel set **di proprietà SummaryInformation,** i nomi non vengono in genere archiviati nel set di proprietà, ma vengono dedotto dall'identificatore della proprietà.



| Nome proprietà      | Identificatore proprietà     | Valore dell'identificatore di proprietà | Tipo VARIANT                      |
|--------------------|-------------------------|---------------------------|-----------------------------------|
| Category           | **CATEGORIA \_ PIDDSI**    | 0x00000002                | **VT \_ LPSTR**                     |
| PresentationTarget | **PIDDSI \_ PRESFORMAT**  | 0x00000003                | **VT \_ LPSTR**                     |
| Byte              | **PIDDSI \_ BYTECOUNT**   | 0x00000004                | **VT \_ I4**                        |
| Linee              | **CONTEGGIO RIGHE PIDDSI \_**   | 0x00000005                | **VT \_ I4**                        |
| Paragrafi         | **PIDDSI \_ FESTUNT**    | 0x00000006                | **VT \_ I4**                        |
| Diapositive             | **PIDDSI \_ SLIDECOUNT**  | 0x00000007                | **VT \_ I4**                        |
| Note              | **PIDDSI \_ NOTECOUNT**   | 0x00000008                | **VT \_ I4**                        |
| HiddenSlides       | **PIDDSI \_ HIDDENCOUNT** | 0x00000009                | **VT \_ I4**                        |
| MMClips            | **PIDDSI \_ MMCLIPCOUNT** | 0x0000000a                | **VT \_ I4**                        |
| ScaleCrop          | **SCALA PIDDSI \_**       | 0x0000000B                | **VT \_ BOOL**                      |
| HeadingPairs       | **INTESTAZIONE \_ PIDDSIPAIR** | 0x0000000C                | **VT \_ VARIANT** \| **VT \_ VECTOR** |
| TitlesofParts      | **PIDDSI \_ DOCPARTS**    | 0x0000000D                | **VT \_ VECTOR** \| **VT \_ LPSTR**   |
| Manager            | **GESTIONE PIDDSI \_**     | 0x0000000E                | **VT \_ LPSTR**                     |
| Company            | **SOCIETÀ PIDDSI \_**     | 0x0000000F                | **VT \_ LPSTR**                     |
| LinksUpToDate      | **COLLEGAMENTI \_ PIDDSIDIRTY**  | 0x00000010                | **VT \_ BOOL**                      |



 

Queste proprietà hanno gli usi seguenti:

<dl> <dt>

<span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoria
</dt> <dd>

Stringa di testo digitata dall'utente che indica la categoria a cui appartiene il file (promemoria, proposta e così via). È utile per trovare file dello stesso tipo.

</dd> <dt>

<span id="PresentationTarget"></span><span id="presentationtarget"></span><span id="PRESENTATIONTARGET"></span>PresentationTarget
</dt> <dd>

Formato di destinazione per la presentazione (35 mm, stampante, video e così via).

</dd> <dt>

<span id="Bytes"></span><span id="bytes"></span><span id="BYTES"></span>Byte
</dt> <dd>

Numero di byte.

</dd> <dt>

<span id="Lines"></span><span id="lines"></span><span id="LINES"></span>Linee
</dt> <dd>

Numero di righe.

</dd> <dt>

<span id="Paragraphs"></span><span id="paragraphs"></span><span id="PARAGRAPHS"></span>Paragrafi
</dt> <dd>

Numero di paragrafi.

</dd> <dt>

<span id="Slides"></span><span id="slides"></span><span id="SLIDES"></span>Diapositive
</dt> <dd>

Numero di diapositive.

</dd> <dt>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>Note
</dt> <dd>

Numero di pagine che contengono note.

</dd> <dt>

<span id="HiddenSlides"></span><span id="hiddenslides"></span><span id="HIDDENSLIDES"></span>HiddenSlides
</dt> <dd>

Numero di diapositive nascoste.

</dd> <dt>

<span id="MMClips"></span><span id="mmclips"></span><span id="MMCLIPS"></span>MMClips
</dt> <dd>

Numero di clip audio o video.

</dd> <dt>

<span id="ScaleCrop"></span><span id="scalecrop"></span><span id="SCALECROP"></span>ScaleCrop
</dt> <dd>

Impostare su True (-1) quando si desidera ridimensionare l'anteprima. Se non è impostato, è necessario ritagliare.

</dd> <dt>

<span id="HeadingPairs"></span><span id="headingpairs"></span><span id="HEADINGPAIRS"></span>HeadingPairs
</dt> <dd>

Proprietà usata internamente che indica il raggruppamento di parti del documento diverse e il numero di elementi in ogni gruppo. I titoli delle parti del documento vengono archiviati nella **proprietà TitlesofParts.** La **proprietà HeadingPairs** viene archiviata come vettore di varianti, in coppie ripetute di valori **\_ VT LPSTR** (o **VT \_ LPWSTR)** e **VT \_ I4.** Il **valore \_ VT LPSTR** rappresenta un nome di intestazione e il valore **VT \_ I4** indica il conteggio delle parti del documento sotto tale intestazione.

</dd> <dt>

<span id="TitlesofParts"></span><span id="titlesofparts"></span><span id="TITLESOFPARTS"></span>TitlesofParts
</dt> <dd>

Nomi delle parti del documento.

</dd> <dt>

<span id="Manager"></span><span id="manager"></span><span id="MANAGER"></span>Manager
</dt> <dd>

Responsabile del progetto.

</dd> <dt>

<span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Azienda
</dt> <dd>

Nome della società.

</dd> <dt>

<span id="LinksUpToDate"></span><span id="linksuptodate"></span><span id="LINKSUPTODATE"></span>LinksUpToDate
</dt> <dd>

Valore booleano per indicare se i collegamenti personalizzati sono ostacolati da un rumore eccessivo, per tutte le applicazioni.

> [!Note]  
> Come descritto nella versione 12.3. Formato serializzato per i set di proprietà della specifica di progettazione OLE 2.0, gli elementi vettoriali nelle proprietà **HeadingPairs** e **TitlesofParts** devono essere allineati sui limiti a 32 bit all'interno del set di proprietà. Tuttavia, nei set **di proprietà DocumentSummaryInformation** e **UserDefined,** quando la tabella codici del set di proprietà non è Unicode, questi elementi devono essere imballati.

 

</dd> </dl>

Il **set di proprietà UserDefined** può essere usato per contenere qualsiasi proprietà. In genere, viene usato per archiviare le proprietà denominate create da un utente.

 

 




