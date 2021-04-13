---
title: Run-Time il collegamento a Wtsapi32.dll
description: L'applicazione può usare l'API Servizi Desktop remoto per collegare in modo dinamico al Wtsapi32.dll in fase di esecuzione. A tale scopo, l'applicazione deve chiamare la funzione LoadLibrary per caricare Wtsapi32.dll.
ms.assetid: b8227e65-be08-4045-a74e-dd3f398a7b9f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c53a992955876bf812a87168d2c74b776cf0d4e6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399418"
---
# <a name="run-time-linking-to-wtsapi32dll"></a><span data-ttu-id="34ab3-104">Run-Time il collegamento a Wtsapi32.dll</span><span class="sxs-lookup"><span data-stu-id="34ab3-104">Run-Time linking to Wtsapi32.dll</span></span>

<span data-ttu-id="34ab3-105">Se l'applicazione viene eseguita in un ambiente che non è un ambiente Servizi Desktop remoto, ma si vuole che l'applicazione fornisca funzionalità aggiuntive quando viene eseguita in un ambiente Servizi Desktop remoto, l'applicazione può usare l'API Servizi Desktop remoto per implementare la funzionalità aggiuntiva e collegarsi dinamicamente al Wtsapi32.dll in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="34ab3-105">If your application runs in an environment that is not a Remote Desktop Services environment, but you want your application to provide additional functionality when it does run in a Remote Desktop Services environment, the application can use the Remote Desktop Services API to implement the additional functionality, and dynamically link to the Wtsapi32.dll at run time.</span></span> <span data-ttu-id="34ab3-106">A tale scopo, l'applicazione deve chiamare la funzione [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) per caricare Wtsapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="34ab3-106">To do this, your application should call the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to load Wtsapi32.dll.</span></span> <span data-ttu-id="34ab3-107">Se la chiamata a **LoadLibrary** ha esito negativo, l'applicazione può essere eseguita usando le funzionalità di base.</span><span class="sxs-lookup"><span data-stu-id="34ab3-107">If the **LoadLibrary** call fails, your application can run using its basic functionality.</span></span> <span data-ttu-id="34ab3-108">Se **LoadLibrary** ha esito positivo, l'applicazione può chiamare la funzione [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per recuperare i puntatori alle funzioni Servizi Desktop remoto che si desidera chiamare.</span><span class="sxs-lookup"><span data-stu-id="34ab3-108">If **LoadLibrary** succeeds, your application can call the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) function to retrieve pointers to the Remote Desktop Services functions that you want to call.</span></span>

<span data-ttu-id="34ab3-109">Se l'applicazione è destinata solo a un ambiente Servizi Desktop remoto, il collegamento dinamico non è necessario.</span><span class="sxs-lookup"><span data-stu-id="34ab3-109">If your application is intended only for a Remote Desktop Services environment, dynamic linking is not necessary.</span></span> <span data-ttu-id="34ab3-110">In questo caso, è possibile includere wtsapi32. h e il collegamento a wtsapi32. lib.</span><span class="sxs-lookup"><span data-stu-id="34ab3-110">In this case, you can include Wtsapi32.h and link with Wtsapi32.lib.</span></span> <span data-ttu-id="34ab3-111">Quindi, se l'applicazione viene avviata in un ambiente diverso da Servizi Desktop remoto, verrà chiusa perché Wtsapi32.dll non è presente.</span><span class="sxs-lookup"><span data-stu-id="34ab3-111">Then, if your application starts up in an environment other than Remote Desktop Services, it will exit because Wtsapi32.dll is not present.</span></span>

<span data-ttu-id="34ab3-112">Per informazioni su come determinare se l'applicazione è in esecuzione in un ambiente di Servizi Desktop remoto, vedere [rilevamento dell'ambiente Servizi Desktop remoto](detecting-the-terminal-services-environment.md).</span><span class="sxs-lookup"><span data-stu-id="34ab3-112">For information about determining whether your application is running in a Remote Desktop Services environment, see [Detecting the Remote Desktop Services Environment](detecting-the-terminal-services-environment.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="34ab3-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="34ab3-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34ab3-114">Linee guida generali per la programmazione</span><span class="sxs-lookup"><span data-stu-id="34ab3-114">General programming guidelines</span></span>](general-programming-guidelines.md)
</dt> </dl>

 

 