---
title: Informazioni sui controlli degli indirizzi IP
description: Un controllo degli indirizzi IP (Internet Protocol) consente all'utente di immettere un indirizzo IP in un formato facilmente comprensibile.
ms.assetid: cf6a59fc-661c-420a-a67f-a42619946357
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6859bd31250d30bcf26d0c5fde37afeca8cc81bd
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424231"
---
# <a name="about-ip-address-controls"></a><span data-ttu-id="0b927-103">Informazioni sui controlli degli indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="0b927-103">About IP Address Controls</span></span>

<span data-ttu-id="0b927-104">Un controllo degli indirizzi IP (Internet Protocol) consente all'utente di immettere un indirizzo IP in un formato facilmente comprensibile.</span><span class="sxs-lookup"><span data-stu-id="0b927-104">An Internet Protocol (IP) address control allows the user to enter an IP address in an easily understood format.</span></span> <span data-ttu-id="0b927-105">Questo controllo consente inoltre all'applicazione di ottenere l'indirizzo in formato numerico anziché in formato testo.</span><span class="sxs-lookup"><span data-stu-id="0b927-105">This control also allows the application to obtain the address in numeric form rather than in text form.</span></span>

-   [<span data-ttu-id="0b927-106">Informazioni sui controlli degli indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="0b927-106">About IP Address Controls</span></span>](#about-ip-address-controls)
-   [<span data-ttu-id="0b927-107">Creazione di un controllo di indirizzo IP</span><span class="sxs-lookup"><span data-stu-id="0b927-107">Creating an IP Address Control</span></span>](#creating-an-ip-address-control)
-   [<span data-ttu-id="0b927-108">Un controllo indirizzo IP è un controllo di modifica?</span><span class="sxs-lookup"><span data-stu-id="0b927-108">Is an IP Address Control an Edit Control?</span></span>](#is-an-ip-address-control-an-edit-control)

## <a name="about-ip-address-controls"></a><span data-ttu-id="0b927-109">Informazioni sui controlli degli indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="0b927-109">About IP Address Controls</span></span>

<span data-ttu-id="0b927-110">Windows Internet Explorer versione 4.0 introduce il controllo indirizzo IP, un nuovo controllo simile a un controllo di modifica che consente all'utente di immettere un indirizzo numerico in formato IP (Internet Protocol).</span><span class="sxs-lookup"><span data-stu-id="0b927-110">Windows Internet Explorer Version 4.0 introduces the IP address control, a new control similar to an edit control that allows the user to enter a numeric address in Internet protocol (IP) format.</span></span> <span data-ttu-id="0b927-111">Questo formato è costituito da quattro campi a tre cifre.</span><span class="sxs-lookup"><span data-stu-id="0b927-111">This format consists of four three-digit fields.</span></span> <span data-ttu-id="0b927-112">Ogni campo viene trattato singolarmente. i numeri di campo sono in base zero e procedono da sinistra a destra, come illustrato in questa figura.</span><span class="sxs-lookup"><span data-stu-id="0b927-112">Each field is treated individually; the field numbers are zero-based and proceed from left to right as shown in this figure.</span></span>

![diagramma che mostra i valori in ognuno dei quattro campi di un controllo di indirizzo IP](images/ipa-scrn.png)

<span data-ttu-id="0b927-114">Il controllo consente di immettere solo testo numerico in ognuno dei campi.</span><span class="sxs-lookup"><span data-stu-id="0b927-114">The control allows only numeric text to be entered in each of the fields.</span></span> <span data-ttu-id="0b927-115">Dopo aver immesso tre cifre in un determinato campo, lo stato attivo della tastiera viene spostato automaticamente nel campo successivo.</span><span class="sxs-lookup"><span data-stu-id="0b927-115">Once three digits have been entered in a given field, keyboard focus is automatically moved to the next field.</span></span> <span data-ttu-id="0b927-116">Se l'applicazione non richiede la compilazione dell'intero campo, l'utente può immettere meno di tre cifre.</span><span class="sxs-lookup"><span data-stu-id="0b927-116">If filling the entire field is not required by the application, the user can enter fewer than three digits.</span></span> <span data-ttu-id="0b927-117">Ad esempio, se il campo deve contenere solo il numero 21, digitando "21" e premendo il tasto l'utente verrà visualizzato il campo successivo.</span><span class="sxs-lookup"><span data-stu-id="0b927-117">For example, if the field should only contain the number twenty-one, typing "21" and pressing the key will take the user to the next field.</span></span>

<span data-ttu-id="0b927-118">L'intervallo predefinito per ogni campo è compreso tra 0 e 255, ma l'applicazione può impostare l'intervallo su qualsiasi valore compreso tra tali limiti con il [**messaggio \_ IPM SETRANGE.**](ipm-setrange.md)</span><span class="sxs-lookup"><span data-stu-id="0b927-118">The default range for each field is 0 to 255, but the application can set the range to any values between those limits with the [**IPM\_SETRANGE**](ipm-setrange.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="0b927-119">Il controllo degli indirizzi IP viene implementato nella versione 4.71 e successive di Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="0b927-119">The IP address control is implemented in version 4.71 and later of Comctl32.dll.</span></span>

 

## <a name="creating-an-ip-address-control"></a><span data-ttu-id="0b927-120">Creazione di un controllo di indirizzo IP</span><span class="sxs-lookup"><span data-stu-id="0b927-120">Creating an IP Address Control</span></span>

<span data-ttu-id="0b927-121">Prima di creare un controllo indirizzo IP, chiamare [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) con il flag **ICC \_ INTERNET \_ CLASSES** impostato nel membro **dwICC** della [**struttura INITCOMMONCONTROLSEX.**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex)</span><span class="sxs-lookup"><span data-stu-id="0b927-121">Before creating an IP address control, call [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) with the **ICC\_INTERNET\_CLASSES** flag set in the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

<span data-ttu-id="0b927-122">Usare la [**funzione CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) per creare un controllo indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="0b927-122">Use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create an IP address control.</span></span> <span data-ttu-id="0b927-123">Il nome della classe per il controllo [**è WC \_ IPADDRESS,**](common-control-window-classes.md)definito in Commctrl.h.</span><span class="sxs-lookup"><span data-stu-id="0b927-123">The class name for the control is [**WC\_IPADDRESS**](common-control-window-classes.md), which is defined in Commctrl.h.</span></span> <span data-ttu-id="0b927-124">Non esistono stili specifici del controllo degli indirizzi IP. Tuttavia, poiché si tratta di un controllo figlio, usare lo [**stile \_ WS CHILD**](/windows/desktop/winmsg/window-styles) come minimo.</span><span class="sxs-lookup"><span data-stu-id="0b927-124">No IP address control-specific styles exist; however, because this is a child control, use the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) style as a minimum.</span></span>

## <a name="is-an-ip-address-control-an-edit-control"></a><span data-ttu-id="0b927-125">Un controllo indirizzo IP è un controllo di modifica?</span><span class="sxs-lookup"><span data-stu-id="0b927-125">Is an IP Address Control an Edit Control?</span></span>

<span data-ttu-id="0b927-126">Un controllo indirizzo IP non è un controllo di modifica e non risponde ai messaggi \_ EM.</span><span class="sxs-lookup"><span data-stu-id="0b927-126">An IP address control is not an edit control and it will not respond to EM\_ messages.</span></span> <span data-ttu-id="0b927-127">Tuttavia, invierà alla finestra del proprietario le notifiche di controllo di modifica seguenti tramite il [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)</span><span class="sxs-lookup"><span data-stu-id="0b927-127">It will, however, send the owner window the following edit control notifications through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="0b927-128">Si noti che il controllo dell'indirizzo IP invierà anche notifiche IPN \_ private tramite il messaggio WM [**\_ NOTIFY.**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="0b927-128">Note that the IP address control will also send private IPN\_ notifications through the [**WM\_NOTIFY**](wm-notify.md) message.</span></span>



|     <span data-ttu-id="0b927-129">Notifica</span><span class="sxs-lookup"><span data-stu-id="0b927-129">Notification</span></span>                              |     <span data-ttu-id="0b927-130">Motivo della notifica</span><span class="sxs-lookup"><span data-stu-id="0b927-130">Reason for notification</span></span>                                                                                                                                                                                                    |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b927-131">EN \_ SETFOCUS</span><span class="sxs-lookup"><span data-stu-id="0b927-131">EN\_SETFOCUS</span></span>](en-setfocus.md)   | <span data-ttu-id="0b927-132">Inviato quando il controllo dell'indirizzo IP ottiene lo stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="0b927-132">Sent when the IP address control gains the keyboard focus.</span></span>                                                                                                                                              |
| [<span data-ttu-id="0b927-133">EN \_ KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="0b927-133">EN\_KILLFOCUS</span></span>](en-killfocus.md) | <span data-ttu-id="0b927-134">Inviato quando il controllo dell'indirizzo IP perde lo stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="0b927-134">Sent when the IP address control loses the keyboard focus.</span></span>                                                                                                                                              |
| [<span data-ttu-id="0b927-135">MODIFICA \_ EN</span><span class="sxs-lookup"><span data-stu-id="0b927-135">EN\_CHANGE</span></span>](en-change.md)       | <span data-ttu-id="0b927-136">Inviato quando viene modificato un campo nel controllo dell'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="0b927-136">Sent when any field in the IP address control changes.</span></span> <span data-ttu-id="0b927-137">Come la [notifica EN \_ CHANGE](en-change.md) da un controllo di modifica standard, questa notifica viene ricevuta dopo l'aggiornamento della schermata.</span><span class="sxs-lookup"><span data-stu-id="0b927-137">Like the [EN\_CHANGE](en-change.md) notification from a standard edit control, this notification is received after the screen has been updated.</span></span> |



 

 

 