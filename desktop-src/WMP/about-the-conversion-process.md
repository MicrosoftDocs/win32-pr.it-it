---
title: Informazioni sul processo di conversione
description: Informazioni sul processo di conversione
ms.assetid: 147b82fd-9e82-4acf-8f8a-43eb02e99024
keywords:
- Media Player Windows, processo di conversione
- Plug-in di Windows Media Player, conversione
- plug-in, conversione
- plug-in di conversione, processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6fe2f2bbedf03b78c0d19abaf3793e8e92c788
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046325"
---
# <a name="about-the-conversion-process"></a><span data-ttu-id="bc484-107">Informazioni sul processo di conversione</span><span class="sxs-lookup"><span data-stu-id="bc484-107">About the Conversion Process</span></span>

<span data-ttu-id="bc484-108">Quando Windows Media Player crea un'istanza del plug-in di conversione, il processo procede come segue:</span><span class="sxs-lookup"><span data-stu-id="bc484-108">After Windows Media Player instantiates the conversion plug-in, the process proceeds as follows:</span></span>

1.  <span data-ttu-id="bc484-109">Il lettore chiama [IWMPConvert:: convertfile](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpconvert-convertfile).</span><span class="sxs-lookup"><span data-stu-id="bc484-109">The Player calls [IWMPConvert::ConvertFile](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpconvert-convertfile).</span></span>
2.  <span data-ttu-id="bc484-110">Il plug-in converte il file specificato nel parametro *bstrInputFile* in un formato ASF.</span><span class="sxs-lookup"><span data-stu-id="bc484-110">The plug-in converts the file provided in the *bstrInputFile* parameter into an ASF format.</span></span>
3.  <span data-ttu-id="bc484-111">Se per qualche motivo la conversione non riesce, il plug-in restituisce un codice di errore appropriato e il processo viene interrotto.</span><span class="sxs-lookup"><span data-stu-id="bc484-111">If the conversion fails for some reason, the plug-in returns an appropriate failure code and the process stops.</span></span>
4.  <span data-ttu-id="bc484-112">Se la conversione ha esito positivo, il plug-in inserisce il file convertito nella cartella specificata nel parametro *bstrDestinationFolder* e restituisce il percorso completo del file convertito tramite il parametro *pbstrOutputFile* .</span><span class="sxs-lookup"><span data-stu-id="bc484-112">If the conversion succeeds, the plug-in places the converted file into the folder provided in the *bstrDestinationFolder* parameter and returns the fully qualified path to the converted file through the *pbstrOutputFile* parameter.</span></span>
5.  <span data-ttu-id="bc484-113">Il plug-in restituisce un codice di esito positivo da **convertfile**.</span><span class="sxs-lookup"><span data-stu-id="bc484-113">The plug-in returns a success code from **ConvertFile**.</span></span>
6.  <span data-ttu-id="bc484-114">Il lettore copia il file convertito in una cartella nella gerarchia di cartelle musica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bc484-114">The Player copies the converted file to a folder in the user's music folder hierarchy.</span></span> <span data-ttu-id="bc484-115">Esattamente dove il lettore copia il file in dipende dal contenuto.</span><span class="sxs-lookup"><span data-stu-id="bc484-115">Exactly where the Player copies the file to depends on content.</span></span> <span data-ttu-id="bc484-116">Come parte di questo processo, il lettore potrebbe rinominare il file.</span><span class="sxs-lookup"><span data-stu-id="bc484-116">As part of this process, the Player might rename the file.</span></span>
7.  <span data-ttu-id="bc484-117">Il lettore copia il file originale (non convertito) in una cartella nella gerarchia di cartelle musica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bc484-117">The Player copies the original (unconverted) file to a folder in the user's music folder hierarchy.</span></span> <span data-ttu-id="bc484-118">Come parte di questo processo, il lettore potrebbe rinominare il file.</span><span class="sxs-lookup"><span data-stu-id="bc484-118">As part of this process, the Player might rename the file.</span></span> <span data-ttu-id="bc484-119">Si tratta della copia del file usato dal giocatore quando l'utente Sincronizza il contenuto dal computer a un dispositivo che richiede il formato di file originale.</span><span class="sxs-lookup"><span data-stu-id="bc484-119">This is the copy of the file that the Player uses when the user syncs the content from the computer to a device that requires the original file format.</span></span> <span data-ttu-id="bc484-120">Questo file è denominato *file shadow*.</span><span class="sxs-lookup"><span data-stu-id="bc484-120">This file is called a *shadow file*.</span></span>
8.  <span data-ttu-id="bc484-121">Il lettore aggiunge alla libreria informazioni sul file convertito.</span><span class="sxs-lookup"><span data-stu-id="bc484-121">The Player adds information about the converted file to the library.</span></span> <span data-ttu-id="bc484-122">Ciò include l'impostazione del valore per l'attributo **ShadowFilePath** sul nuovo percorso in cui viene salvato il file shadow.</span><span class="sxs-lookup"><span data-stu-id="bc484-122">This includes setting the value for the **ShadowFilePath** attribute to the new location where the shadow file is saved.</span></span>

