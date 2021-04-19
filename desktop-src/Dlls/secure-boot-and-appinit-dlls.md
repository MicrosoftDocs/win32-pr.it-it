---
description: A partire da Windows 8, l' \_ infrastruttura delle DLL AppInit è disabilitata quando è abilitato l'avvio protetto.
ms.assetid: 3ADE71C7-7113-4D26-8D6D-5609CAF13397
title: AppInit dll e avvio protetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2915dda53959f2a403a62112385fe80e735cbfd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317817"
---
# <a name="appinit-dlls-and-secure-boot"></a><span data-ttu-id="f5146-103">AppInit dll e avvio protetto</span><span class="sxs-lookup"><span data-stu-id="f5146-103">AppInit DLLs and Secure Boot</span></span>

<span data-ttu-id="f5146-104">A partire da Windows 8, l' \_ infrastruttura delle DLL AppInit è disabilitata quando è abilitato l'avvio protetto.</span><span class="sxs-lookup"><span data-stu-id="f5146-104">Starting in Windows 8, the AppInit\_DLLs infrastructure is disabled when secure boot is enabled.</span></span>

## <a name="about-appinit_dlls"></a><span data-ttu-id="f5146-105">Informazioni sulle \_ DLL AppInit</span><span class="sxs-lookup"><span data-stu-id="f5146-105">About AppInit\_DLLs</span></span>

<span data-ttu-id="f5146-106">L' \_ infrastruttura dll di AppInit fornisce un modo semplice per associare le API di sistema consentendo il caricamento di DLL personalizzate nello spazio degli indirizzi di ogni applicazione interattiva.</span><span class="sxs-lookup"><span data-stu-id="f5146-106">The AppInit\_DLLs infrastructure provides an easy way to hook system APIs by allowing custom DLLs to be loaded into the address space of every interactive application.</span></span> <span data-ttu-id="f5146-107">Le applicazioni e il software dannoso usano entrambe le DLL AppInit per lo stesso motivo di base, ovvero l'hook delle API; una volta caricata la DLL personalizzata, può associare un'API di sistema nota e implementare funzionalità alternative.</span><span class="sxs-lookup"><span data-stu-id="f5146-107">Applications and malicious software both use AppInit DLLs for the same basic reason, which is to hook APIs; after the custom DLL is loaded, it can hook a well-known system API and implement alternate functionality.</span></span> <span data-ttu-id="f5146-108">Un piccolo set di applicazioni legittime moderne utilizza questo meccanismo per caricare le dll, mentre un ampio set di malware utilizza questo meccanismo per compromettere i sistemi.</span><span class="sxs-lookup"><span data-stu-id="f5146-108">Only a small set of modern legitimate applications use this mechanism to load DLLs, while a large set of malware use this mechanism to compromise systems.</span></span> <span data-ttu-id="f5146-109">Anche le DLL AppInit legittime \_ possono causare involontariamente deadlock di sistema e problemi di prestazioni, pertanto l'uso di \_ DLL AppInit non è consigliato.</span><span class="sxs-lookup"><span data-stu-id="f5146-109">Even legitimate AppInit\_DLLs can unintentionally cause system deadlocks and performance problems, therefore usage of AppInit\_DLLs is not recommended.</span></span>

## <a name="appinit_dlls-and-secure-boot"></a><span data-ttu-id="f5146-110">AppInit \_ dll e avvio protetto</span><span class="sxs-lookup"><span data-stu-id="f5146-110">AppInit\_DLLs and secure boot</span></span>

<span data-ttu-id="f5146-111">Windows 8 ha adottato UEFI e l'avvio protetto per migliorare l'integrità complessiva del sistema e garantire una protezione avanzata da minacce sofisticate.</span><span class="sxs-lookup"><span data-stu-id="f5146-111">Windows 8 adopted UEFI and secure boot to improve the overall system integrity and to provide strong protection against sophisticated threats.</span></span> <span data-ttu-id="f5146-112">Quando è abilitato l'avvio protetto, il \_ meccanismo DLL AppInit è disabilitato come parte di un approccio senza compromessi per proteggere i clienti da malware e minacce.</span><span class="sxs-lookup"><span data-stu-id="f5146-112">When secure boot is enabled, the AppInit\_DLLs mechanism is disabled as part of a no-compromise approach to protect customers against malware and threats.</span></span>

