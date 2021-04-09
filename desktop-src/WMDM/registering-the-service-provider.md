---
title: Registrazione del provider di servizi
description: Registrazione del provider di servizi
ms.assetid: 556d6519-bc24-446b-a360-e3d83b40d541
keywords:
- Windows Media Gestione dispositivi, registrazione dei provider di servizi
- Gestione dispositivi, registrazione di provider di servizi
- Guida per programmatori, registrazione di provider di servizi
- provider di servizi, registrazione di provider di servizi
- creazione di provider di servizi, registrazione di provider di servizi
- registrazione di provider di servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1226b724b06990fc1e000a522e3a61672789cf3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044252"
---
# <a name="registering-the-service-provider"></a><span data-ttu-id="85afe-109">Registrazione del provider di servizi</span><span class="sxs-lookup"><span data-stu-id="85afe-109">Registering the Service Provider</span></span>

<span data-ttu-id="85afe-110">Oltre a essere registrato come oggetto COM, un provider di servizi deve essere registrato come plug-in a Windows Media Gestione dispositivi.</span><span class="sxs-lookup"><span data-stu-id="85afe-110">In addition to being registered as a COM object, a service provider must be registered as a plug-in to Windows Media Device Manager.</span></span> <span data-ttu-id="85afe-111">Per eseguire la registrazione, un provider di servizi deve creare la seguente chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="85afe-111">To register, a service provider must create the following registry key:</span></span>

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Media Device Manager\Plugins\SP\<             `

<span data-ttu-id="85afe-112">In questa chiave < *il nome del provider di servizi* > è il nome della dll. ad esempio, il provider di servizi di esempio utilizza MsHDSP.</span><span class="sxs-lookup"><span data-stu-id="85afe-112">In this key, < *your service provider name* > is the name of your DLL; for example, the sample service provider uses MsHDSP.</span></span> <span data-ttu-id="85afe-113">La chiave ProgID deve avere un valore stringa corrispondente al CLSID del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="85afe-113">The ProgID key should have a string value that corresponds to the CLSID of your service provider.</span></span> <span data-ttu-id="85afe-114">Ad esempio, il provider di servizi di esempio ha il valore "MDServiceProviderHD. MDServiceProviderHD".</span><span class="sxs-lookup"><span data-stu-id="85afe-114">For instance, the sample service provider has the value "MDServiceProviderHD.MDServiceProviderHD".</span></span>

<span data-ttu-id="85afe-115">L'implementazione del provider di servizi di esempio di DLLRegisterServer in MDSP. cpp aggiunge questa chiave del registro di sistema quando si registra la DLL del provider di servizi di esempio.</span><span class="sxs-lookup"><span data-stu-id="85afe-115">The sample service provider's implementation of DLLRegisterServer in Mdsp.cpp adds this registry key when you register the sample service provider DLL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85afe-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="85afe-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85afe-117">**Creazione di un provider di servizi**</span><span class="sxs-lookup"><span data-stu-id="85afe-117">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




