---
description: In questo argomento viene descritta la struttura di un file di formato Advanced Systems (ASF).
ms.assetid: 4a817efa-5452-46bf-8921-2ba199c21949
title: Struttura di file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672067b5f933884326038a93b6d4538c68558856
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524673"
---
# <a name="asf-file-structure"></a><span data-ttu-id="5accf-103">Struttura di file ASF</span><span class="sxs-lookup"><span data-stu-id="5accf-103">ASF File Structure</span></span>

<span data-ttu-id="5accf-104">In questo argomento viene descritta la struttura di un file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="5accf-104">This topic describes the structure of an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="5accf-105">Per informazioni dettagliate sui file ASF, scaricare la [specifica ASF](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span><span class="sxs-lookup"><span data-stu-id="5accf-105">For detailed information about ASF files, download the [ASF Specification](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span></span> <span data-ttu-id="5accf-106">È inoltre possibile utilizzare lo strumento [Windows Media ASF Viewer 9 Series](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea) per visualizzare la struttura di un file ASF esistente.</span><span class="sxs-lookup"><span data-stu-id="5accf-106">You can also use the [Windows Media ASF Viewer 9 Series](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea) tool to see the structure of an existing ASF file.</span></span>

<span data-ttu-id="5accf-107">L'unità di base dell'organizzazione per i file ASF è denominata *oggetto*.</span><span class="sxs-lookup"><span data-stu-id="5accf-107">The base unit of organization for ASF files is called an *object*.</span></span> <span data-ttu-id="5accf-108">Un oggetto file ASF contiene i dati seguenti.</span><span class="sxs-lookup"><span data-stu-id="5accf-108">An ASF file object contains the following data.</span></span>



| <span data-ttu-id="5accf-109">Data</span><span class="sxs-lookup"><span data-stu-id="5accf-109">Data</span></span>                                                        | <span data-ttu-id="5accf-110">Dimensione</span><span class="sxs-lookup"><span data-stu-id="5accf-110">Size</span></span>     |
|-------------------------------------------------------------|----------|
| <span data-ttu-id="5accf-111">GUID che identifica l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5accf-111">A GUID that identifies the object.</span></span>                          | <span data-ttu-id="5accf-112">128 bit</span><span class="sxs-lookup"><span data-stu-id="5accf-112">128 bits</span></span> |
| <span data-ttu-id="5accf-113">Dimensione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5accf-113">The size of the object.</span></span>                                     | <span data-ttu-id="5accf-114">64 bit.</span><span class="sxs-lookup"><span data-stu-id="5accf-114">64-bits.</span></span> |
| <span data-ttu-id="5accf-115">Dati dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5accf-115">Object data.</span></span> <span data-ttu-id="5accf-116">I dati dell'oggetto possono contenere altri oggetti ASF.</span><span class="sxs-lookup"><span data-stu-id="5accf-116">The object data can contain other ASF objects.</span></span> | <span data-ttu-id="5accf-117">Variabile.</span><span class="sxs-lookup"><span data-stu-id="5accf-117">Varies.</span></span>  |



 

> [!Note]  
> <span data-ttu-id="5accf-118">Un oggetto file ASF è semplicemente un blocco di dati.</span><span class="sxs-lookup"><span data-stu-id="5accf-118">An ASF file object is simply a chunk of data.</span></span> <span data-ttu-id="5accf-119">Non si tratta di un oggetto nel senso della programmazione del computer.</span><span class="sxs-lookup"><span data-stu-id="5accf-119">It is not an object in the computer programming sense.</span></span>

 

<span data-ttu-id="5accf-120">Un file ASF contiene tre tipi di oggetti file di primo livello.</span><span class="sxs-lookup"><span data-stu-id="5accf-120">An ASF file contains three types of top-level file objects.</span></span>



| <span data-ttu-id="5accf-121">Oggetto file ASF</span><span class="sxs-lookup"><span data-stu-id="5accf-121">ASF File Object</span></span>                                                                                                                      | <span data-ttu-id="5accf-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5accf-122">Description</span></span>                                          |
|--------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5accf-123"><span id="_Header_Object"></span><span id="_header_object"></span><span id="_HEADER_OBJECT"></span> Oggetto Header</span><span class="sxs-lookup"><span data-stu-id="5accf-123"><span id="_Header_Object"></span><span id="_header_object"></span><span id="_HEADER_OBJECT"></span> Header Object</span></span><br/>         | <span data-ttu-id="5accf-124">Contiene informazioni sul file ASF.</span><span class="sxs-lookup"><span data-stu-id="5accf-124">Contains information about the ASF file.</span></span><br/>  |
| <span data-ttu-id="5accf-125"><span id="Data_Object"></span><span id="data_object"></span><span id="DATA_OBJECT"></span>Oggetto dati</span><span class="sxs-lookup"><span data-stu-id="5accf-125"><span id="Data_Object"></span><span id="data_object"></span><span id="DATA_OBJECT"></span>Data Object</span></span><br/>                     | <span data-ttu-id="5accf-126">Contiene pacchetti di dati multimediali.</span><span class="sxs-lookup"><span data-stu-id="5accf-126">Contains packets of media data.</span></span><br/>           |
| <span data-ttu-id="5accf-127"><span id="_Index_Object_s_"></span><span id="_index_object_s_"></span><span id="_INDEX_OBJECT_S_"></span> Oggetti indice</span><span class="sxs-lookup"><span data-stu-id="5accf-127"><span id="_Index_Object_s_"></span><span id="_index_object_s_"></span><span id="_INDEX_OBJECT_S_"></span> Index Object(s)</span></span><br/> | <span data-ttu-id="5accf-128">Contiene uno o più indici.</span><span class="sxs-lookup"><span data-stu-id="5accf-128">Contains one or more indexes.</span></span> <span data-ttu-id="5accf-129">Facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5accf-129">(Optional.)</span></span><br/> |



 

<span data-ttu-id="5accf-130">Nel diagramma seguente viene illustrata la struttura del file ASF.</span><span class="sxs-lookup"><span data-stu-id="5accf-130">The following diagram shows the ASF file structure.</span></span>

![diagramma che illustra la struttura dei file ASF, inclusi gli elementi all'interno dell'intestazione, dei dati e dell'indice](images/asf-components04.png)

<span data-ttu-id="5accf-132">Il diagramma non viene disegnato per la scalabilità. in genere l'oggetto dati comprende la maggior parte del file.</span><span class="sxs-lookup"><span data-stu-id="5accf-132">This diagram is not drawn to scale; typically the Data Object comprises most of the file.</span></span>

### <a name="header-object"></a><span data-ttu-id="5accf-133">Oggetto Header</span><span class="sxs-lookup"><span data-stu-id="5accf-133">Header Object</span></span>

<span data-ttu-id="5accf-134">L'oggetto Header è obbligatorio e viene visualizzato all'inizio di ogni file ASF.</span><span class="sxs-lookup"><span data-stu-id="5accf-134">The Header Object is mandatory and appears at the beginning of every ASF file.</span></span> <span data-ttu-id="5accf-135">Contiene attributi di file globali e informazioni sui flussi nel file ASF.</span><span class="sxs-lookup"><span data-stu-id="5accf-135">It contains global file attributes and information about the streams in the ASF file.</span></span> <span data-ttu-id="5accf-136">Queste informazioni vengono usate per interpretare e riprodurre i dati nel file.</span><span class="sxs-lookup"><span data-stu-id="5accf-136">This information is used to interpret and play the data in the file.</span></span>

<span data-ttu-id="5accf-137">L'oggetto header contiene diversi oggetti secondari madatory:</span><span class="sxs-lookup"><span data-stu-id="5accf-137">The Header Object contains several madatory sub-objects:</span></span>

-   <span data-ttu-id="5accf-138">L'oggetto proprietà file descrive gli attributi globali del file, ad esempio le dimensioni del file, la durata della riproduzione, il numero di pacchetti di dati, le dimensioni minime e massime del pacchetto e la velocità in bit massima.</span><span class="sxs-lookup"><span data-stu-id="5accf-138">The File Properties Object describes global attributes of the file, such as the file size, play duration, number of data packets, minimum and maximum packet size, and maximum bit rate.</span></span>
-   <span data-ttu-id="5accf-139">L'oggetto estensione dell'intestazione consente di aggiungere funzionalità aggiuntive a un file ASF mantenendo la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="5accf-139">The Header Extension Object enables additional functionality to be added to an ASF file while maintaining backward compatibility.</span></span>
-   <span data-ttu-id="5accf-140">L'oggetto proprietà del flusso descrive un flusso nel file.</span><span class="sxs-lookup"><span data-stu-id="5accf-140">The Stream Properties Object describes one stream in the file.</span></span> <span data-ttu-id="5accf-141">Un file ASF deve contenere almeno un flusso e pertanto almeno un oggetto proprietà del flusso.</span><span class="sxs-lookup"><span data-stu-id="5accf-141">An ASF file must contain at least one stream, and therefore at least one Stream Properties Object.</span></span>

<span data-ttu-id="5accf-142">L'oggetto Header può contenere informazioni facoltative aggiuntive, inclusi i metadati sul file (ad esempio titolo e autore), un elenco dei codec usati per codificare il file e le informazioni sulla protezione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="5accf-142">The Header Object can contain additional optional information, including metadata about the file (such as title and author), a list of the codecs used to encode the file, and content protection information.</span></span>

### <a name="data-object"></a><span data-ttu-id="5accf-143">Oggetto dati</span><span class="sxs-lookup"><span data-stu-id="5accf-143">Data Object</span></span>

<span data-ttu-id="5accf-144">L'oggetto dati ASF contiene tutti i dati multimediali per il file ASF.</span><span class="sxs-lookup"><span data-stu-id="5accf-144">The ASF Data Object contains all of the media data for the ASF file.</span></span> <span data-ttu-id="5accf-145">Questo oggetto è obbligatorio e deve seguire l'oggetto intestazione ASF.</span><span class="sxs-lookup"><span data-stu-id="5accf-145">This object is mandatory and must follow the ASF Header Object.</span></span>

<span data-ttu-id="5accf-146">L'oggetto dati è suddiviso in *pacchetti* di dati.</span><span class="sxs-lookup"><span data-stu-id="5accf-146">The Data Object is divided into data *packets*.</span></span> <span data-ttu-id="5accf-147">Ogni pacchetto contiene dati per uno o più flussi del file.</span><span class="sxs-lookup"><span data-stu-id="5accf-147">Each packet contains data for one or several streams in the file.</span></span> <span data-ttu-id="5accf-148">Un pacchetto di dati contiene un'intestazione del pacchetto di dati che fornisce informazioni sull'analisi dei pacchetti, seguite dai dati del payload, ovvero i dati effettivi dei supporti digitali.</span><span class="sxs-lookup"><span data-stu-id="5accf-148">A data packet contains a data packet header that provides packet parsing information, followed by the payload data the actual digital media data.</span></span> <span data-ttu-id="5accf-149">A tutti i pacchetti di dati è associato un tempo di presentazione e sono disposti nell'ordine in cui sono stati ricevuti.</span><span class="sxs-lookup"><span data-stu-id="5accf-149">All of the data packets have a presentation time associated with it and are arranged in the order received.</span></span>

<span data-ttu-id="5accf-150">Le informazioni sul contenuto dell'oggetto dati, ad esempio le dimensioni del pacchetto e il numero di pacchetti, vengono archiviate nell'oggetto intestazione.</span><span class="sxs-lookup"><span data-stu-id="5accf-150">Information about the contents of the Data Object, such as the packet size and packet count, is stored in the Header Object.</span></span>

### <a name="index-object"></a><span data-ttu-id="5accf-151">Oggetto index</span><span class="sxs-lookup"><span data-stu-id="5accf-151">Index Object</span></span>

<span data-ttu-id="5accf-152">L'oggetto index è facoltativo ed è l'ultimo oggetto nel file ASF.</span><span class="sxs-lookup"><span data-stu-id="5accf-152">The Index Object is optional and is the last object in the ASF file.</span></span> <span data-ttu-id="5accf-153">Un file ASF può contenere più di un oggetto index.</span><span class="sxs-lookup"><span data-stu-id="5accf-153">An ASF file can contain more than one Index Object.</span></span> <span data-ttu-id="5accf-154">L'oggetto index fornisce accesso casuale basato sul tempo nell'oggetto dati ASF.</span><span class="sxs-lookup"><span data-stu-id="5accf-154">The Index Object provides time-based random access into the ASF Data Object.</span></span>

<span data-ttu-id="5accf-155">Un oggetto indice semplice è un altro tipo di indice.</span><span class="sxs-lookup"><span data-stu-id="5accf-155">A Simple Index Object is another type of index.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5accf-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5accf-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5accf-157">Supporto ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5accf-157">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




