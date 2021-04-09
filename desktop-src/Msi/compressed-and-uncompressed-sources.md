---
description: Gli autori di pacchetti possono ridurre le dimensioni dei pacchetti di installazione comprimendo i file di origine e inserendoli nei file CAB. L'immagine del file di origine può essere compressa, non compressa o una combinazione di entrambi i tipi.
ms.assetid: e84c52ca-a1c4-4c81-9c24-31ea435054db
title: Origini compresse e non compresse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43dc706a73d52f1dac35c917bd6c178a543ab300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966928"
---
# <a name="compressed-and-uncompressed-sources"></a>Origini compresse e non compresse

Gli autori di pacchetti possono ridurre le dimensioni dei pacchetti di installazione comprimendo i file di origine e inserendoli nei [file CAB](cabinet-files.md). L'immagine del file di origine può essere compressa, non compressa o una combinazione di entrambi i tipi.

<dl> <dt>

<span id="_____Compressed_Sources"></span><span id="_____compressed_sources"></span><span id="_____COMPRESSED_SOURCES"></span> Origini compresse
</dt> <dd>

Un'origine costituita interamente da file compressi deve includere il bit del flag compresso nella proprietà [**riepilogo Conteggio parole**](word-count-summary.md) . I file di origine compressi devono essere archiviati in file CAB che si trovano in un flusso di dati all'interno del file con estensione msi o in un file CAB separato che si trova nella radice dell'albero di origine. Tutti i cabinet nell'origine devono essere elencati nella [tabella dei supporti](media-table.md).

</dd> <dt>

<span id="Uncompressed_Sources"></span><span id="uncompressed_sources"></span><span id="UNCOMPRESSED_SOURCES"></span>Origini non compresse
</dt> <dd>

Un'origine costituita interamente da file di origine non compressi deve omettere il bit del flag compresso dalla proprietà [**riepilogo Conteggio parole**](word-count-summary.md) . Tutti i file non compressi nell'origine devono esistere nell'albero di origine specificato dalla [tabella di directory](directory-table.md).

</dd> <dt>

<span id="Mixed_Sources_____"></span><span id="mixed_sources_____"></span><span id="MIXED_SOURCES_____"></span>Origini miste 
</dt> <dd>

Per combinare i file di origine compressi e non compressi nello stesso pacchetto, eseguire l'override del valore predefinito della proprietà [**riepilogo Conteggio parole**](word-count-summary.md) impostando i flag di bit MsidbFileAttributesCompressed o msidbFileAttributesNoncompressed su file specifici. Questi flag di bit vengono impostati nella colonna attributi della [tabella file](file-table.md) se lo stato di compressione del file non corrisponde al valore predefinito specificato dalla proprietà [**riepilogo Conteggio parole**](word-count-summary.md) .

Se, ad esempio, per la proprietà di [**Riepilogo di Word Count**](word-count-summary.md) è impostato il bit del flag compresso, tutti i file vengono considerati compressi in un file CAB. Tutti i file non compressi nell'origine devono includere msidbFileAttributesNoncompressed nella colonna attributi della [tabella file](file-table.md). I file non compressi devono trovarsi nella radice dell'albero di origine.

Se per la proprietà [**riepilogo Conteggio parole**](word-count-summary.md) è impostato il flag non compresso, i file vengono considerati come non compressi per impostazione predefinita e tutti i file compressi devono includere msidbFileAttributesCompressed nella colonna attributi della tabella file. Tutti i file compressi devono essere archiviati in file CAB che si trovano in un flusso di dati all'interno del file con estensione msi o in un file CAB separato che si trova nella radice dell'albero di origine.

Per altre informazioni, vedere [uso di cabinet e origini compresse](using-cabinets-and-compressed-sources.md).

</dd> </dl>

 

 



