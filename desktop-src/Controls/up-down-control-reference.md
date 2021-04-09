---
title: Controllo Up-Down
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli di scorrimento.
ms.assetid: 48c6b4bd-65b4-4388-959e-efffa7658274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8364eb44ee01e27439c82d1d77e674bfb9e3165
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044551"
---
# <a name="up-down-control"></a><span data-ttu-id="4367a-103">Controllo Up-Down</span><span class="sxs-lookup"><span data-stu-id="4367a-103">Up-Down Control</span></span>

<span data-ttu-id="4367a-104">Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="4367a-104">This section contains information about the programming elements used with up-down controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="4367a-105">Cenni preliminari</span><span class="sxs-lookup"><span data-stu-id="4367a-105">Overviews</span></span>



| <span data-ttu-id="4367a-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="4367a-106">Topic</span></span>                                    | <span data-ttu-id="4367a-107">Contenuto</span><span class="sxs-lookup"><span data-stu-id="4367a-107">Contents</span></span>                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4367a-108">Controlli di scorrimento</span><span class="sxs-lookup"><span data-stu-id="4367a-108">Up-Down Controls</span></span>](up-down-controls.md) | <span data-ttu-id="4367a-109">Un controllo di scorrimento è una coppia di pulsanti freccia su cui l'utente può fare clic per incrementare o decrementare un valore, ad esempio una posizione di scorrimento o un numero visualizzato in un controllo complementare (chiamato finestra di Buddy).</span><span class="sxs-lookup"><span data-stu-id="4367a-109">An up-down control is a pair of arrow buttons that the user can click to increment or decrement a value, such as a scroll position or a number displayed in a companion control (called a buddy window).</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="4367a-110">Funzioni</span><span class="sxs-lookup"><span data-stu-id="4367a-110">Functions</span></span>



| <span data-ttu-id="4367a-111">Argomento</span><span class="sxs-lookup"><span data-stu-id="4367a-111">Topic</span></span>                                              | <span data-ttu-id="4367a-112">Contenuto</span><span class="sxs-lookup"><span data-stu-id="4367a-112">Contents</span></span>                                                                                                                                                |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4367a-113">**CreateUpDownControl**</span><span class="sxs-lookup"><span data-stu-id="4367a-113">**CreateUpDownControl**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-createupdowncontrol) | <span data-ttu-id="4367a-114">Crea un controllo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="4367a-114">Creates an up-down control.</span></span> <span data-ttu-id="4367a-115">Nota: questa funzione è obsoleta.</span><span class="sxs-lookup"><span data-stu-id="4367a-115">Note: This function is obsolete.</span></span> <span data-ttu-id="4367a-116">Si tratta di una funzione a 16 bit e non è in grado di gestire valori di bit 32 per l'intervallo e la posizione.</span><span class="sxs-lookup"><span data-stu-id="4367a-116">It is a 16 bit function and cannot handle 32 bit values for range and position.</span></span><br/> |



 

### <a name="messages"></a><span data-ttu-id="4367a-117">Messaggi</span><span class="sxs-lookup"><span data-stu-id="4367a-117">Messages</span></span>



