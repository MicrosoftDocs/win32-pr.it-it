---
title: Linee guida per testo e carattere internazionali
description: Linee guida per testo e carattere internazionali
ms.assetid: 0540C9AD-8774-4F0F-B013-48C3EAE59BF2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2f9d94c53e4db45666d28a7c23a0e883043ba27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399043"
---
# <a name="international-text-and-font-guidance"></a><span data-ttu-id="ac4b6-103">Linee guida per testo e carattere internazionali</span><span class="sxs-lookup"><span data-stu-id="ac4b6-103">International text and font guidance</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="ac4b6-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="ac4b6-104">Affected Platforms</span></span>

<dl> <span data-ttu-id="ac4b6-105">Client-Windows 8 \| Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ac4b6-105">Clients - Windows 8 \| Windows 8.1</span></span>  
<span data-ttu-id="ac4b6-106">Server-Windows Server 2012 \| Windows server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ac4b6-106">Servers - Windows Server 2012 \| Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="ac4b6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac4b6-107">Description</span></span>

<span data-ttu-id="ac4b6-108">Dal momento precedente a Windows 2000, è stato aggiunto il supporto per la visualizzazione di testo per i nuovi script in ogni versione principale di Windows.</span><span class="sxs-lookup"><span data-stu-id="ac4b6-108">Since before Windows 2000, text-display support for new scripts has been added in each major release of Windows.</span></span> <span data-ttu-id="ac4b6-109">Per informazioni sulle modifiche apportate in ogni versione principale, vedere l'articolo [relativo al supporto dello script e dei tipi di carattere per Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx) in [go Global Development Center](https://msdn.microsoft.com/goglobal/default).</span><span class="sxs-lookup"><span data-stu-id="ac4b6-109">You can find descriptions of the changes made in each major release in the [Script and Font Support for Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx) article at the [Go Global Development Center](https://msdn.microsoft.com/goglobal/default).</span></span>

<span data-ttu-id="ac4b6-110">Si noti che il supporto per uno script può richiedere alcune modifiche ai componenti dello stack di testo e alle modifiche ai tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="ac4b6-110">Note that support for a script may require certain changes to text stack components as well as changes to fonts.</span></span> <span data-ttu-id="ac4b6-111">Il sistema operativo Windows include molti componenti dello stack di testo: DirectWrite, GDI, Uniscribe, GDI+, WPF, RichEdit, ComCtl32 e altri.</span><span class="sxs-lookup"><span data-stu-id="ac4b6-111">The Windows operating system has many text stack components: DirectWrite, GDI, Uniscribe, GDI+, WPF, RichEdit, ComCtl32, and others.</span></span> <span data-ttu-id="ac4b6-112">Le informazioni fornite riguardano principalmente GDI e DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="ac4b6-112">The information provided pertains primarily to GDI and DirectWrite.</span></span> <span data-ttu-id="ac4b6-113">È inoltre generalmente applicabile ai Framework dell'interfaccia utente, ad esempio RichEdit o l'agente di rendering MSHTML usato per le app di Windows 8 Store e per il rendering del contenuto Web, sebbene tali componenti possano presentare alcune differenze.</span><span class="sxs-lookup"><span data-stu-id="ac4b6-113">It is also generally applicable to UI frameworks such as RichEdit or the MSHTML rendering agent used for Windows 8 Store apps and for rendering web content, though those components may exhibit certain differences.</span></span>

## <a name="best-practices"></a><span data-ttu-id="ac4b6-114">Procedure consigliate</span><span class="sxs-lookup"><span data-stu-id="ac4b6-114">Best Practices</span></span>

<span data-ttu-id="ac4b6-115">**Linee guida per le tipografie per sviluppatori**</span><span class="sxs-lookup"><span data-stu-id="ac4b6-115">**Typography guidance for developers**</span></span>

