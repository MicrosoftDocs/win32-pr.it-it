---
title: Messaggi in Active Directory Domain Services
description: I messaggi in Active Directory Domain Services sono funzionali in Windows 2000 e Windows NT 4,0 con Service Pack 6a (SP6a) e versioni successive con DSClient.
ms.assetid: 32a4724b-3182-4521-975c-cef33afee0b2
ms.tgt_platform: multiple
keywords:
- ANNUNCIO Active Directory messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6895aee711af04778318cf42920d0b0416725205
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297723"
---
# <a name="messages-in-active-directory-domain-services"></a><span data-ttu-id="e4659-104">Messaggi in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="e4659-104">Messages in Active Directory Domain Services</span></span>

<span data-ttu-id="e4659-105">I messaggi in Active Directory Domain Services sono funzionali in Windows 2000 e Windows NT 4,0 con Service Pack 6a (SP6a) e versioni successive con DSClient.</span><span class="sxs-lookup"><span data-stu-id="e4659-105">Messages in Active Directory Domain Services are functional in Windows 2000 and Windows NT 4.0 with Service Pack 6a (SP6a) and later with DSClient.</span></span> <span data-ttu-id="e4659-106">Sono anche funzionali nelle workstation Windows 98/95 con IE 4.01 e versioni successive e DSClient.</span><span class="sxs-lookup"><span data-stu-id="e4659-106">They are also functional in Windows 98/95 workstations with IE4.01 and later and DSClient.</span></span> <span data-ttu-id="e4659-107">Se, tuttavia, le pagine delle proprietà MultiSelect vengono avviate dalla shell, il messaggio di [**\_ \_ \_ errore WM ADSPROP Notify**](wm-adsprop-notify-error.md) e le funzioni helper corrispondenti, [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) e [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) , non sono funzionali e non verranno visualizzate.</span><span class="sxs-lookup"><span data-stu-id="e4659-107">However, if multiselect property pages are launched from the shell, then the [**WM\_ADSPROP\_NOTIFY\_ERROR**](wm-adsprop-notify-error.md) message and its corresponding helper functions, [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) and [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) are not functional and will not be displayed.</span></span> <span data-ttu-id="e4659-108">Se le pagine delle proprietà MultiSelect vengono avviate all'interno di uno strumento di amministrazione, ad esempio utenti e computer di Active Directory, tutti i messaggi sono funzionali e disponibili per essere visualizzati nelle pagine delle proprietà MultiSelect.</span><span class="sxs-lookup"><span data-stu-id="e4659-108">If multiselect property pages are launched within an admin tool, for example, AD Users and Computers, then all messages are functional and available to be displayed within the multiselect property pages.</span></span>

<span data-ttu-id="e4659-109">Active Directory Domain Services utilizzare i messaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="e4659-109">Active Directory Domain Services use the following messages:</span></span>

-   [<span data-ttu-id="e4659-110">**richiesta di notifica di WM \_ ADSPROP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e4659-110">**WM\_ADSPROP\_NOTIFY\_APPLY**</span></span>](wm-adsprop-notify-apply.md)
-   [<span data-ttu-id="e4659-111">**\_ \_ modifica notifica ADSPROP \_ WM**</span><span class="sxs-lookup"><span data-stu-id="e4659-111">**WM\_ADSPROP\_NOTIFY\_CHANGE**</span></span>](wm-adsprop-notify-change.md)
-   [<span data-ttu-id="e4659-112">**\_errore di \_ notifica \_ ADSPROP di WM**</span><span class="sxs-lookup"><span data-stu-id="e4659-112">**WM\_ADSPROP\_NOTIFY\_ERROR**</span></span>](wm-adsprop-notify-error.md)
-   [<span data-ttu-id="e4659-113">**\_ \_ uscita notifica ADSPROP \_ WM**</span><span class="sxs-lookup"><span data-stu-id="e4659-113">**WM\_ADSPROP\_NOTIFY\_EXIT**</span></span>](wm-adsprop-notify-exit.md)
-   [<span data-ttu-id="e4659-114">**\_ \_ primo piano della notifica ADSPROP WM \_**</span><span class="sxs-lookup"><span data-stu-id="e4659-114">**WM\_ADSPROP\_NOTIFY\_FOREGROUND**</span></span>](wm-adsprop-notify-foreground.md)
-   [<span data-ttu-id="e4659-115">**WM \_ ADSPROP \_ Notify \_ PAGEHWND**</span><span class="sxs-lookup"><span data-stu-id="e4659-115">**WM\_ADSPROP\_NOTIFY\_PAGEHWND**</span></span>](wm-adsprop-notify-pagehwnd.md)
-   [<span data-ttu-id="e4659-116">**WM \_ ADSPROP \_ Notify \_ PAGEINIT**</span><span class="sxs-lookup"><span data-stu-id="e4659-116">**WM\_ADSPROP\_NOTIFY\_PAGEINIT**</span></span>](wm-adsprop-notify-pageinit.md)
-   [<span data-ttu-id="e4659-117">**STATO di notifica di WM \_ ADSPROP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e4659-117">**WM\_ADSPROP\_NOTIFY\_SETFOCUS**</span></span>](wm-adsprop-notify-setfocus.md)
-   [<span data-ttu-id="e4659-118">**\_ \_ creazione foglio ADSPROP \_ WM**</span><span class="sxs-lookup"><span data-stu-id="e4659-118">**WM\_ADSPROP\_SHEET\_CREATE**</span></span>](wm-adsprop-sheet-create.md)
-   [<span data-ttu-id="e4659-119">**\_notifica di \_ chiusura del foglio DSA \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="e4659-119">**WM\_DSA\_SHEET\_CLOSE\_NOTIFY**</span></span>](wm-dsa-sheet-close-notify.md)
-   [<span data-ttu-id="e4659-120">**\_ \_ \_ creazione \_ notifica foglio DSA WM**</span><span class="sxs-lookup"><span data-stu-id="e4659-120">**WM\_DSA\_SHEET\_CREATE\_NOTIFY**</span></span>](wm-dsa-sheet-create-notify.md)

 

 




