---
title: Messaggi di errore e notifiche
description: Messaggi di errore e notifiche
ms.assetid: 7f804364-d8be-4e52-ab0e-fba05bcf76ce
keywords:
- MCIWndGetError (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37e40e78c72dc378baa37b56dbb2d5718ae2d85b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046640"
---
# <a name="error-messages-and-notifications"></a><span data-ttu-id="9c592-104">Messaggi di errore e notifiche</span><span class="sxs-lookup"><span data-stu-id="9c592-104">Error Messages and Notifications</span></span>

<span data-ttu-id="9c592-105">MCIWnd USA MCI per controllare i dispositivi che riproducono e registrano i dati multimediali.</span><span class="sxs-lookup"><span data-stu-id="9c592-105">MCIWnd uses MCI to control the devices that play and record multimedia data.</span></span> <span data-ttu-id="9c592-106">In generale, MCIWnd Visualizza gli errori di MCI in una finestra di dialogo di errore.</span><span class="sxs-lookup"><span data-stu-id="9c592-106">In general, MCIWnd displays MCI errors in an error dialog box.</span></span> <span data-ttu-id="9c592-107">Un errore MCI viene generato ogni volta che un comando MCI ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="9c592-107">An MCI error is generated whenever an MCI command fails.</span></span> <span data-ttu-id="9c592-108">Ad esempio, se l'applicazione tenta di riprendere la riproduzione sospesa usando la macro [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) e il dispositivo corrente non supporta la ripresa, viene restituito un errore all'utente.</span><span class="sxs-lookup"><span data-stu-id="9c592-108">For example, if your application tries to resume paused playback by using the [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) macro and the current device does not support resume, an error is reported to the user.</span></span>

<span data-ttu-id="9c592-109">MCIWnd consente due opzioni per la gestione dei messaggi di errore:</span><span class="sxs-lookup"><span data-stu-id="9c592-109">MCIWnd allows you two choices for handling error messages:</span></span>

-   <span data-ttu-id="9c592-110">È possibile impedire che i messaggi di errore raggiungano l'utente.</span><span class="sxs-lookup"><span data-stu-id="9c592-110">You can prevent error messages from reaching the user.</span></span> <span data-ttu-id="9c592-111">Per evitare la visualizzazione di messaggi di errore MCI, specificare lo \_ stile della finestra MCIWNDF NOERRORDLG quando si crea un'istanza di una finestra MCIWnd usando la funzione [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) o [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="9c592-111">To prevent the display of MCI error messages, specify the MCIWNDF\_NOERRORDLG window style when you create an instance of an MCIWnd window by using the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) or [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span>
-   <span data-ttu-id="9c592-112">È possibile reindirizzarli all'applicazione per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9c592-112">You can redirect them to your application for display.</span></span> <span data-ttu-id="9c592-113">Per reindirizzare i messaggi di errore di MCI all'applicazione, specificare lo \_ stile della finestra MCIWNDF NOTIFYERROR quando si crea un'istanza di una finestra MCIWnd usando **MCIWndCreate** o **CreateWindowEx**.</span><span class="sxs-lookup"><span data-stu-id="9c592-113">To redirect MCI error messages to your application, specify the MCIWNDF\_NOTIFYERROR window style when you create an instance of an MCIWnd window by using **MCIWndCreate** or **CreateWindowEx**.</span></span>

<span data-ttu-id="9c592-114">Quando è abilitata la notifica degli errori, MCIWnd invia ogni messaggio di notifica ([**MCIWNDM \_ NOTIFYERROR**](mciwndm-notifyerror.md)) al gestore di messaggi principale dell'elemento padre della finestra MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="9c592-114">When error notification is enabled, MCIWnd sends each notification message ([**MCIWNDM\_NOTIFYERROR**](mciwndm-notifyerror.md)) to the main message handler of the parent of the MCIWnd window.</span></span> <span data-ttu-id="9c592-115">Per elaborare i messaggi di notifica ricevuti, l'applicazione deve disporre di un gestore di messaggi.</span><span class="sxs-lookup"><span data-stu-id="9c592-115">Your application must have a message handler to process the notification messages it receives.</span></span>

<span data-ttu-id="9c592-116">È possibile ottenere una descrizione testuale del messaggio di errore MCI più recente utilizzando la macro [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) .</span><span class="sxs-lookup"><span data-stu-id="9c592-116">You can obtain a textual description of the most recent MCI error message by using the [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) macro.</span></span> <span data-ttu-id="9c592-117">Questa macro restituisce il testo in un buffer definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9c592-117">This macro returns the text in an application-defined buffer.</span></span> <span data-ttu-id="9c592-118">Se la stringa di errore è più lunga del buffer, MCIWnd tronca la stringa.</span><span class="sxs-lookup"><span data-stu-id="9c592-118">If the error string is longer than the buffer, MCIWnd truncates the string.</span></span>

<span data-ttu-id="9c592-119">È possibile instradare tutte le notifiche a un'altra finestra usando la macro [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) .</span><span class="sxs-lookup"><span data-stu-id="9c592-119">You can route all notifications to another window by using the [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) macro.</span></span>

 

 