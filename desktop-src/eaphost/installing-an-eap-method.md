---
title: Installazione di un metodo EAP
description: Seguire le istruzioni riportate di seguito per installare un metodo EAP implementato dall'utente in un computer client che esegue EAPHost.
ms.assetid: c353550f-73a7-4195-81ea-544f74abc880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93e7796c216b5f60b7a46768ed9db9ca913482d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726287"
---
# <a name="installing-an-eap-method"></a><span data-ttu-id="289a8-103">Installazione di un metodo EAP</span><span class="sxs-lookup"><span data-stu-id="289a8-103">Installing an EAP Method</span></span>

<span data-ttu-id="289a8-104">Seguire le istruzioni riportate di seguito per installare un metodo EAP implementato dall'utente in un computer client che esegue EAPHost.</span><span class="sxs-lookup"><span data-stu-id="289a8-104">Follow the instructions below to install a user-implemented EAP method on a client computer running EAPHost.</span></span>

-   <span data-ttu-id="289a8-105">Implementare [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) e [**DLLUNREGISTERSERVER**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) per la dll del metodo EAP.</span><span class="sxs-lookup"><span data-stu-id="289a8-105">Implement [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) for your EAP Method DLL.</span></span> <span data-ttu-id="289a8-106">Queste funzioni aggiungono e rimuovono le chiavi del registro di sistema appropriate per il metodo EAP durante il processo di installazione e (disinstallazione).</span><span class="sxs-lookup"><span data-stu-id="289a8-106">These functions add and remove the appropriate registry keys for your EAP method during the installation and (uninstallation) process.</span></span>

    <span data-ttu-id="289a8-107">Per informazioni sulle chiavi del registro di sistema specifiche associate all'installazione di un metodo EAP, vedere l'argomento configurazione del registro di sistema [per i metodi EAP](registry-keys-for-eap-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="289a8-107">For information on the specific registry keys associated with the installation of an EAP method, see the [Registry Configuration for EAP Methods](registry-keys-for-eap-methods.md) topic.</span></span>

-   <span data-ttu-id="289a8-108">Installare la DLL che contiene l'implementazione del metodo EAP con il comando della console seguente.</span><span class="sxs-lookup"><span data-stu-id="289a8-108">Install the DLL that contains the EAP method implementation with the following console command.</span></span>

    <span data-ttu-id="289a8-109"> *&lt; Nome &gt; della dll* regsvr32.exe</span><span class="sxs-lookup"><span data-stu-id="289a8-109">**regsvr32.exe** *&lt;DLL name&gt;*</span></span>

    <span data-ttu-id="289a8-110">Per disinstallare la DLL, usare il comando console seguente:</span><span class="sxs-lookup"><span data-stu-id="289a8-110">To uninstall the DLL, use the following console command:</span></span>

    <span data-ttu-id="289a8-111">**regsvr32.exe** **/u** *&lt; nome &gt; dll*</span><span class="sxs-lookup"><span data-stu-id="289a8-111">**regsvr32.exe** **/u** *&lt;DLL name&gt;*</span></span>

-   <span data-ttu-id="289a8-112">Riavviare il servizio EAPHost.</span><span class="sxs-lookup"><span data-stu-id="289a8-112">Restart the EAPHost service.</span></span>

## <a name="related-topics"></a><span data-ttu-id="289a8-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="289a8-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="289a8-114">Uso di EAPHost</span><span class="sxs-lookup"><span data-stu-id="289a8-114">Using EAPHost</span></span>](using-eap-host.md)
</dt> </dl>

 

 