| <span data-ttu-id="4367a-118">Argomento</span><span class="sxs-lookup"><span data-stu-id="4367a-118">Topic</span></span>                                                 | <span data-ttu-id="4367a-119">Contenuto</span><span class="sxs-lookup"><span data-stu-id="4367a-119">Contents</span></span>                                                                                                                                                                                                                               |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4367a-120">**\_GETACCEL UDM**</span><span class="sxs-lookup"><span data-stu-id="4367a-120">**UDM\_GETACCEL**</span></span>](udm-getaccel.md)                 | <span data-ttu-id="4367a-121">Recupera le informazioni di accelerazione per un controllo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="4367a-121">Retrieves acceleration information for an up-down control.</span></span> <br/>                                                                                                                                                                 |
| [<span data-ttu-id="4367a-122">**UDM \_ GETbase**</span><span class="sxs-lookup"><span data-stu-id="4367a-122">**UDM\_GETBASE**</span></span>](udm-getbase.md)                   | <span data-ttu-id="4367a-123">Recupera la base radice corrente, ovvero in base 10 o 16, per un controllo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="4367a-123">Retrieves the current radix base (that is, either base 10 or 16) for an up-down control.</span></span> <br/>                                                                                                                                   |
| [<span data-ttu-id="4367a-124">**UDM \_ GETbuddy**</span><span class="sxs-lookup"><span data-stu-id="4367a-124">**UDM\_GETBUDDY**</span></span>](udm-getbuddy.md)                 | <span data-ttu-id="4367a-125">Recupera l'handle per la finestra Buddy corrente.</span><span class="sxs-lookup"><span data-stu-id="4367a-125">Retrieves the handle to the current buddy window.</span></span> <br/>                                                                                                                                                                          |
| [<span data-ttu-id="4367a-126">**\_GETPOS UDM**</span><span class="sxs-lookup"><span data-stu-id="4367a-126">**UDM\_GETPOS**</span></span>](udm-getpos.md)                     | <span data-ttu-id="4367a-127">Recupera la posizione corrente di un controllo di scorrimento con precisione a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="4367a-127">Retrieves the current position of an up-down control with 16-bit precision.</span></span> <br/>                                                                                                                                                |
| [<span data-ttu-id="4367a-128">**\_GETPOS32 UDM**</span><span class="sxs-lookup"><span data-stu-id="4367a-128">**UDM\_GETPOS32**</span></span>](udm-getpos32.md)                 | <span data-ttu-id="4367a-129">Restituisce la posizione a 32 bit di un controllo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="4367a-129">Returns the 32-bit position of an up-down control.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="4367a-130">**UDM \_ GETrange**</span><span class="sxs-lookup"><span data-stu-id="4367a-130">**UDM\_GETRANGE**</span></span>](udm-getrange.md)                 | <span data-ttu-id="4367a-131">Recupera le posizioni minime e massime (intervallo) per un controllo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="4367a-131">Retrieves the minimum and maximum positions (range) for an up-down control.</span></span> <br/>                                                                                                                                                |
| [<span data-ttu-id="4367a-132">**\_GETRANGE32 UDM**</span><span class="sxs-lookup"><span data-stu-id="4367a-132">**UDM\_GETRANGE32**</span></span>](udm-getrange32.md)             | <span data-ttu-id="4367a-133">Recupera l'intervallo di 32 bit di un controllo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="4367a-133">Retrieves the 32-bit range of an up-down control.</span></span> <br/>                                                                                                                                                                          |
| [<span data-ttu-id="4367a-134">**\_GETUNICODEFORMAT UDM**</span><span class="sxs-lookup"><span data-stu-id="4367a-134">**UDM\_GETUNICODEFORMAT**</span></span>](udm-getunicodeformat.md) | <span data-ttu-id="4367a-135">Recupera il flag del formato carattere Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="4367a-135">Retrieves the Unicode character format flag for the control.</span></span> <br/>                                                                                                                                                               |
| [<span data-ttu-id="4367a-136">**\_SETACCEL UDM**</span><span class="sxs-lookup"><span data-stu-id="4367a-136">**UDM\_SETACCEL**</span></span>](udm-setaccel.md)                 | <span data-ttu-id="4367a-137">Imposta l'accelerazione per un controllo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="4367a-137">Sets the acceleration for an up-down control.</span></span> <br/>                                                                                                                                                                              |
| [<span data-ttu-id="4367a-138">**UDM di \_ base**</span><span class="sxs-lookup"><span data-stu-id="4367a-138">**UDM\_SETBASE**</span></span>](udm-setbase.md)                   | <span data-ttu-id="4367a-139">Imposta la base radice per un controllo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="4367a-139">Sets the radix base for an up-down control.</span></span> <span data-ttu-id="4367a-140">Il valore di base determina se la finestra Buddy Visualizza numeri in cifre decimali o esadecimali.</span><span class="sxs-lookup"><span data-stu-id="4367a-140">The base value determines whether the buddy window displays numbers in decimal or hexadecimal digits.</span></span> <span data-ttu-id="4367a-141">I numeri esadecimali sono sempre senza segno e i numeri decimali sono firmati.</span><span class="sxs-lookup"><span data-stu-id="4367a-141">Hexadecimal numbers are always unsigned, and decimal numbers are signed.</span></span> <br/> |
| [<span data-ttu-id="4367a-142">**UDM \_ SEbuddy**</span><span class="sxs-lookup"><span data-stu-id="4367a-142">**UDM\_SETBUDDY**</span></span>](udm-setbuddy.md)                 | <span data-ttu-id="4367a-143">Imposta la finestra buddy per un controllo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="4367a-143">Sets the buddy window for an up-down control.</span></span> <br/>                                                                                                                                                                              |
| [<span data-ttu-id="4367a-144">**\_SETPOS UDM**</span><span class="sxs-lookup"><span data-stu-id="4367a-144">**UDM\_SETPOS**</span></span>](udm-setpos.md)                     | <span data-ttu-id="4367a-145">Imposta la posizione corrente per un controllo di scorrimento con precisione a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="4367a-145">Sets the current position for an up-down control with 16-bit precision.</span></span> <br/>                                                                                                                                                    |
| [<span data-ttu-id="4367a-146">**\_SETPOS32 UDM**</span><span class="sxs-lookup"><span data-stu-id="4367a-146">**UDM\_SETPOS32**</span></span>](udm-setpos32.md)                 | <span data-ttu-id="4367a-147">Imposta la posizione di un controllo di scorrimento con precisione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="4367a-147">Sets the position of an up-down control with 32-bit precision.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="4367a-148">**\_SEtrange UDM**</span><span class="sxs-lookup"><span data-stu-id="4367a-148">**UDM\_SETRANGE**</span></span>](udm-setrange.md)                 | <span data-ttu-id="4367a-149">Imposta le posizioni minime e massime (intervallo) per un controllo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="4367a-149">Sets the minimum and maximum positions (range) for an up-down control.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="4367a-150">**\_SETRANGE32 UDM**</span><span class="sxs-lookup"><span data-stu-id="4367a-150">**UDM\_SETRANGE32**</span></span>](udm-setrange32.md)             | <span data-ttu-id="4367a-151">Imposta l'intervallo di 32 bit di un controllo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="4367a-151">Sets the 32-bit range of an up-down control.</span></span> <br/>                                                                                                                                                                               |
| [<span data-ttu-id="4367a-152">**\_SETUNICODEFORMAT UDM**</span><span class="sxs-lookup"><span data-stu-id="4367a-152">**UDM\_SETUNICODEFORMAT**</span></span>](udm-setunicodeformat.md) | <span data-ttu-id="4367a-153">Imposta il flag di formato carattere Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="4367a-153">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="4367a-154">Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover ricreare il controllo.</span><span class="sxs-lookup"><span data-stu-id="4367a-154">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <br/>                                   |



 

