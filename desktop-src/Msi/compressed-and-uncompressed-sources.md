---
description: Gli autori di pacchetti possono ridurre le dimensioni dei pacchetti di installazione comprimendo i file di origine e includendoli nei file cab. L'immagine del file di origine può essere compressa, non compressa o una combinazione di entrambi i tipi.
ms.assetid: e84c52ca-a1c4-4c81-9c24-31ea435054db
title: Origini compresse e non compresse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca7d35a5723261ab1c62866d185a8402a9607600cad906c2fb66ddc5dc85ac08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144452"
---
# <a name="compressed-and-uncompressed-sources"></a>Origini compresse e non compresse

Gli autori di pacchetti possono ridurre le dimensioni dei pacchetti di installazione comprimendo i file di origine e includendoli nei [file cab](cabinet-files.md). L'immagine del file di origine può essere compressa, non compressa o una combinazione di entrambi i tipi.

<dl> <dt>

<span id="_____Compressed_Sources"></span><span id="_____compressed_sources"></span><span id="_____COMPRESSED_SOURCES"></span> Origini compresse
</dt> <dd>

Un'origine costituita interamente da file compressi deve includere il bit del flag compresso nella [**proprietà Riepilogo conteggio**](word-count-summary.md) parole. I file di origine compressi devono essere archiviati in file CAB che si trovano in un flusso di dati all'interno del file .msi o in un file cab separato che si trova nella radice dell'albero di origine. Tutti gli archivi nell'origine devono essere elencati nella [tabella Media](media-table.md).

</dd> <dt>

<span id="Uncompressed_Sources"></span><span id="uncompressed_sources"></span><span id="UNCOMPRESSED_SOURCES"></span>Origini non compresse
</dt> <dd>

Un'origine costituita interamente da file di origine non compressi deve omettere il bit del flag compresso dalla [**proprietà Riepilogo conteggio**](word-count-summary.md) parole. Tutti i file non compressi nell'origine devono esistere nell'albero di origine specificato dalla [tabella Directory](directory-table.md).

</dd> <dt>

<span id="Mixed_Sources_____"></span><span id="mixed_sources_____"></span><span id="MIXED_SOURCES_____"></span>Origini miste 
</dt> <dd>

Per combinare file di origine compressi e non compressi nello stesso pacchetto, eseguire l'override del valore predefinito della proprietà [**Riepilogo**](word-count-summary.md) conteggio parole impostando i flag di bit msidbFileAttributesCompressed o msidbFileAttributesNoncompressed in determinati file. Questi flag di bit vengono impostati nella colonna Attributi della tabella [File](file-table.md) se lo stato di compressione del file non corrisponde all'impostazione predefinita specificata dalla [**proprietà Riepilogo**](word-count-summary.md) conteggio parole.

Ad esempio, se per la [**proprietà Riepilogo conteggio**](word-count-summary.md) parole è impostato il bit del flag compresso, tutti i file vengono considerati compressi in un file cab. Tutti i file non compressi nell'origine devono includere msidbFileAttributesNoncompressed nella colonna Attributi della [tabella File](file-table.md). I file non compressi devono trovarsi nella radice dell'albero di origine.

Se per la proprietà [**Riepilogo**](word-count-summary.md) conteggio parole è impostato il flag non compresso, i file vengono considerati non compressi per impostazione predefinita e tutti i file compressi devono includere msidbFileAttributesCompressed nella colonna Attributi della tabella File. Tutti i file compressi devono essere archiviati in file CAB che si trovano in un flusso di dati all'interno del file .msi o in un file CAB separato che si trova nella radice dell'albero di origine.

Per altre informazioni, vedere [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).

</dd> </dl>

 

 