<span data-ttu-id="bc484-123">Se è necessario utilizzare il file convertito, è possibile eseguire una query sulla libreria per recuperare il contenuto utilizzando gli attributi **contentdistributor** e **WM/UniqueFileIdentifier** .</span><span class="sxs-lookup"><span data-stu-id="bc484-123">If you need to work with the converted file, you can query the library to retrieve the content by using the **ContentDistributor** and **WM/UniqueFileIdentifier** attributes.</span></span> <span data-ttu-id="bc484-124">Se è necessario utilizzare il file shadow, è comunque necessario recuperare l'oggetto **multimediale** per il file convertito, quindi eseguire una query per l'attributo **ShadowFilePath** .</span><span class="sxs-lookup"><span data-stu-id="bc484-124">If you need to work with the shadow file, you must still retrieve the **Media** object for the converted file and then query for the **ShadowFilePath** attribute.</span></span> <span data-ttu-id="bc484-125">Vedere [aggiunta di metadati ai file convertiti](adding-metadata-to-converted-files.md).</span><span class="sxs-lookup"><span data-stu-id="bc484-125">See [Adding Metadata to Converted Files](adding-metadata-to-converted-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc484-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bc484-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc484-127">**Informazioni sui plug-in di conversione**</span><span class="sxs-lookup"><span data-stu-id="bc484-127">**About Conversion Plug-ins**</span></span>](about-conversion-plug-ins.md)
</dt> <dt>

[<span data-ttu-id="bc484-128">**Aggiunta di metadati ai file convertiti**</span><span class="sxs-lookup"><span data-stu-id="bc484-128">**Adding Metadata to Converted Files**</span></span>](adding-metadata-to-converted-files.md)
</dt> <dt>

[<span data-ttu-id="bc484-129">**Lettura di valori di attributo**</span><span class="sxs-lookup"><span data-stu-id="bc484-129">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="bc484-130">**Attributo ShadowFilePath**</span><span class="sxs-lookup"><span data-stu-id="bc484-130">**ShadowFilePath Attribute**</span></span>](shadowfilepath-attribute.md)
</dt> <dt>

[<span data-ttu-id="bc484-131">**Attributo WM/ContentDistributor**</span><span class="sxs-lookup"><span data-stu-id="bc484-131">**WM/ContentDistributor Attribute**</span></span>](wm-contentdistributor-attribute.md)
</dt> <dt>

[<span data-ttu-id="bc484-132">**Attributo WM/UniqueFileIdentifier**</span><span class="sxs-lookup"><span data-stu-id="bc484-132">**WM/UniqueFileIdentifier Attribute**</span></span>](wm-uniquefileidentifier-attribute.md)
</dt> </dl>

 

 