### <a name="notifications"></a><span data-ttu-id="4367a-155">Notifiche</span><span class="sxs-lookup"><span data-stu-id="4367a-155">Notifications</span></span>



| <span data-ttu-id="4367a-156">Argomento</span><span class="sxs-lookup"><span data-stu-id="4367a-156">Topic</span></span>                                                            | <span data-ttu-id="4367a-157">Contenuto</span><span class="sxs-lookup"><span data-stu-id="4367a-157">Contents</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4367a-158">NM \_ RELEASEDCAPTURE (Down)</span><span class="sxs-lookup"><span data-stu-id="4367a-158">NM\_RELEASEDCAPTURE (up-down)</span></span>](nm-releasedcapture-up-down-.md) | <span data-ttu-id="4367a-159">Notifica alla finestra padre di un controllo di scorrimento che il controllo sta rilasciando l'acquisizione del mouse.</span><span class="sxs-lookup"><span data-stu-id="4367a-159">Notifies an up-down control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="4367a-160">Questa notifica viene inviata sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="4367a-160">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/>                                                                                                                                                                       |
| [<span data-ttu-id="4367a-161">\_DELTAPOS UDN</span><span class="sxs-lookup"><span data-stu-id="4367a-161">UDN\_DELTAPOS</span></span>](udn-deltapos.md)                                | <span data-ttu-id="4367a-162">Inviato dal sistema operativo alla finestra padre di un controllo di scorrimento quando la posizione del controllo sta per essere modificata.</span><span class="sxs-lookup"><span data-stu-id="4367a-162">Sent by the operating system to the parent window of an up-down control when the position of the control is about to change.</span></span> <span data-ttu-id="4367a-163">Questo errore si verifica quando l'utente richiede una modifica nel valore premendo la freccia su o giù del controllo.</span><span class="sxs-lookup"><span data-stu-id="4367a-163">This happens when the user requests a change in the value by pressing the control's up or down arrow.</span></span> <span data-ttu-id="4367a-164">Il messaggio [UDN \_ DELTAPOS](udn-deltapos.md) viene inviato sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="4367a-164">The [UDN\_DELTAPOS](udn-deltapos.md) message is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/> |



 

