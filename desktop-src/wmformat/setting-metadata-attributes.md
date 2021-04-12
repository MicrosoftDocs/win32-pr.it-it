---
title: Impostazione degli attributi dei metadati
description: Impostazione degli attributi dei metadati
ms.assetid: a5d99361-9919-4548-a24d-900ac65cc634
keywords:
- Windows Media Format SDK, impostazione degli attributi dei metadati
- ASF (Advanced Systems Format), impostazione degli attributi dei metadati
- ASF (Advanced Systems Format), impostazione degli attributi dei metadati
- metadati, impostazione degli attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfde27d7bc965076d1a4b5f9674c6d198ce61da5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398616"
---
# <a name="setting-metadata-attributes"></a><span data-ttu-id="1a2da-107">Impostazione degli attributi dei metadati</span><span class="sxs-lookup"><span data-stu-id="1a2da-107">Setting Metadata Attributes</span></span>

<span data-ttu-id="1a2da-108">Gli attributi dei metadati vengono impostati tramite il metodo [**IWMHeaderInfo3:: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) .</span><span class="sxs-lookup"><span data-stu-id="1a2da-108">Metadata attributes are set by using the [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) method.</span></span>

<span data-ttu-id="1a2da-109">A tutti gli attributi viene assegnata una lingua dall'elenco di lingue per il file.</span><span class="sxs-lookup"><span data-stu-id="1a2da-109">All attributes are assigned a language from the language list for the file.</span></span> <span data-ttu-id="1a2da-110">È possibile accedere all'elenco di lingue usando l'interfaccia [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) .</span><span class="sxs-lookup"><span data-stu-id="1a2da-110">You can access the language list by using the [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) interface.</span></span> <span data-ttu-id="1a2da-111">Per ottenere un puntatore a un'interfaccia **IWMLanguageList** , chiamare **QueryInterface** su qualsiasi interfaccia dell'oggetto da cui è stato ottenuto [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3).</span><span class="sxs-lookup"><span data-stu-id="1a2da-111">To get a pointer to an **IWMLanguageList** interface, call **QueryInterface** on any interface of the object from which you have obtained [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3).</span></span>

<span data-ttu-id="1a2da-112">È possibile aggiungere attributi con qualsiasi nome.</span><span class="sxs-lookup"><span data-stu-id="1a2da-112">You can add attributes with any name you like.</span></span> <span data-ttu-id="1a2da-113">Tuttavia, l'utilizzo di nomi di attributo che non sono nomi standard supportati da Windows Media Format SDK può rendere i metadati più difficili da individuare.</span><span class="sxs-lookup"><span data-stu-id="1a2da-113">However, using attribute names that are not standard names supported by the Windows Media Format SDK can make your metadata difficult for users to discover.</span></span> <span data-ttu-id="1a2da-114">La maggior parte delle applicazioni per la riproduzione di contenuti multimediali verificherà i valori standard.</span><span class="sxs-lookup"><span data-stu-id="1a2da-114">Most media-playing applications will check for standard values.</span></span> <span data-ttu-id="1a2da-115">Per ulteriori informazioni, vedere [Custom Metadata](custom-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="1a2da-115">For more information, see [Custom Metadata](custom-metadata.md).</span></span>

<span data-ttu-id="1a2da-116">Non è possibile usare il numero di flusso 0xFFFF per aggiungere un attributo a livello globale.</span><span class="sxs-lookup"><span data-stu-id="1a2da-116">You cannot use stream number 0xFFFF to add an attribute globally.</span></span> <span data-ttu-id="1a2da-117">Per gli attributi a livello di file, è necessario assegnare ogni attributo a un numero di flusso specifico o a un flusso 0.</span><span class="sxs-lookup"><span data-stu-id="1a2da-117">You must assign each attribute to a specific stream number, or stream 0 for file-level attributes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a2da-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1a2da-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a2da-119">**Utilizzo dei metadati**</span><span class="sxs-lookup"><span data-stu-id="1a2da-119">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




