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
# <a name="compressed-and-uncompressed-sources"></a><span data-ttu-id="0ad29-104">Origini compresse e non compresse</span><span class="sxs-lookup"><span data-stu-id="0ad29-104">Compressed and Uncompressed Sources</span></span>

<span data-ttu-id="0ad29-105">Gli autori di pacchetti possono ridurre le dimensioni dei pacchetti di installazione comprimendo i file di origine e inserendoli nei [file CAB](cabinet-files.md).</span><span class="sxs-lookup"><span data-stu-id="0ad29-105">Package authors can reduce the size of their installation packages by compressing the source files and including them in [cabinet files](cabinet-files.md).</span></span> <span data-ttu-id="0ad29-106">L'immagine del file di origine può essere compressa, non compressa o una combinazione di entrambi i tipi.</span><span class="sxs-lookup"><span data-stu-id="0ad29-106">The source file image can be compressed, uncompressed, or a mixture of both types.</span></span>

<dl> <dt>

<span data-ttu-id="0ad29-107"><span id="_____Compressed_Sources"></span><span id="_____compressed_sources"></span><span id="_____COMPRESSED_SOURCES"></span> Origini compresse</span><span class="sxs-lookup"><span data-stu-id="0ad29-107"><span id="_____Compressed_Sources"></span><span id="_____compressed_sources"></span><span id="_____COMPRESSED_SOURCES"></span> Compressed Sources</span></span>
</dt> <dd>

<span data-ttu-id="0ad29-108">Un'origine costituita interamente da file compressi deve includere il bit del flag compresso nella proprietà [**riepilogo Conteggio parole**](word-count-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="0ad29-108">A source consisting entirely of compressed files should include the compressed flag bit in the [**Word Count Summary**](word-count-summary.md) Property.</span></span> <span data-ttu-id="0ad29-109">I file di origine compressi devono essere archiviati in file CAB che si trovano in un flusso di dati all'interno del file con estensione msi o in un file CAB separato che si trova nella radice dell'albero di origine.</span><span class="sxs-lookup"><span data-stu-id="0ad29-109">The compressed source files must be stored in cabinet files located in a data stream inside the .msi file or in a separate cabinet file located at the root of the source tree.</span></span> <span data-ttu-id="0ad29-110">Tutti i cabinet nell'origine devono essere elencati nella [tabella dei supporti](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="0ad29-110">All of the cabinets in the source must be listed in the [Media table](media-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ad29-111"><span id="Uncompressed_Sources"></span><span id="uncompressed_sources"></span><span id="UNCOMPRESSED_SOURCES"></span>Origini non compresse</span><span class="sxs-lookup"><span data-stu-id="0ad29-111"><span id="Uncompressed_Sources"></span><span id="uncompressed_sources"></span><span id="UNCOMPRESSED_SOURCES"></span>Uncompressed Sources</span></span>
</dt> <dd>

<span data-ttu-id="0ad29-112">Un'origine costituita interamente da file di origine non compressi deve omettere il bit del flag compresso dalla proprietà [**riepilogo Conteggio parole**](word-count-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="0ad29-112">A source consisting entirely of uncompressed source files should omit the compressed flag bit from the [**Word Count Summary**](word-count-summary.md) Property.</span></span> <span data-ttu-id="0ad29-113">Tutti i file non compressi nell'origine devono esistere nell'albero di origine specificato dalla [tabella di directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="0ad29-113">All of the uncompressed files in the source must exist in the source tree specified by the [Directory table](directory-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ad29-114"><span id="Mixed_Sources_____"></span><span id="mixed_sources_____"></span><span id="MIXED_SOURCES_____"></span>Origini miste</span><span class="sxs-lookup"><span data-stu-id="0ad29-114"><span id="Mixed_Sources_____"></span><span id="mixed_sources_____"></span><span id="MIXED_SOURCES_____"></span>Mixed Sources</span></span> 
</dt> <dd>

<span data-ttu-id="0ad29-115">Per combinare i file di origine compressi e non compressi nello stesso pacchetto, eseguire l'override del valore predefinito della proprietà [**riepilogo Conteggio parole**](word-count-summary.md) impostando i flag di bit MsidbFileAttributesCompressed o msidbFileAttributesNoncompressed su file specifici.</span><span class="sxs-lookup"><span data-stu-id="0ad29-115">To mix compressed and uncompressed source files in the same package, override the [**Word Count Summary**](word-count-summary.md) property default by setting the msidbFileAttributesCompressed or msidbFileAttributesNoncompressed bit flags on particular files.</span></span> <span data-ttu-id="0ad29-116">Questi flag di bit vengono impostati nella colonna attributi della [tabella file](file-table.md) se lo stato di compressione del file non corrisponde al valore predefinito specificato dalla proprietà [**riepilogo Conteggio parole**](word-count-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="0ad29-116">These bit flags are set in the Attributes column of the [File table](file-table.md) if the compression state of the file does not match the default specified by the [**Word Count Summary**](word-count-summary.md) property.</span></span>

<span data-ttu-id="0ad29-117">Se, ad esempio, per la proprietà di [**Riepilogo di Word Count**](word-count-summary.md) è impostato il bit del flag compresso, tutti i file vengono considerati compressi in un file CAB.</span><span class="sxs-lookup"><span data-stu-id="0ad29-117">For example, if the [**Word Count Summary**](word-count-summary.md) property has the compressed flag bit set, all files are treated as compressed into a cabinet.</span></span> <span data-ttu-id="0ad29-118">Tutti i file non compressi nell'origine devono includere msidbFileAttributesNoncompressed nella colonna attributi della [tabella file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="0ad29-118">Any uncompressed files in the source must include msidbFileAttributesNoncompressed in the Attributes column of the [File table](file-table.md).</span></span> <span data-ttu-id="0ad29-119">I file non compressi devono trovarsi nella radice dell'albero di origine.</span><span class="sxs-lookup"><span data-stu-id="0ad29-119">The uncompressed files must be located at the root of the source tree.</span></span>

<span data-ttu-id="0ad29-120">Se per la proprietà [**riepilogo Conteggio parole**](word-count-summary.md) è impostato il flag non compresso, i file vengono considerati come non compressi per impostazione predefinita e tutti i file compressi devono includere msidbFileAttributesCompressed nella colonna attributi della tabella file.</span><span class="sxs-lookup"><span data-stu-id="0ad29-120">If the [**Word Count Summary**](word-count-summary.md) property has the uncompressed flag set, files are treated as uncompressed by default and any compressed files must include msidbFileAttributesCompressed in the Attributes column of the File table.</span></span> <span data-ttu-id="0ad29-121">Tutti i file compressi devono essere archiviati in file CAB che si trovano in un flusso di dati all'interno del file con estensione msi o in un file CAB separato che si trova nella radice dell'albero di origine.</span><span class="sxs-lookup"><span data-stu-id="0ad29-121">All of the compressed files must be stored in cabinet files located in a data stream inside the .msi file or in a separate cabinet file located at the root of the source tree.</span></span>

<span data-ttu-id="0ad29-122">Per altre informazioni, vedere [uso di cabinet e origini compresse](using-cabinets-and-compressed-sources.md).</span><span class="sxs-lookup"><span data-stu-id="0ad29-122">For more information, see [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

</dd> </dl>

 

 



