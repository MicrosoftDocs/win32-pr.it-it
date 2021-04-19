---
title: Accesso a una visualizzazione del registro di sistema alternativa
description: Per impostazione predefinita, un'applicazione a 32 bit in esecuzione su WOW64 accede alla visualizzazione del Registro di sistema a 32 bit e un'applicazione a 64 bit accede alla visualizzazione del Registro di sistema a 64 bit.
ms.assetid: 2c5fd3de-998c-44ab-863e-8e0e90d56e5d
keywords:
- Visualizzazioni del registro di sistema a 64 bit programmazione Windows
- Programmazione Windows WOW64 a 64 bit, viste del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3bca57367394e1b2fffc6486065e93c966f224
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "106320252"
---
# <a name="accessing-an-alternate-registry-view"></a><span data-ttu-id="1d10a-105">Accesso a una visualizzazione del registro di sistema alternativa</span><span class="sxs-lookup"><span data-stu-id="1d10a-105">Accessing an Alternate Registry View</span></span>

<span data-ttu-id="1d10a-106">Per impostazione predefinita, un'applicazione a 32 bit in esecuzione su WOW64 accede alla visualizzazione del Registro di sistema a 32 bit e un'applicazione a 64 bit accede alla visualizzazione del Registro di sistema a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="1d10a-106">By default, a 32-bit application running on WOW64 accesses the 32-bit registry view and a 64-bit application accesses the 64-bit registry view.</span></span> <span data-ttu-id="1d10a-107">I flag seguenti consentono alle applicazioni a 32 bit di accedere alle chiavi reindirizzate nella visualizzazione del registro di sistema a 64 bit e alle applicazioni a 64 bit per accedere alle chiavi reindirizzate nella visualizzazione del registro di sistema a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="1d10a-107">The following flags enable 32-bit applications to access redirected keys in the 64-bit registry view and 64-bit applications to access redirected keys in the 32-bit registry view.</span></span> <span data-ttu-id="1d10a-108">Questi flag non hanno effetto sulle chiavi del registro di sistema condivise.</span><span class="sxs-lookup"><span data-stu-id="1d10a-108">These flags have no effect on shared registry keys.</span></span> <span data-ttu-id="1d10a-109">Per altre informazioni, vedere [chiavi del registro di sistema interessate da WOW64](shared-registry-keys.md).</span><span class="sxs-lookup"><span data-stu-id="1d10a-109">For more information, see [Registry Keys Affected by WOW64](shared-registry-keys.md).</span></span>



| <span data-ttu-id="1d10a-110">Nome del flag</span><span class="sxs-lookup"><span data-stu-id="1d10a-110">Flag name</span></span>         | <span data-ttu-id="1d10a-111">Valore</span><span class="sxs-lookup"><span data-stu-id="1d10a-111">Value</span></span>  | <span data-ttu-id="1d10a-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d10a-112">Description</span></span>                                                                                                                                                                                                                                       |
|-------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d10a-113">CHIAVE \_ WOW64 \_ 64KEY</span><span class="sxs-lookup"><span data-stu-id="1d10a-113">KEY\_WOW64\_64KEY</span></span> | <span data-ttu-id="1d10a-114">0x0100</span><span class="sxs-lookup"><span data-stu-id="1d10a-114">0x0100</span></span> | <span data-ttu-id="1d10a-115">Accedere a una chiave a 64 bit da un'applicazione a 32 bit o a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="1d10a-115">Access a 64-bit key from either a 32-bit or 64-bit application.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="1d10a-116">CHIAVE \_ WOW64 \_ 32KEY</span><span class="sxs-lookup"><span data-stu-id="1d10a-116">KEY\_WOW64\_32KEY</span></span> | <span data-ttu-id="1d10a-117">0x0200</span><span class="sxs-lookup"><span data-stu-id="1d10a-117">0x0200</span></span> | <span data-ttu-id="1d10a-118">Accedere a una chiave a 32 bit da un'applicazione a 32 bit o a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="1d10a-118">Access a 32-bit key from either a 32-bit or 64-bit application.</span></span><br/><span data-ttu-id="1d10a-119">**Windows 10 su ARM:** Si fa riferimento alla visualizzazione del registro di sistema ARM a 32 bit per i processi ARM a 32 bit e alla visualizzazione del registro di sistema x86 a 32 bit per i processi ARM64 a 32 bit x86 e a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="1d10a-119">**Windows 10 on ARM:** This refers to the 32-bit ARM registry view for 32-bit ARM processes and the 32-bit x86 registry view for 32-bit x86 and 64-bit ARM64 processes.</span></span> |



 

<span data-ttu-id="1d10a-120">Questi flag possono essere specificati nel parametro *samDesired* delle funzioni del registro di sistema seguenti:</span><span class="sxs-lookup"><span data-stu-id="1d10a-120">These flags can be specified in the *samDesired* parameter of the following registry functions:</span></span>