<span data-ttu-id="ac4b6-116">Tipografia è alla base del linguaggio di progettazione Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ac4b6-116">Typography is at the heart of the Microsoft design language.</span></span> <span data-ttu-id="ac4b6-117">Ognuno dei principi di progettazione Microsoft rafforza l'importanza della tipografia.</span><span class="sxs-lookup"><span data-stu-id="ac4b6-117">Each of the Microsoft design principles reinforces the importance of typography.</span></span> <span data-ttu-id="ac4b6-118">Per la prima volta, gli sviluppatori di app hanno un set di Framework che supportano funzionalità tipografiche avanzate.</span><span class="sxs-lookup"><span data-stu-id="ac4b6-118">For the first time, app developers have a set of frameworks that support advanced typographic features.</span></span> <span data-ttu-id="ac4b6-119">Per informazioni su come usare JavaScript e HTML per visualizzare e modificare il testo nelle app di Windows Store, vedere [visualizzazione e modifica del testo](/previous-versions/windows/apps/hh465442(v=win.10)) .</span><span class="sxs-lookup"><span data-stu-id="ac4b6-119">Go to [Displaying and editing text](/previous-versions/windows/apps/hh465442(v=win.10)) for information about how to use JavaScript and HTML to display and edit text in Windows Store apps.</span></span>

<span data-ttu-id="ac4b6-120">**Metriche dei tipi di carattere**</span><span class="sxs-lookup"><span data-stu-id="ac4b6-120">**Font metrics**</span></span>

<span data-ttu-id="ac4b6-121">Le metriche dei tipi di carattere sono un'area di particolare importanza per gli sviluppatori di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="ac4b6-121">Font metrics are an area of particular importance to application developers.</span></span> <span data-ttu-id="ac4b6-122">I file del tipo di carattere contengono diversi valori correlati alle metriche verticali e orizzontali.</span><span class="sxs-lookup"><span data-stu-id="ac4b6-122">Font files contain various values related to vertical and horizontal metrics.</span></span> <span data-ttu-id="ac4b6-123">Questi valori sono documentati nella [specifica OpenType](https://www.microsoft.com/typography/otspec/) e vengono esposti tramite un'ampia gamma di API trovate nella [ \_ struttura di \_ metrica del tipo di carattere DWrite](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) e nella [struttura TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica).</span><span class="sxs-lookup"><span data-stu-id="ac4b6-123">These values are documented in the [OpenType specification](https://www.microsoft.com/typography/otspec/) and these are exposed via a variety of APIs found at [DWRITE\_FONT\_METRICS structure](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) and at [TEXTMETRIC Structure](/windows/win32/api/wingdi/ns-wingdi-textmetrica).</span></span>

## <a name="resources"></a><span data-ttu-id="ac4b6-124">Risorse</span><span class="sxs-lookup"><span data-stu-id="ac4b6-124">Resources</span></span>

-   [<span data-ttu-id="ac4b6-125">Supporto dello script e dei tipi di carattere per Windows</span><span class="sxs-lookup"><span data-stu-id="ac4b6-125">Script and Font Support for Windows</span></span>](https://msdn.microsoft.com/goglobal/bb688099.aspx)
-   [<span data-ttu-id="ac4b6-126">Vai al centro per sviluppatori globali</span><span class="sxs-lookup"><span data-stu-id="ac4b6-126">Go Global Development Center</span></span>](https://msdn.microsoft.com/goglobal/default)
-   <span data-ttu-id="ac4b6-127">[Visualizzazione e modifica di testo](/previous-versions/windows/apps/hh465442(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="ac4b6-127">[Displaying and editing text](/previous-versions/windows/apps/hh465442(v=win.10))</span></span>
-   [<span data-ttu-id="ac4b6-128">Specifica OpenType</span><span class="sxs-lookup"><span data-stu-id="ac4b6-128">OpenType specification</span></span>](https://www.microsoft.com/typography/otspec/)
-   [<span data-ttu-id="ac4b6-129">\_Struttura della metrica del tipo di carattere DWrite \_</span><span class="sxs-lookup"><span data-stu-id="ac4b6-129">DWRITE\_FONT\_METRICS structure</span></span>](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)
-   [<span data-ttu-id="ac4b6-130">Struttura TEXTMETRIC</span><span class="sxs-lookup"><span data-stu-id="ac4b6-130">TEXTMETRIC Structure</span></span>](/windows/win32/api/wingdi/ns-wingdi-textmetrica)

 

 