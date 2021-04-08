---
title: Creazione di licenze localmente
description: Creazione di licenze localmente
ms.assetid: 151dd231-26a9-4203-84e1-446a07c1e07a
keywords:
- Windows Media Format SDK, creazione di licenze localmente
- Windows Media Format SDK, licenze
- Digital Rights Management (DRM), creazione di licenze localmente
- DRM (Digital Rights Management), creazione di licenze localmente
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- API estese del client DRM, creazione di licenze localmente
- API estese client, creazione di licenze localmente
- licenze, creazione di licenze in locale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32fc4305c77be2132611df925ae08458fe2bb4a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045333"
---
# <a name="creating-licenses-locally"></a><span data-ttu-id="21783-112">Creazione di licenze localmente</span><span class="sxs-lookup"><span data-stu-id="21783-112">Creating Licenses Locally</span></span>

<span data-ttu-id="21783-113">In alcuni casi, ad esempio durante l' [importazione di DRM](drm-import.md), è possibile creare licenze personalizzate.</span><span class="sxs-lookup"><span data-stu-id="21783-113">In certain circumstances, such as during [DRM Import](drm-import.md), you can create your own licenses.</span></span> <span data-ttu-id="21783-114">Le licenze DRM di Windows Media possono essere scritte in modi diversi, ma per creare una licenza personalizzata è necessario utilizzare lo schema binario XMR (Extensible Media Rights).</span><span class="sxs-lookup"><span data-stu-id="21783-114">Windows Media DRM licenses can be written a few different ways, but to make your own license, you must use the Extensible Media Rights (XMR) binary schema.</span></span> <span data-ttu-id="21783-115">Per ulteriori informazioni, vedere la pagina relativa alla [compilazione di una licenza XMR](building-an-xmr-license.md).</span><span class="sxs-lookup"><span data-stu-id="21783-115">For more information, see [Building an XMR License](building-an-xmr-license.md).</span></span>

<span data-ttu-id="21783-116">Quando si crea una licenza, è possibile aggiungerla all'archivio licenze locale chiamando il metodo [**IWMDRMLicenseManagement:: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="21783-116">When you create a license, you can add it to the local license store by calling the [**IWMDRMLicenseManagement::StoreLicense**](iwmdrmlicensemanagement-storelicense.md) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="21783-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="21783-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21783-118">**Acquisizione di licenze**</span><span class="sxs-lookup"><span data-stu-id="21783-118">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="21783-119">**Creazione di una licenza XMR**</span><span class="sxs-lookup"><span data-stu-id="21783-119">**Building an XMR License**</span></span>](building-an-xmr-license.md)
</dt> </dl>

 

 




