---
description: Una famiglia di immagini è un gruppo di una o più immagini aggiornate di un prodotto aggiornate alla versione più recente.
ms.assetid: 06a77b35-b593-47e6-9083-46a6b65b7481
title: Tabella ImageFamilies (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ece99e3c42626eb2155f16f2198703dc31b682
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966973"
---
# <a name="imagefamilies-table-patchwizdll"></a>Tabella ImageFamilies (Patchwiz.dll)

Una famiglia di immagini è un gruppo di una o più immagini aggiornate di un prodotto aggiornate alla versione più recente. Ogni immagine aggiornata può appartenere a un solo gruppo. Le immagini aggiornate che appartengono a una famiglia di immagini condividono uno o più file. Ogni famiglia di immagini ha il proprio file CAB nel file con estensione msp contenente le patch binarie e i nuovi file necessari per aggiornare le differenze tra i file di destinazione e quelli aggiornati. Il file CAB non replica le patch binarie e i nuovi file usati dai file condivisi.

Una tabella ImageFamilies contenente almeno un record è obbligatoria in ogni database di creazione della patch (file con estensione PCP). Questa tabella viene utilizzata dalla funzione [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .

La tabella ImageFamilies contiene le informazioni relative all'applicazione di patch che devono essere aggiunte alla [tabella media](media-table.md). Una patch aggiunge una voce alla tabella media. Ogni record delle tabelle ImageFamilies fa riferimento a un gruppo di immagini di prodotto correlate che sono state aggiornate alla versione più recente del prodotto.

La tabella ImageFamilies include le colonne seguenti. Se la patch viene applicata con Windows Installer e Patchwiz.dll versione 2,0, è possibile usare un valore null nelle colonne MediaSrcPropName, MediaDiskId e FileSequenceStart.



| Colonna            | Tipo    | Chiave | Nullable |
|-------------------|---------|-----|----------|
| Famiglia            | text    | S   | N        |
| MediaSrcPropName  | text    |     | S        |
| MediaDiskId       | numero intero |     | S        |
| FileSequenceStart | numero intero |     | S        |
| DiskPrompt        | text    |     | S        |
| VolumeLabel       | text    |     | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Famiglia
</dt> <dd>

Il valore immesso in questo campo è un identificatore per un gruppo di immagini di prodotto correlate aggiornate alla versione più recente del prodotto. Limitato a un totale di 8 caratteri alfanumerici o caratteri di sottolineatura. Il programma di installazione incorpora un flusso CAB nel file di patch Windows Installer (file con estensione msp) per ogni famiglia nella tabella. Il cabinet contiene le patch binarie e i nuovi file necessari per aggiornare un'immagine di destinazione in un'immagine aggiornata del prodotto. Il programma di installazione prefissa il nome della famiglia con PCW \_ CAB \_ per generare il nome del flusso del file CAB inserito nel campo CAB della nuova voce della [tabella multimediale](media-table.md) .

</dd> <dt>

<span id="MediaSrcPropName"></span><span id="mediasrcpropname"></span><span id="MEDIASRCPROPNAME"></span>MediaSrcPropName
</dt> <dd>

Valore immesso nel campo di origine della nuova voce della [tabella multimediale](media-table.md) dell'immagine aggiornata. Questo campo può essere null solo se si usa la versione 2,0 di Patchwiz.dll e se MinimumRequiredMsiVersion nella [tabella Properties (Patchwiz.dll)](properties-table-patchwiz-dll-.md) è impostato su 200.

</dd> <dt>

<span id="MediaDiskId"></span><span id="mediadiskid"></span><span id="MEDIADISKID"></span>MediaDiskId
</dt> <dd>

Il programma di installazione immette questo valore nel campo DiskID del nuovo record della [tabella dei supporti](media-table.md) . Il valore DiskID deve essere maggiore di qualsiasi DiskID corrente nel pacchetto di destinazione. Il limite per MediaDiskId è 32767. Questo campo può essere null solo se si usa la versione 2,0 di Patchwiz.dll e se MinimumRequiredMsiVersion nella [tabella Properties (Patchwiz.dll)](properties-table-patchwiz-dll-.md) è impostato su 200.

</dd> <dt>

<span id="FileSequenceStart"></span><span id="filesequencestart"></span><span id="FILESEQUENCESTART"></span>FileSequenceStart
</dt> <dd>

Questo campo è il numero di sequenza per il file di avvio. Questo stesso numero di sequenza del file non deve esistere in due patch per lo stesso prodotto. Per garantire questo problema, il valore in questo campo deve essere maggiore di tutti i numeri di sequenza utilizzati nelle patch precedenti o nel pacchetto di installazione originale. Il numero di sequenza maggiore in una patch può essere determinato aggiungendo il numero totale di voci nel file CAB patch al numero FileSequenceStart per la patch. Un modo per determinare questo problema consiste nell'esaminare il file con estensione DDF generato da [Patchwiz.dll](patchwiz-dll.md) durante la creazione della patch. Il limite per FileSequenceStart è 32767. Questo campo può essere null solo se si usa la versione 2,0 di Patchwiz.dll e se MinimumRequiredMsiVersion nella [tabella Properties (Patchwiz.dll)](properties-table-patchwiz-dll-.md) è impostato su 200.

</dd> <dt>

<span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt
</dt> <dd>

Il programma di installazione immette questo valore nel campo DiskPrompt del nuovo record della [tabella dei supporti](media-table.md) .

</dd> <dt>

<span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel
</dt> <dd>

Il programma di installazione immette questo valore nel campo VolumeLabel del nuovo record multimediale.

</dd> </dl>

## <a name="remarks"></a>Commenti

La patch aggiunge il nome del file CAB nel file con estensione msp al campo cabinet del nuovo record aggiunto alla [tabella media](media-table.md). Poiché si tratta di un cabinet incorporato, il nome è preceduto da un \# carattere "". La patch aggiunge una proprietà al campo di origine del nuovo record nella tabella media. Due patch non possono avere la stessa proprietà Source.

I file condivisi nella famiglia di immagini devono avere la stessa chiave della tabella file in ogni immagine aggiornata della famiglia. Tutte le chiavi della tabella file condivise tra le immagini aggiornate devono rappresentare lo stesso file e devono essere identiche in tutte le immagini aggiornate. La chiave della tabella file è il valore immesso nella colonna file della [tabella file](file-table.md).

Il limite per MediaDiskId e FileSequenceStart è 32767. Per aumentare questo limite esportare la tabella ImageFamilies in un file con estensione IDT con [Msidb.exe](msidb-exe.md) e modificare il tipo di colonna da i2 a I4 o da i2 a I4, quindi importare di nuovo il file con estensione IDT nel database. PCP. Non è possibile creare trasformazioni e patch tra due pacchetti con tipi di colonne diversi.

 

 