<span data-ttu-id="f5146-113">Si noti che l'avvio protetto è un protocollo UEFI e non una funzionalità di Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f5146-113">Please note that secure boot is a UEFI protocol and not a Windows 8 feature.</span></span> <span data-ttu-id="f5146-114">Altre informazioni su UEFI e sulla specifica del protocollo di avvio protetto sono disponibili in [https://www.uefi.org](https://www.uefi.org/) .</span><span class="sxs-lookup"><span data-stu-id="f5146-114">More info on UEFI and the secure boot protocol specification can be found at [https://www.uefi.org](https://www.uefi.org/).</span></span>

## <a name="appinit_dlls-certification-requirement-for-windows-8-desktop-apps"></a><span data-ttu-id="f5146-115">\_Requisiti di certificazione delle DLL AppInit per le app desktop di Windows 8</span><span class="sxs-lookup"><span data-stu-id="f5146-115">AppInit\_DLLs certification requirement for Windows 8 desktop apps</span></span>

<span data-ttu-id="f5146-116">Uno dei requisiti di certificazione per le applicazioni desktop di Windows 8 è che l'app non deve caricare dll arbitrarie per intercettare le chiamate all'API Win32 usando il \_ meccanismo DLL AppInit.</span><span class="sxs-lookup"><span data-stu-id="f5146-116">One of the certification requirements for Windows 8 desktop apps is that the app must not load arbitrary DLLs to intercept Win32 API calls using the AppInit\_DLLs mechanism.</span></span> <span data-ttu-id="f5146-117">Per informazioni più dettagliate sui requisiti di certificazione, vedere la sezione 1,1 relativa ai [requisiti di certificazione per le app desktop di Windows 8](../win_cert/certification-requirements-for-windows-desktop-apps.md).</span><span class="sxs-lookup"><span data-stu-id="f5146-117">For more detailed information about the certification requirements, refer to section 1.1 of [Certification requirements for Windows 8 desktop apps](../win_cert/certification-requirements-for-windows-desktop-apps.md).</span></span>

## <a name="summary"></a><span data-ttu-id="f5146-118">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="f5146-118">Summary</span></span>

-   <span data-ttu-id="f5146-119">Il \_ meccanismo DLL AppInit non è un approccio consigliato per le applicazioni legittime, in quanto può causare problemi di prestazioni e deadlock del sistema.</span><span class="sxs-lookup"><span data-stu-id="f5146-119">The AppInit\_DLLs mechanism is not a recommended approach for legitimate applications because it can lead to system deadlocks and performance problems.</span></span>
-   <span data-ttu-id="f5146-120">Il \_ meccanismo DLL AppInit è disabilitato per impostazione predefinita quando è abilitato l'avvio protetto.</span><span class="sxs-lookup"><span data-stu-id="f5146-120">The AppInit\_DLLs mechanism is disabled by default when secure boot is enabled.</span></span>
-   <span data-ttu-id="f5146-121">L'uso \_ di DLL AppInit in un'app desktop di Windows 8 è un errore di certificazione di un'applicazione desktop Windows.</span><span class="sxs-lookup"><span data-stu-id="f5146-121">Using AppInit\_DLLs in a Windows 8 desktop app is a Windows desktop app certification failure.</span></span>

<span data-ttu-id="f5146-122">Vedere il white paper seguente per informazioni sulle DLL di AppInit in \_ Windows 7 e Windows server 2008 R2: [DLL AppInit in Windows 7 e windows Server 2008 R2](/previous-versions/windows/hardware/download/dn550976(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f5146-122">See the following whitepaper for info about AppInit\_DLLs on Windows 7 and Windows Server 2008 R2: [AppInit DLLs in Windows 7 and Windows Server 2008 R2](/previous-versions/windows/hardware/download/dn550976(v=vs.85)).</span></span>

 

 