### <a name="structures"></a><span data-ttu-id="4367a-165">Strutture</span><span class="sxs-lookup"><span data-stu-id="4367a-165">Structures</span></span>



| <span data-ttu-id="4367a-166">Argomento</span><span class="sxs-lookup"><span data-stu-id="4367a-166">Topic</span></span>                        | <span data-ttu-id="4367a-167">Contenuto</span><span class="sxs-lookup"><span data-stu-id="4367a-167">Contents</span></span>                                                                                                                                          |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4367a-168">**NMUPDOWN**</span><span class="sxs-lookup"><span data-stu-id="4367a-168">**NMUPDOWN**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmupdown) | <span data-ttu-id="4367a-169">Contiene informazioni specifiche per i messaggi di notifica del controllo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="4367a-169">Contains information specific to up-down control notification messages.</span></span> <span data-ttu-id="4367a-170">È identica a e sostituisce la struttura **a \_ discesa Nm** .</span><span class="sxs-lookup"><span data-stu-id="4367a-170">It is identical to and replaces the **NM\_UPDOWN** structure.</span></span> <br/> |
| [<span data-ttu-id="4367a-171">**UDACCEL**</span><span class="sxs-lookup"><span data-stu-id="4367a-171">**UDACCEL**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-udaccel)   | <span data-ttu-id="4367a-172">Contiene informazioni sull'accelerazione per un controllo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="4367a-172">Contains acceleration information for an up-down control.</span></span> <br/>                                                                             |



 

### <a name="constants"></a><span data-ttu-id="4367a-173">Costanti</span><span class="sxs-lookup"><span data-stu-id="4367a-173">Constants</span></span>



| <span data-ttu-id="4367a-174">Argomento</span><span class="sxs-lookup"><span data-stu-id="4367a-174">Topic</span></span>                                                | <span data-ttu-id="4367a-175">Contenuto</span><span class="sxs-lookup"><span data-stu-id="4367a-175">Contents</span></span>                                                                      |
|------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="4367a-176">Stili di controllo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="4367a-176">Up-Down Control Styles</span></span>](up-down-control-styles.md) | <span data-ttu-id="4367a-177">Questa sezione elenca gli stili usati per la creazione di controlli di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="4367a-177">This section lists the styles used when creating up-down controls.</span></span><br/> |



 

 

 





