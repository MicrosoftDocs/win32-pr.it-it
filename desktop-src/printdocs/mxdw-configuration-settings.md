---
description: Microsoft XPS Document Writer (MXDW) consente agli utenti di creare file di documenti XPS stampando da qualsiasi applicazione Windows.
ms.assetid: 1fa50337-2df7-48d3-a179-0ca5ae3dfda3
title: Impostazioni di configurazione di MXDW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4026a99baa33ec50bc3ad129ef6610a428f83ab
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320965"
---
# <a name="mxdw-configuration-settings"></a><span data-ttu-id="47202-103">Impostazioni di configurazione di MXDW</span><span class="sxs-lookup"><span data-stu-id="47202-103">MXDW Configuration Settings</span></span>

<span data-ttu-id="47202-104">Microsoft XPS Document Writer (MXDW) consente agli utenti di creare file di documenti XPS stampando da qualsiasi applicazione Windows.</span><span class="sxs-lookup"><span data-stu-id="47202-104">The Microsoft XPS Document Writer (MXDW) enables users to create XPS document files by printing from any Windows application.</span></span> <span data-ttu-id="47202-105">Gli sviluppatori di applicazioni possono controllare le seguenti impostazioni di output di MXDW utilizzando le parti PrintTicket e PrintCapabilities dello [schema di stampa](./printschema.md).</span><span class="sxs-lookup"><span data-stu-id="47202-105">Applications developers can control the following output settings of the MXDW using the PrintTicket and PrintCapabilities parts of the [Print Schema](./printschema.md).</span></span>

## <a name="jobinterleaving"></a><span data-ttu-id="47202-106">JobInterleaving</span><span class="sxs-lookup"><span data-stu-id="47202-106">JobInterleaving</span></span>

<span data-ttu-id="47202-107">L'impostazione JobInterleaving controlla l'ordine di interfoliazione del contenuto per i documenti XPS.</span><span class="sxs-lookup"><span data-stu-id="47202-107">The JobInterleaving setting controls the content interleaving order for the XPS Documents.</span></span> <span data-ttu-id="47202-108">Per informazioni sull'interfoliazione dei processi, vedere la [specifica del documento XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span><span class="sxs-lookup"><span data-stu-id="47202-108">For information about job interleaving, see the [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span></span> <span data-ttu-id="47202-109">MXDW supporta le due opzioni seguenti per questa impostazione:</span><span class="sxs-lookup"><span data-stu-id="47202-109">MXDW supports the following two options for this setting:</span></span>

-   <span data-ttu-id="47202-110">**Off** : questa opzione Disabilita l'interfoliazione in modo che tutti i dati per ogni elemento contenuto nel documento siano contigui, migliorando così l'efficienza dell'accesso casuale.</span><span class="sxs-lookup"><span data-stu-id="47202-110">**Off** - This option disables interleaving so that all data for each content element in the document is contiguous, which improves the efficiency of random access.</span></span> <span data-ttu-id="47202-111">Questa opzione è consigliata per la visualizzazione di un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="47202-111">This option is best for viewing an XPS document.</span></span>
-   <span data-ttu-id="47202-112">**On** : questa opzione consente l'interfoliazione in modo che i dati per ogni elemento di contenuto vengano suddivisi e riordinati per un'elaborazione sequenziale più efficiente.</span><span class="sxs-lookup"><span data-stu-id="47202-112">**On** - This option enables interleaving so that data for each content element is broken up and reordered for more efficient sequential processing.</span></span> <span data-ttu-id="47202-113">Questa opzione è consigliata per il download e la stampa Web.</span><span class="sxs-lookup"><span data-stu-id="47202-113">This option is best for web download and printing.</span></span>

<span data-ttu-id="47202-114">Nell'esempio seguente viene riportato un esempio del codice XML PrintCapabilities che include l'impostazione JobInterleaving.</span><span class="sxs-lookup"><span data-stu-id="47202-114">The following example is an example of the PrintCapabilities XML that includes the JobInterleaving setting.</span></span>


```XML
<psf:Feature name="ns0000:JobInterleaving">
   <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value> 
   </psf:Property>
   <psf:Property name="psk:DisplayName">
      <psf:Value xsi:type="xsd:string">Interleaving</psf:Value> 
   </psf:Property>
   <psf:Option name="ns0000:OFF" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">Off - Best for viewing</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:ON" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">On - Best for the web/printing</psf:Value> 
      </psf:Property>
   </psf:Option>
</psf:Feature>
```



<span data-ttu-id="47202-115">Il codice XML PrintTicket è simile, ad eccezione del fatto che specifica una particolare opzione.</span><span class="sxs-lookup"><span data-stu-id="47202-115">The PrintTicket XML is similar, except that it specifies a particular option.</span></span> <span data-ttu-id="47202-116">Per informazioni dettagliate, vedere lo [schema di stampa](./printschema.md) .</span><span class="sxs-lookup"><span data-stu-id="47202-116">See the [Print Schema](./printschema.md) for details.</span></span>

