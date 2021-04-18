---
description: In alcuni casi potrebbe essere necessario determinare se l'applicazione è in esecuzione in un Tablet PC perché si desidera che le applicazioni possano sfruttare le funzionalità intrinseche di input penna, riconoscimento e penna.
ms.assetid: 86a3eddb-6541-4b73-b2ca-6adedad1a1e5
title: Determinare se un PC è un Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c793d5531d6091d4bce73d99bfa32d100c2b9304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316858"
---
# <a name="determining-whether-a-pc-is-a-tablet-pc"></a><span data-ttu-id="dc99e-103">Determinare se un PC è un Tablet PC</span><span class="sxs-lookup"><span data-stu-id="dc99e-103">Determining Whether a PC is a Tablet PC</span></span>

<span data-ttu-id="dc99e-104">In alcuni casi potrebbe essere necessario determinare se l'applicazione è in esecuzione in un Tablet PC perché si desidera che le applicazioni possano sfruttare le funzionalità intrinseche di input penna, riconoscimento e penna.</span><span class="sxs-lookup"><span data-stu-id="dc99e-104">You may occasionally need to determine whether your application is running on a Tablet PC because you may want your applications to take advantage of inherent ink, recognition, and pen capabilities.</span></span> <span data-ttu-id="dc99e-105">Per determinare se l'applicazione ha accesso alle funzionalità di Tablet PC, è possibile usare la chiamata all'API Windows GetSystemMetrics () come descritto in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="dc99e-105">To help you determine whether your application has access to the Tablet PC features, you can use the GetSystemMetrics() Windows API call as described in this topic.</span></span>

## <a name="client-side-applications"></a><span data-ttu-id="dc99e-106">Applicazioni Client-Side</span><span class="sxs-lookup"><span data-stu-id="dc99e-106">Client-Side Applications</span></span>

<span data-ttu-id="dc99e-107">È possibile utilizzare le tecniche seguenti per determinare se il codice è in esecuzione in un Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="dc99e-107">You can use the following techniques to determine whether your code is running on a Tablet PC.</span></span>

