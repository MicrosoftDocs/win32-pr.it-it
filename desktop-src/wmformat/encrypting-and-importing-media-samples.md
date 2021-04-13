---
title: Crittografia e importazione di esempi di supporti
description: Crittografia e importazione di esempi di supporti
ms.assetid: f9784c9a-c672-432d-a3ad-eb2ed73ac523
keywords:
- Windows Media Format SDK, importazione DRM
- Windows Media Format SDK, importazione
- Windows Media Format SDK, crittografia degli esempi di supporti
- Digital Rights Management (DRM), importazione
- DRM (Digital Rights Management), importazione
- Digital Rights Management (DRM), crittografia degli esempi di supporti
- DRM (Digital Rights Management), crittografia degli esempi di supporti
- API estese del client DRM, importazione
- API estese client, importazione
- API estese del client DRM, crittografia degli esempi di supporti
- API estese del client, crittografia degli esempi di contenuti multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473db9580990b62818842aaa5eeea3e82f38c5ad
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398567"
---
# <a name="encrypting-and-importing-media-samples"></a><span data-ttu-id="5dcc0-114">Crittografia e importazione di esempi di supporti</span><span class="sxs-lookup"><span data-stu-id="5dcc0-114">Encrypting and Importing Media Samples</span></span>

<span data-ttu-id="5dcc0-115">Per ogni esempio di supporto crittografato con Windows Media DRM, è necessario generare un valore salt che è strettamente superiore rispetto a quello precedente (a incremento progressivo costante).</span><span class="sxs-lookup"><span data-stu-id="5dcc0-115">For each media sample that you encrypt using Windows Media DRM, you must generate a salt value that is strictly bigger than the previous one (monotonically increasing).</span></span> <span data-ttu-id="5dcc0-116">Usare il nuovo valore salt per creare una chiave di crittografia transitoria applicando l'algoritmo di crittografia SHA-1 al vettore di inizializzazione concatenato con il valore salt.</span><span class="sxs-lookup"><span data-stu-id="5dcc0-116">Use the new salt value to create a transitory encryption key by applying the SHA-1 encryption algorithm to the initialization vector concatenated with the salt value.</span></span>

<span data-ttu-id="5dcc0-117">Successivamente, crittografare l'esempio in base all'algoritmo RC4 usando la chiave transitoria generata.</span><span class="sxs-lookup"><span data-stu-id="5dcc0-117">Next, encrypt the sample according to the RC4 algorithm using the generated transitory key.</span></span> <span data-ttu-id="5dcc0-118">Prima che l'esempio venga passato all'SDK, l'applicazione deve associare il valore salt all'esempio impostando un attributo di estensione.</span><span class="sxs-lookup"><span data-stu-id="5dcc0-118">Before the sample is passed to the SDK, your application must associate the salt value with the sample by setting an extension attribute.</span></span>

<span data-ttu-id="5dcc0-119">Ecco i passaggi per la crittografia degli esempi di supporti:</span><span class="sxs-lookup"><span data-stu-id="5dcc0-119">Here are the steps for encrypting media samples:</span></span>

1.  <span data-ttu-id="5dcc0-120">Chiamare il metodo **QueryInterface** dell'oggetto di esempio per ottenere l'interfaccia [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) .</span><span class="sxs-lookup"><span data-stu-id="5dcc0-120">Call the **QueryInterface** method of the sample object to get the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface.</span></span>
2.  <span data-ttu-id="5dcc0-121">Incrementare il valore salt.</span><span class="sxs-lookup"><span data-stu-id="5dcc0-121">Increment the salt value.</span></span>
3.  <span data-ttu-id="5dcc0-122">Crittografare l'esempio usando un algoritmo di crittografia RC1.</span><span class="sxs-lookup"><span data-stu-id="5dcc0-122">Encrypt the sample using an RC1 encryption algorithm.</span></span> <span data-ttu-id="5dcc0-123">Per la crittografia si crea una chiave concatenando il vettore di inizializzazione e il valore salt.</span><span class="sxs-lookup"><span data-stu-id="5dcc0-123">For the encryption you create a key by concatenating the initialization vector and the salt value.</span></span>
4.  <span data-ttu-id="5dcc0-124">Specificare il valore salt per l'SDK chiamando [**INSSBuffer:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty).</span><span class="sxs-lookup"><span data-stu-id="5dcc0-124">Provide the salt value to the SDK by calling [**INSSBuffer::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5dcc0-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5dcc0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5dcc0-126">**Importazione DRM**</span><span class="sxs-lookup"><span data-stu-id="5dcc0-126">**DRM Import**</span></span>](drm-import.md)
</dt> <dt>

[<span data-ttu-id="5dcc0-127">**Esempio di crittografia di esempio multimediale**</span><span class="sxs-lookup"><span data-stu-id="5dcc0-127">**Media Sample Encryption Example**</span></span>](media-sample-encryption-example.md)
</dt> </dl>

 

 