<span data-ttu-id="47202-117">Poiché JobInterleaving non è una delle [parole chiave pubbliche dello schema di stampa](./print-schema-public-keywords.md), è necessario includere una dichiarazione dello spazio dei nomi (in questo caso "ns0000" nel tag **PrintCapabilities** (o **PrintTicket**) all'inizio del documento PrintCapabilities (o PrintTicket), come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="47202-117">Since JobInterleaving is not one of the [Print Schema Public Keywords](./print-schema-public-keywords.md), you must include a declaration of the namespace (in this case "ns0000" in the **PrintCapabilities** (or **PrintTicket**) tag at the beginning of the PrintCapabilities (or PrintTicket) document, as shown in the following example:</span></span>


```XML
<psf:PrintCapabilities 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="jobimagetype"></a><span data-ttu-id="47202-118">JobImageType</span><span class="sxs-lookup"><span data-stu-id="47202-118">JobImageType</span></span>

<span data-ttu-id="47202-119">JobImageType controlla il formato di output dei formati bitmap incorporati.</span><span class="sxs-lookup"><span data-stu-id="47202-119">JobImageType controls the output format of embedded bitmap formats.</span></span> <span data-ttu-id="47202-120">MXDW supporta le quattro opzioni seguenti per questa impostazione:</span><span class="sxs-lookup"><span data-stu-id="47202-120">MXDW supports the following four options for this setting:</span></span>

-   <span data-ttu-id="47202-121">**JPEGHigh** : questa opzione specifica l'immagine JPEG con un livello elevato di compressione.</span><span class="sxs-lookup"><span data-stu-id="47202-121">**JPEGHigh** - This option specifies the JPEG image with a high level of compression.</span></span> <span data-ttu-id="47202-122">Questa opzione produce le dimensioni del file più piccole, ma la qualità dell'immagine più bassa.</span><span class="sxs-lookup"><span data-stu-id="47202-122">This option produces the smallest file size, but the lowest image quality.</span></span>
-   <span data-ttu-id="47202-123">**JPEGMed** : questa opzione specifica l'immagine JPEG con un livello di compressione medio.</span><span class="sxs-lookup"><span data-stu-id="47202-123">**JPEGMed** - This option specifies the JPEG image with a medium level of compression.</span></span> <span data-ttu-id="47202-124">Questa opzione offre il migliore equilibrio tra dimensioni del file e qualità dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="47202-124">This option provides the best balance of file size and image quality.</span></span>
-   <span data-ttu-id="47202-125">**JPEGLow** : questa opzione specifica l'immagine JPEG con un basso livello di compressione.</span><span class="sxs-lookup"><span data-stu-id="47202-125">**JPEGLow** - This option specifies the JPEG image with a low level of compression.</span></span> <span data-ttu-id="47202-126">Questa opzione produce una riduzione minima delle dimensioni dei file e della qualità dell'immagine elevata.</span><span class="sxs-lookup"><span data-stu-id="47202-126">This option produces the least reduction in file size and high image quality.</span></span>
-   <span data-ttu-id="47202-127">**Png** : questa opzione specifica il formato dell'immagine PNG con compressione senza perdita di perdite.</span><span class="sxs-lookup"><span data-stu-id="47202-127">**PNG** - This option specifies the PNG image format with lossless compression.</span></span> <span data-ttu-id="47202-128">Questa opzione produce le dimensioni massime del file e la qualità dell'immagine più elevata.</span><span class="sxs-lookup"><span data-stu-id="47202-128">This option produces the largest file size and the highest image quality.</span></span>

<span data-ttu-id="47202-129">Di seguito è riportato il codice XML PrintCapabilities dell'impostazione JobImageType:</span><span class="sxs-lookup"><span data-stu-id="47202-129">The PrintCapabilities XML of the JobImageType setting appears below:</span></span>


```XML
<psf:Feature name="ns0000:JobImageType">
   <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value> 
   </psf:Property>
   <psf:Property name="psk:DisplayName">
      <psf:Value xsi:type="xsd:string">Images</psf:Value> 
   </psf:Property>
   <psf:Option name="ns0000:JPEGHigh" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">JPG - Maximum compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:JPEGMed" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
        <psf:Value xsi:type="xsd:string">JPG - Medium compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:JPEGLow" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">JPG - Minimum compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:PNG" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">PNG - Lossless compression</psf:Value> 
      </psf:Property>
   </psf:Option>
</psf:Feature>
```



<span data-ttu-id="47202-130">Il codice XML PrintTicket è simile, ad eccezione del fatto che specifica una particolare opzione.</span><span class="sxs-lookup"><span data-stu-id="47202-130">The PrintTicket XML is similar, except that it specifies a particular option.</span></span> <span data-ttu-id="47202-131">Per informazioni dettagliate, vedere lo [schema di stampa](./printschema.md) .</span><span class="sxs-lookup"><span data-stu-id="47202-131">See the [Print Schema](./printschema.md) for details.</span></span>

<span data-ttu-id="47202-132">Poiché JobImageType non è una delle [parole chiave pubbliche dello schema di stampa](./print-schema-public-keywords.md), è necessario includere una dichiarazione dello spazio dei nomi (in questo caso "ns0000" nel tag **PrintCapabilities** (o **PrintTicket**) all'inizio del documento PrintCapabilities (o PrintTicket), come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="47202-132">Since JobImageType is not one of the [Print Schema Public Keywords](./print-schema-public-keywords.md), you must include a declaration of the namespace (in this case "ns0000" in the **PrintCapabilities** (or **PrintTicket**) tag at the beginning of the PrintCapabilities (or PrintTicket) document, as shown in the following example:</span></span>


```XML
<psf:PrintTicket 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="related-topics"></a><span data-ttu-id="47202-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="47202-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47202-134">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="47202-134">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[<span data-ttu-id="47202-135">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="47202-135">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[<span data-ttu-id="47202-136">Stampa schema</span><span class="sxs-lookup"><span data-stu-id="47202-136">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="47202-137">Specifiche XPS e download delle licenze</span><span class="sxs-lookup"><span data-stu-id="47202-137">XPS Specification and License Downloads</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
