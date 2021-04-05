---
title: Condivisione surrogati
description: I server DLL condivideranno un surrogato se hanno identità di sicurezza corrispondenti e condividono lo stesso valore AppID.
ms.assetid: 88544be1-4716-47b6-9c08-2b5b2b178e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6a934f03d42113cf73df4f059ac108801d21ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709424"
---
# <a name="surrogate-sharing"></a><span data-ttu-id="8ac68-103">Condivisione surrogati</span><span class="sxs-lookup"><span data-stu-id="8ac68-103">Surrogate Sharing</span></span>

<span data-ttu-id="8ac68-104">I server DLL condivideranno un surrogato se hanno identità di sicurezza corrispondenti e condividono lo stesso valore AppID.</span><span class="sxs-lookup"><span data-stu-id="8ac68-104">DLL servers will share a surrogate if they have matching security identities and share the same AppID value.</span></span>

<span data-ttu-id="8ac68-105">Per impostazione predefinita, i server DLL vengono caricati nel proprio processo surrogato.</span><span class="sxs-lookup"><span data-stu-id="8ac68-105">DLL servers are loaded, by default, into their own surrogate process.</span></span> <span data-ttu-id="8ac68-106">Per caricare altri server DLL in un surrogato esistente in modo che supporti più di un server DLL, esistono due requisiti:</span><span class="sxs-lookup"><span data-stu-id="8ac68-106">To load other DLL servers into an existing surrogate so that it supports more than one DLL server, there are two requirements:</span></span>

-   <span data-ttu-id="8ac68-107">I server DLL devono avere lo stesso valore AppID.</span><span class="sxs-lookup"><span data-stu-id="8ac68-107">The DLL servers must have the same AppID value.</span></span>
-   <span data-ttu-id="8ac68-108">Il contesto di sicurezza dei server DLL deve essere lo stesso.</span><span class="sxs-lookup"><span data-stu-id="8ac68-108">The security context of the DLL servers must be the same.</span></span>

<span data-ttu-id="8ac68-109">Se due server DLL devono essere avviati con diverse identità di sicurezza, devono trovarsi in surrogati diversi, indipendentemente dal fatto che i rispettivi AppID corrispondano.</span><span class="sxs-lookup"><span data-stu-id="8ac68-109">If two DLL servers are to be launched under different security identities, they must be in different surrogates, whether their AppIDs match.</span></span>

<span data-ttu-id="8ac68-110">Di seguito è riportato un esempio di amministrazione della condivisione surrogata con AppID:</span><span class="sxs-lookup"><span data-stu-id="8ac68-110">Following is an example of administering surrogate sharing with AppIDs:</span></span>

``` syntax
    AppID
        {12345678-0000-0000-0000-abcdabcdabcd}
            @DllSurrogate    REG_SZ
    CLSID
        {12345678-0000-0000-0000-000000000001}
            @AppId    REG_SZ    {12345678-0000-0000-0000-abcdabcdabcd}
            InProcServer32
    @    REG_SZ    c:\myapp\comp1.dll
        {12345678-0000-0000-0000-000000000002}
            @AppId    REG_SZ    {12345678-0000-0000-0000-abcdabcdabcd}
            InProcServer32
    @    REG_SZ    c:\myapp\comp2.dll
 
```

<span data-ttu-id="8ac68-111">I due CLSID per i componenti DLL comp1.dll e comp2.dll sono stati configurati per la condivisione di un AppID.</span><span class="sxs-lookup"><span data-stu-id="8ac68-111">The two CLSIDs for DLL components comp1.dll and comp2.dll have been configured to share an AppID.</span></span> <span data-ttu-id="8ac68-112">La chiave [AppID](appid-key.md) specifica che il server dll può essere caricato in un surrogato specificando il valore [DllSurrogate](dllsurrogate.md) .</span><span class="sxs-lookup"><span data-stu-id="8ac68-112">The [AppID](appid-key.md) key specifies that the DLL server can be loaded in a surrogate by specifying the [DllSurrogate](dllsurrogate.md) value.</span></span> <span data-ttu-id="8ac68-113">In questo esempio, il valore **DllSurrogate** è una stringa vuota, che indica che deve essere utilizzata l'implementazione di sistema predefinita del surrogato della dll.</span><span class="sxs-lookup"><span data-stu-id="8ac68-113">In this example, the **DllSurrogate** value is an empty string, indicating that the default system implementation of the DLL surrogate should be used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ac68-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8ac68-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ac68-115">Requisiti del server DLL</span><span class="sxs-lookup"><span data-stu-id="8ac68-115">DLL Server Requirements</span></span>](dll-server-requirements.md)
</dt> <dt>

[<span data-ttu-id="8ac68-116">Registrazione del server DLL per l'attivazione surrogata</span><span class="sxs-lookup"><span data-stu-id="8ac68-116">Registering the DLL Server for Surrogate Activation</span></span>](registering-the-dll-server-for-surrogate-activation.md)
</dt> </dl>

 

 




