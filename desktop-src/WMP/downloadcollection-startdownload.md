---
title: Metodo DownloadCollection. startDownload
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. Il metodo startDownload Accoda un download.
ms.assetid: 54cf91fe-cef9-4424-9f99-629e773eade1
keywords:
- metodo startDownload Windows Media Player
- metodo startDownload Windows Media Player, classe DownloadCollection
- Scaricacollection (classe) Windows Media Player, metodo startDownload
topic_type:
- apiref
api_name:
- DownloadCollection.startDownload
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3187ce00dda45f7e4660b4961c78af6db2af50e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331485"
---
# <a name="downloadcollectionstartdownload-method"></a><span data-ttu-id="e7131-108">Metodo DownloadCollection. startDownload</span><span class="sxs-lookup"><span data-stu-id="e7131-108">DownloadCollection.startDownload method</span></span>

> [!Note]  
> <span data-ttu-id="e7131-109">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="e7131-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="e7131-110">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e7131-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="e7131-111">Il metodo **startDownload** Accoda un download.</span><span class="sxs-lookup"><span data-stu-id="e7131-111">The **startDownload** method queues a download.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7131-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7131-112">Syntax</span></span>


```JScript
retVal = DownloadCollection.startDownload(
  sourceURL,
  type
)
```



## <a name="parameters"></a><span data-ttu-id="e7131-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7131-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7131-114">*sourceURL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7131-114">*sourceURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7131-115">**Stringa** che specifica l'URL del download.</span><span class="sxs-lookup"><span data-stu-id="e7131-115">**String** specifying the URL of the download.</span></span>

</dd> <dt>

<span data-ttu-id="e7131-116">*tipo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="e7131-116">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7131-117">**Stringa** che specifica il tipo di download.</span><span class="sxs-lookup"><span data-stu-id="e7131-117">**String** specifying the type of download.</span></span> <span data-ttu-id="e7131-118">Contiene uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e7131-118">Contains one of the following values.</span></span>



| <span data-ttu-id="e7131-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e7131-119">Value</span></span>      | <span data-ttu-id="e7131-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7131-120">Description</span></span>                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7131-121">background</span><span class="sxs-lookup"><span data-stu-id="e7131-121">background</span></span> | <span data-ttu-id="e7131-122">(Windows XP e versioni successive). Il download viene eseguito come processo in background, in quanto il tempo del processore diventa disponibile.</span><span class="sxs-lookup"><span data-stu-id="e7131-122">(Windows XP and later.) The download occurs as a background process as processor time becomes available.</span></span> <span data-ttu-id="e7131-123">Gli Stati di download vengono mantenuti anche quando Windows Media Player o Windows XP viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="e7131-123">Download states persist even when Windows Media Player or Windows XP is shut down.</span></span> |
| <span data-ttu-id="e7131-124">tempo reale</span><span class="sxs-lookup"><span data-stu-id="e7131-124">real time</span></span>  | <span data-ttu-id="e7131-125">(Tutti i sistemi operativi supportati). Il download viene eseguito in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="e7131-125">(All supported operating systems.) The download occurs all at once.</span></span> <span data-ttu-id="e7131-126">Nessun stato di download viene mantenuto tra le sessioni.</span><span class="sxs-lookup"><span data-stu-id="e7131-126">No download states persist between sessions.</span></span>                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7131-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e7131-127">Return value</span></span>

<span data-ttu-id="e7131-128">Questo metodo restituisce un oggetto **DownloadItem** .</span><span class="sxs-lookup"><span data-stu-id="e7131-128">This method returns a **DownloadItem** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7131-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7131-129">Remarks</span></span>

<span data-ttu-id="e7131-130">Quando viene avviato un nuovo download, gestione download lo aggiunge come elemento alla raccolta di download che ha avviato il download.</span><span class="sxs-lookup"><span data-stu-id="e7131-130">When a new download is started, Download Manager adds it as an item to the download collection that initiated the download.</span></span>

<span data-ttu-id="e7131-131">È possibile scaricare solo i formati multimediali digitali seguenti:</span><span class="sxs-lookup"><span data-stu-id="e7131-131">Only the following digital media formats can be downloaded:</span></span>

