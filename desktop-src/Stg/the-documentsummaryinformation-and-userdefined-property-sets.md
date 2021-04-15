---
title: Set di proprietà DocumentSummaryInformation e UserDefined
description: Un set di proprietà DocumentSummaryInformation e UserDefined è un'estensione del set di proprietà informazioni di riepilogo. Entrambi i set di proprietà possono esistere simultaneamente.
ms.assetid: c6d4e2bc-f7f6-429d-aa91-432d833c69d1
keywords:
- DocumentSummaryInformation
- Set di Proprietà UserDefined
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411c6081ec098539baa2b26b6594d04216f5b455
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515721"
---
# <a name="the-documentsummaryinformation-and-userdefined-property-sets"></a>Set di proprietà DocumentSummaryInformation e UserDefined

Un set di proprietà **DocumentSummaryInformation** e **UserDefined** è un'estensione [del set di proprietà informazioni di riepilogo](the-summary-information-property-set.md). Entrambi i set di proprietà possono esistere simultaneamente.

Il nome del flusso che contiene il set di proprietà **DocumentSummaryInformation** è **" \\ 005DocumentSummaryInformation"**. L'identificatore di formato (FMTID) per il set di proprietà **DocumentSummaryInformation** è **D5CDD502-2E9C-101B-9397-08002B2CF9AE**.

La dichiarazione per questo valore è disponibile nei file di intestazione specificati come **fmtid \_ DocSummaryInformation**. Per ulteriori informazioni, vedere [nomi in IStorage](names-in-istorage.md), [il set di proprietà informazioni di riepilogo](the-summary-information-property-set.md), [**IPropertySetStorage:: create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) e [identificatori di formato](format-identifiers.md).

Questo flusso include anche una sezione separata per le proprietà personalizzate definite dall'utente, come nei set di proprietà **DocumentSummaryInformation** e **UserDefined** . Questa sezione viene visualizzata nell'interfaccia [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) come set di proprietà separato, con il fmtid seguente (disponibile come **fmtid \_ UserDefinedProperties**): **D5CDD505-2E9C-101B-9397-08002B2CF9AE**.

Questi due set di proprietà sono gli unici per i quali un singolo flusso può ospitare più set di proprietà. Il fatto che questi due set di proprietà si trovino in un singolo flusso influiscono sul comportamento dell'interfaccia **IPropertySetStorage** . Per ulteriori informazioni, vedere [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).

Nella tabella seguente sono elencate le proprietà aggiunte al set di proprietà **DocumentSummaryInformation** e **UserDefined** . Come nel set di proprietà **SummaryInformation** , i nomi non vengono in genere archiviati nel set di proprietà, ma vengono dedotti dall'identificatore della proprietà.



| Nome proprietà      | Identificatore proprietà     | Valore dell'identificatore di proprietà | Tipo VARIANT                      |
|--------------------|-------------------------|---------------------------|-----------------------------------|
| Category           | **\_categoria PIDDSI**    | 0x00000002                | **\_LPSTR VT**                     |
| DestinazionePresentazione | **\_PRESFORMAT PIDDSI**  | 0x00000003                | **\_LPSTR VT**                     |
| Byte              | **PIDDSI ( \_ GetByteCount)**   | 0x00000004                | **VT \_ I4**                        |
| Linee              | **\_LINECOUNT PIDDSI**   | 0x00000005                | **VT \_ I4**                        |
| Paragrafi         | **\_PARCOUNT PIDDSI**    | 0x00000006                | **VT \_ I4**                        |
| Diapositive             | **\_SLIDECOUNT PIDDSI**  | 0x00000007                | **VT \_ I4**                        |
| Note              | **\_NOTECOUNT PIDDSI**   | 0x00000008                | **VT \_ I4**                        |
| HiddenSlides       | **\_HIDDENCOUNT PIDDSI** | 0x00000009                | **VT \_ I4**                        |
| MMClips            | **\_MMCLIPCOUNT PIDDSI** | 0x0000000A                | **VT \_ I4**                        |
| ScaleCrop          | **\_scalabilità PIDDSI**       | 0x0000000B                | **\_bool VT**                      |
| HeadingPairs       | **\_HEADINGPAIR PIDDSI** | 0x0000000C                | **VT \_** \| **\_ vettore VT** Variant |
| TitlesofParts      | **\_DOCPARTS PIDDSI**    | 0x0000000D                | **VT \_** \| **\_ LPSTR Vector VT**   |
| Manager            | **\_gestione PIDDSI**     | 0x0000000E                | **\_LPSTR VT**                     |
| Company            | **\_società PIDDSI**     | 0x0000000F                | **\_LPSTR VT**                     |
| LinksUpToDate      | **\_LINKSDIRTY PIDDSI**  | 0x00000010                | **\_bool VT**                      |



 

Queste proprietà hanno i seguenti usi:

<dl> <dt>

<span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoria
</dt> <dd>

Stringa di testo digitata dall'utente che indica a quale categoria appartiene il file (promemoria, proposta e così via). È utile per trovare file dello stesso tipo.

</dd> <dt>

<span id="PresentationTarget"></span><span id="presentationtarget"></span><span id="PRESENTATIONTARGET"></span>DestinazionePresentazione
</dt> <dd>

Formato di destinazione per la presentazione (35mm, stampante, video e così via).

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

Impostare su true (-1) quando si vuole ridimensionare l'anteprima. Se non è impostato, si desidera il ritaglio.

</dd> <dt>

<span id="HeadingPairs"></span><span id="headingpairs"></span><span id="HEADINGPAIRS"></span>HeadingPairs
</dt> <dd>

Proprietà utilizzata internamente che indica il raggruppamento di diverse parti del documento e il numero di elementi in ogni gruppo. I titoli delle parti del documento vengono archiviati nella proprietà **TitlesofParts** . La proprietà **HeadingPairs** viene archiviata come vettore di varianti, in coppie ripetute di valori VT **\_ LPSTR** (o **VT \_ LPWSTR**) e **VT \_ I4** . Il valore **VT \_ LPSTR** rappresenta un nome di intestazione e il valore **VT \_ I4** indica il numero di parti del documento sotto tale intestazione.

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

Valore booleano che indica se i collegamenti personalizzati sono ostacolati da un rumore eccessivo, per tutte le applicazioni.

> [!Note]  
> Come descritto in 12,3. Formato serializzato per i set di proprietà della specifica di progettazione OLE 2,0, gli elementi Vector nelle proprietà **HeadingPairs** e **TitlesofParts** devono essere allineati nei limiti di 32 bit all'interno del set di proprietà. Tuttavia, nei set di proprietà **DocumentSummaryInformation** e **UserDefined** , quando la tabella codici della proprietà impostata non è Unicode, questi elementi devono essere compressi.

 

</dd> </dl>

Il set di proprietà **UserDefined** può essere utilizzato per contenere qualsiasi proprietà. Viene in genere usato per archiviare le proprietà denominate create da un utente.

 

 