-   [<span data-ttu-id="1d10a-121">**RegCreateKeyEx**</span><span class="sxs-lookup"><span data-stu-id="1d10a-121">**RegCreateKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [<span data-ttu-id="1d10a-122">**RegDeleteKeyEx**</span><span class="sxs-lookup"><span data-stu-id="1d10a-122">**RegDeleteKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regdeletekeyexa)
-   [<span data-ttu-id="1d10a-123">**RegOpenKeyEx**</span><span class="sxs-lookup"><span data-stu-id="1d10a-123">**RegOpenKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)

<span data-ttu-id="1d10a-124">\_ \_ È possibile specificare la chiave WOW64 32KEY o la chiave \_ WOW64 \_ 64KEY.</span><span class="sxs-lookup"><span data-stu-id="1d10a-124">Either KEY\_WOW64\_32KEY or KEY\_WOW64\_64KEY can be specified.</span></span> <span data-ttu-id="1d10a-125">Se vengono specificati entrambi i flag, la funzione ha esito negativo con errore \_ parametro non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="1d10a-125">If both flags are specified, the function fails with ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="1d10a-126">**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Se vengono specificati entrambi i flag, il comportamento della funzione non è definito.</span><span class="sxs-lookup"><span data-stu-id="1d10a-126">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** If both flags are specified, the function s behavior is undefined.</span></span>

<span data-ttu-id="1d10a-127">Impossibile utilizzare la funzione [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya) per accedere a una visualizzazione del registro di sistema alternativa.</span><span class="sxs-lookup"><span data-stu-id="1d10a-127">The [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya) function cannot be used to access an alternate registry view.</span></span>

<span data-ttu-id="1d10a-128">Di seguito sono illustrate le procedure consigliate per l'accesso al registro di sistema da un'applicazione:</span><span class="sxs-lookup"><span data-stu-id="1d10a-128">The following are best practices when accessing the registry from an application:</span></span>

-   <span data-ttu-id="1d10a-129">Dopo che l'applicazione ha eseguito l'accesso a una visualizzazione del registro di sistema alternativa utilizzando uno dei flag, tutte le operazioni successive (crea, Elimina o Apri) sulle chiavi del registro di sistema figlio devono utilizzare in modo esplicito lo stesso flag.</span><span class="sxs-lookup"><span data-stu-id="1d10a-129">After the application has accessed an alternate registry view using one of the flags, all subsequent operations (create, delete, or open) on child registry keys must explicitly use the same flag.</span></span> <span data-ttu-id="1d10a-130">In caso contrario, è possibile che si verifichi un comportamento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="1d10a-130">Otherwise, there can be unexpected behavior.</span></span>
-   <span data-ttu-id="1d10a-131">Per enumerare accuratamente tutte le chiavi in entrambe le visualizzazioni, eseguire l'enumerazione in due passaggi.</span><span class="sxs-lookup"><span data-stu-id="1d10a-131">To accurately enumerate all keys in both views, perform the enumeration in two passes.</span></span> <span data-ttu-id="1d10a-132">Il primo passaggio deve usare un handle aperto con uno dei flag e l'altro pass deve usare un handle aperto con l'altro flag.</span><span class="sxs-lookup"><span data-stu-id="1d10a-132">The first pass should use a handle opened with one of the flags, and the other pass should use a handle opened with the other flag.</span></span>

> [!Note]  
> <span data-ttu-id="1d10a-133">Le chiavi **Wow6432Node** e **WowAA32Node** sono riservate.</span><span class="sxs-lookup"><span data-stu-id="1d10a-133">The **Wow6432Node** and **WowAA32Node** keys are reserved.</span></span> <span data-ttu-id="1d10a-134">Per compatibilità, le applicazioni non devono utilizzare direttamente queste chiavi.</span><span class="sxs-lookup"><span data-stu-id="1d10a-134">For compatibility, applications should not use these keys directly.</span></span>

 

<span data-ttu-id="1d10a-135">Per informazioni sull'accesso alla visualizzazione del registro di sistema alternativa tramite WMI, vedere [richiesta di dati WMI in una piattaforma a 64 bit](/windows/desktop/WmiSdk/requesting-wmi-data-on-a-64-bit-platform).</span><span class="sxs-lookup"><span data-stu-id="1d10a-135">For information about accessing the alternate registry view through WMI, see [Requesting WMI Data on a 64-bit Platform](/windows/desktop/WmiSdk/requesting-wmi-data-on-a-64-bit-platform).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d10a-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1d10a-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d10a-137">Redirector del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="1d10a-137">Registry Redirector</span></span>](registry-redirector.md)
</dt> <dt>

[<span data-ttu-id="1d10a-138">Reflection del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="1d10a-138">Registry Reflection</span></span>](registry-reflection.md)
</dt> </dl>

 

