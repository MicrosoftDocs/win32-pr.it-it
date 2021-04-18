---
title: Chiave e ID chiave
description: Chiave e ID chiave
ms.assetid: 40618771-d601-4c31-8da9-5c649651f2f2
keywords:
- Windows Media Format SDK, Digital Rights Management (DRM)
- Digital Rights Management (DRM), chiavi
- DRM (Digital Rights Management), chiavi
- Digital Rights Management (DRM), KID
- DRM (Digital Rights Management), KID
- ID chiave (KID)
- KID (ID chiave)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca7f74521fdf0f6cc268b8af1259f8468087f45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298141"
---
# <a name="key-and-key-id"></a><span data-ttu-id="f89cb-110">Chiave e ID chiave</span><span class="sxs-lookup"><span data-stu-id="f89cb-110">Key and Key ID</span></span>

<span data-ttu-id="f89cb-111">Quando si crea il pacchetto di un file, si usa una chiave.</span><span class="sxs-lookup"><span data-stu-id="f89cb-111">When you package a file, you use a key.</span></span> <span data-ttu-id="f89cb-112">Una chiave è una porzione di dati usati negli algoritmi di crittografia che proteggono il contenuto.</span><span class="sxs-lookup"><span data-stu-id="f89cb-112">A key is a piece of data used in the encryption algorithms that protect the content.</span></span> <span data-ttu-id="f89cb-113">Sono disponibili due parti per ogni chiave, ovvero un valore di inizializzazione della chiave di licenza e un ID chiave (spesso abbreviato come KID).</span><span class="sxs-lookup"><span data-stu-id="f89cb-113">There are two parts to each key: a license key seed and a key ID (often abbreviated as KID).</span></span> <span data-ttu-id="f89cb-114">L'ID chiave è pubblico e viene archiviato nell'intestazione del file come un modo per identificare la chiave necessaria per decrittografare il file.</span><span class="sxs-lookup"><span data-stu-id="f89cb-114">The key ID is public, and is stored in the file header as a way to identify the key required to decrypt the file.</span></span> <span data-ttu-id="f89cb-115">Il valore di inizializzazione chiave di licenza è un valore segreto che deve essere condiviso dal pacchetto di contenuto e dall'emittente della licenza.</span><span class="sxs-lookup"><span data-stu-id="f89cb-115">The license key seed is a secret value that must be shared by the content packager and the license issuer.</span></span>

<span data-ttu-id="f89cb-116">Un ID chiave identifica il contenuto protetto dal punto di vista della licenza.</span><span class="sxs-lookup"><span data-stu-id="f89cb-116">A key ID identifies protected content from the perspective of the license.</span></span> <span data-ttu-id="f89cb-117">Sebbene sia possibile utilizzare lo stesso ID chiave per più file, è consigliabile utilizzare sempre un ID chiave univoco per ogni parte del contenuto protetto.</span><span class="sxs-lookup"><span data-stu-id="f89cb-117">Although you can use the same key ID for multiple files, it is recommended that you always use a unique key ID for each piece of protected content.</span></span>

<span data-ttu-id="f89cb-118">Molti dei metodi descritti in questa documentazione usano le stringhe ID chiave per selezionare le licenze.</span><span class="sxs-lookup"><span data-stu-id="f89cb-118">Many of the methods described in this documentation use key ID strings to select licenses.</span></span> <span data-ttu-id="f89cb-119">Queste stringhe contengono l'ID chiave codificato in Base64.</span><span class="sxs-lookup"><span data-stu-id="f89cb-119">These strings contain the key ID encoded in base64.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f89cb-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f89cb-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f89cb-121">**Concetti**</span><span class="sxs-lookup"><span data-stu-id="f89cb-121">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 