-   [<span data-ttu-id="dc99e-108">Uso di GetSystemMetrics (SM \_ TABLETPC)</span><span class="sxs-lookup"><span data-stu-id="dc99e-108">Using GetSystemMetrics (SM\_TABLETPC)</span></span>](/windows)
-   [<span data-ttu-id="dc99e-109">Uso della presenza di file binari della piattaforma Tablet</span><span class="sxs-lookup"><span data-stu-id="dc99e-109">Using the Presence of Tablet Platform Binaries</span></span>](#using-the-presence-of-tablet-platform-binaries)
-   [<span data-ttu-id="dc99e-110">Applicazioni basate sul Web</span><span class="sxs-lookup"><span data-stu-id="dc99e-110">Web-Based Applications</span></span>](#web-based-applications)

### <a name="using-getsystemmetrics-sm_tabletpc"></a><span data-ttu-id="dc99e-111">Uso di GetSystemMetrics (SM \_ TABLETPC)</span><span class="sxs-lookup"><span data-stu-id="dc99e-111">Using GetSystemMetrics (SM\_TABLETPC)</span></span>

### <a name="windows-xp-tablet-pc-edition"></a><span data-ttu-id="dc99e-112">Windows XP Tablet PC Edition</span><span class="sxs-lookup"><span data-stu-id="dc99e-112">Windows XP Tablet PC Edition</span></span>

<span data-ttu-id="dc99e-113">In Microsoft Windows XP Tablet PC Edition utilizzare la funzione GetSystemMetrics (SM \_ TABLETPC) per determinare se un computer è un Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="dc99e-113">In Microsoft Windows XP Tablet PC Edition, use the GetSystemMetrics(SM\_TABLETPC) function to determine whether a computer is a Tablet PC.</span></span> <span data-ttu-id="dc99e-114">GetSystemMetrics (SM \_ TABLETPC) è progettato per restituire true in un computer in cui è in esecuzione Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="dc99e-114">GetSystemMetrics(SM\_TABLETPC) is designed to return TRUE on a computer running Windows XP Tablet PC Edition.</span></span>

### <a name="windows-vista"></a><span data-ttu-id="dc99e-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc99e-115">Windows Vista</span></span>

<span data-ttu-id="dc99e-116">In Windows Vista non è più disponibile un Tablet PC SDK distinto.</span><span class="sxs-lookup"><span data-stu-id="dc99e-116">In Windows Vista, there is no longer a distinct Tablet PC SDK.</span></span> <span data-ttu-id="dc99e-117">Il Windows SDK ora contiene una sezione denominata "Tablet PC and Touch Technology" e la logica di GetSystemMetrics (SM \_ TABLETPC) è stata modificata per riflettere questo problema.</span><span class="sxs-lookup"><span data-stu-id="dc99e-117">The Windows SDK now contains a section called "Tablet PC and Touch Technology" and the logic of GetSystemMetrics(SM\_TABLETPC) has been changed to reflect this.</span></span> <span data-ttu-id="dc99e-118">GetSystemMetrics (SM \_ TABLETPC) restituisce ora true se si verificano tutte le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="dc99e-118">GetSystemMetrics(SM\_TABLETPC) now returns true if all of the following are true:</span></span>

-   <span data-ttu-id="dc99e-119">Nel sistema è presente un digitalizzatore integrato, ovvero Pen o touch.</span><span class="sxs-lookup"><span data-stu-id="dc99e-119">There is an integrated digitizer, either pen or touch, on the system.</span></span>
-   <span data-ttu-id="dc99e-120">Il componente facoltativo di Tablet PC è installato.</span><span class="sxs-lookup"><span data-stu-id="dc99e-120">The Tablet PC optional component is installed.</span></span> <span data-ttu-id="dc99e-121">Questo componente contiene funzionalità come il pannello input penna di Tablet PC e Windows Journal.</span><span class="sxs-lookup"><span data-stu-id="dc99e-121">This component contains features such as Tablet PC Input Panel and Windows Journal.</span></span>
-   <span data-ttu-id="dc99e-122">Il computer dispone di una licenza per l'utilizzo del componente facoltativo.</span><span class="sxs-lookup"><span data-stu-id="dc99e-122">The computer is licensed to use the optional component.</span></span> <span data-ttu-id="dc99e-123">Le versioni Premium di Windows Vista, ad esempio Windows Vista Home Premium, Windows Vista Small Business, Windows Vista Professional, Windows Vista Enterprise e Windows Vista Ultimate, sono concesse in licenza per l'uso del componente facoltativo.</span><span class="sxs-lookup"><span data-stu-id="dc99e-123">Premium versions of Windows Vista—such as Windows Vista Home Premium, Windows Vista Small Business, Windows Vista Professional, Windows Vista Enterprise, and Windows Vista Ultimate—are licensed to use the optional component.</span></span>
-   <span data-ttu-id="dc99e-124">Il servizio di input di Tablet PC è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="dc99e-124">Tablet PC Input Service is running.</span></span> <span data-ttu-id="dc99e-125">Il servizio di input di Tablet PC è un nuovo servizio di Windows Vista che controlla l'input di Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="dc99e-125">Tablet PC Input Service is a new service for Windows Vista that controls Tablet PC input.</span></span>

<span data-ttu-id="dc99e-126">Con questa maggiore precisione, GetSystemMetrics (SM \_ TABLETPC) continua a essere il metodo consigliato per determinare se un computer che esegue Windows Vista è un Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="dc99e-126">With this increased accuracy, GetSystemMetrics(SM\_TABLETPC) continues to be the recommended way to determine whether a computer running Windows Vista is a Tablet PC.</span></span>

### <a name="using-the-presence-of-tablet-platform-binaries"></a><span data-ttu-id="dc99e-127">Uso della presenza di file binari della piattaforma Tablet</span><span class="sxs-lookup"><span data-stu-id="dc99e-127">Using the Presence of Tablet Platform Binaries</span></span>

<span data-ttu-id="dc99e-128">In Windows XP Tablet PC Edition e Windows Vista è possibile cercare la presenza dei file binari di input penna, ad esempio inkobj.dll e Microsoft.Ink.dll, e utilizzare le funzionalità supportate, se presenti.</span><span class="sxs-lookup"><span data-stu-id="dc99e-128">In both Windows XP Tablet PC Edition and Windows Vista, you can search for the presence of the ink binaries—such as inkobj.dll and Microsoft.Ink.dll—and use their supported functionality if they are present.</span></span>

<span data-ttu-id="dc99e-129">In Windows Vista, per impostazione predefinita, i file binari della piattaforma Tablet PC vengono installati in tutte le versioni client.</span><span class="sxs-lookup"><span data-stu-id="dc99e-129">In Windows Vista, the Tablet PC Platform binaries are installed on all client versions by default.</span></span> <span data-ttu-id="dc99e-130">Le funzionalità di input e Inking sono disponibili in tali versioni.</span><span class="sxs-lookup"><span data-stu-id="dc99e-130">Input and inking functionality are available on those versions.</span></span> <span data-ttu-id="dc99e-131">Il riconoscimento è disponibile solo nelle versioni Premium di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dc99e-131">Recognition is available only in premium versions of Windows Vista.</span></span>

### <a name="web-based-applications"></a><span data-ttu-id="dc99e-132">Applicazioni Web-Based</span><span class="sxs-lookup"><span data-stu-id="dc99e-132">Web-Based Applications</span></span>

<span data-ttu-id="dc99e-133">In Windows Vista, la stringa dell'agente utente segnalata da Internet Explorer include "Tablet PC 2,0" Se, in base a GetSystemMetrics (SM \_ TABLETPC), il dispositivo è un Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="dc99e-133">In Windows Vista, the user-agent string reported by Internet Explorer includes "Tablet PC 2.0" if, according to GetSystemMetrics(SM\_TABLETPC), the device is a Tablet PC.</span></span>

<span data-ttu-id="dc99e-134">In Windows XP Tablet PC Edition 2005, la stringa dell'agente utente include Tablet PC 1,7.</span><span class="sxs-lookup"><span data-stu-id="dc99e-134">In Windows XP Tablet PC Edition 2005, the user-agent string includes Tablet PC 1.7.</span></span> <span data-ttu-id="dc99e-135">La stringa dell'agente utente ha un aspetto simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="dc99e-135">The user-agent string looks something like the following:</span></span>

`Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1; .NET CLR 1.0.3705; Tablet PC 2.0)`

<span data-ttu-id="dc99e-136">Utilizzare questo valore per determinare se il computer client è un Tablet PC e supporta i controlli Inking basati sul Web.</span><span class="sxs-lookup"><span data-stu-id="dc99e-136">Use this value to determine whether the client computer is a Tablet PC and supports Web-based inking controls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc99e-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dc99e-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc99e-138">**GetSystemMetrics**</span><span class="sxs-lookup"><span data-stu-id="dc99e-138">**GetSystemMetrics**</span></span>](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> </dl>

 

 