-   <span data-ttu-id="e7131-132">Advanced Systems Format (ASF)</span><span class="sxs-lookup"><span data-stu-id="e7131-132">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="e7131-133">MP3</span><span class="sxs-lookup"><span data-stu-id="e7131-133">MP3</span></span>
-   <span data-ttu-id="e7131-134">Windows Media Audio (WMA)</span><span class="sxs-lookup"><span data-stu-id="e7131-134">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="e7131-135">Windows Media Video (WMV)</span><span class="sxs-lookup"><span data-stu-id="e7131-135">Windows Media Video (WMV)</span></span>

<span data-ttu-id="e7131-136">Il parametro *sourceURL* non supporta stringhe con codifica Unicode.</span><span class="sxs-lookup"><span data-stu-id="e7131-136">The *sourceURL* parameter does not support Unicode-encoded strings.</span></span> <span data-ttu-id="e7131-137">Deve puntare al contenuto valido.</span><span class="sxs-lookup"><span data-stu-id="e7131-137">It must point to valid content.</span></span> <span data-ttu-id="e7131-138">I reindirizzamenti non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="e7131-138">Redirects are not supported.</span></span>

<span data-ttu-id="e7131-139">Quando si utilizza Windows XP, i file audio vengono inseriti automaticamente nelle sottocartelle **My Music** appropriate in base ai valori dei metadati a livello di file.</span><span class="sxs-lookup"><span data-stu-id="e7131-139">When using Windows XP, audio files are automatically placed into appropriate **My Music** subfolders based upon file-level metadata values.</span></span> <span data-ttu-id="e7131-140">I file video vengono inseriti nel \\ \\ \\  \\ *tipo* di numero casuale di download per musica, dove *numero casuale* è un valore casuale generato da Windows Media Player per ogni utente e il *tipo* è "tempo reale" o "sfondo", a seconda del tipo di download.</span><span class="sxs-lookup"><span data-stu-id="e7131-140">Video files are placed into \\My Music\\download\\*random number*\\*type*, where *random number* is a random value generated by Windows Media Player for each user, and *type* is either "real time" or "background", depending upon the download type.</span></span>

<span data-ttu-id="e7131-141">Quando si usa Windows Media Player 9 Series con Windows 98 e Windows Millennium Edition (me), i file audio e video vengono \\ inseriti nel \\ tipo di numero casuale di download Music \\  \\ , dove *numero casuale* è un valore casuale generato dal lettore per ogni utente e il *tipo* è "tempo reale" o "sfondo", a seconda del tipo di download.</span><span class="sxs-lookup"><span data-stu-id="e7131-141">When using Windows Media Player 9 Series with Windows 98 and Windows Millennium Edition (ME), audio and video files are placed into \\My Music\\download\\*random number*\\*type*, where *random number* is a random value generated by the Player for each user, and *type* is either "real time" or "background", depending upon the download type.</span></span>

<span data-ttu-id="e7131-142">Si noti che i file possono essere rinominati in base agli attributi dei metadati contenuti nel file e alle regole specificate dall'utente nella finestra di dialogo **Opzioni** .</span><span class="sxs-lookup"><span data-stu-id="e7131-142">Note that files may be renamed based upon metadata attributes contained in the file and rules specified by the user in the **Options** dialog box.</span></span> <span data-ttu-id="e7131-143">I file che non contengono metadati, ad esempio **album** o **Artist**, possono essere spostati in cartelle con etichetta Unknown Artist o Unknown album.</span><span class="sxs-lookup"><span data-stu-id="e7131-143">Files that don't contain metadata, such as **Album** or **Artist**, may be moved to folders labeled Unknown Artist or Unknown Album.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7131-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7131-144">Requirements</span></span>



| <span data-ttu-id="e7131-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7131-145">Requirement</span></span> | <span data-ttu-id="e7131-146">Valore</span><span class="sxs-lookup"><span data-stu-id="e7131-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e7131-147">Versione</span><span class="sxs-lookup"><span data-stu-id="e7131-147">Version</span></span><br/> | <span data-ttu-id="e7131-148">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e7131-148">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="e7131-149">DLL</span><span class="sxs-lookup"><span data-stu-id="e7131-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="e7131-150"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7131-150"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7131-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7131-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7131-152">**Download (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="e7131-152">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> <dt>

[<span data-ttu-id="e7131-153">**Oggetto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="e7131-153">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





