---
title: Controllo indirizzo IP
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli degli indirizzi IP.
ms.assetid: vs|controls|~\controls\ipaddress\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c80fc87a12ce49038f4c1836e684fa0f8895bd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471070"
---
# <a name="ip-address-control"></a><span data-ttu-id="45d00-103">Controllo indirizzo IP</span><span class="sxs-lookup"><span data-stu-id="45d00-103">IP Address Control</span></span>

<span data-ttu-id="45d00-104">Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli degli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="45d00-104">This section contains information about the programming elements used with IP address controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="45d00-105">Cenni preliminari</span><span class="sxs-lookup"><span data-stu-id="45d00-105">Overviews</span></span>



| <span data-ttu-id="45d00-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="45d00-106">Topic</span></span>                                          | <span data-ttu-id="45d00-107">Contenuto</span><span class="sxs-lookup"><span data-stu-id="45d00-107">Contents</span></span>                                                                                                                    |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45d00-108">Controlli degli indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="45d00-108">IP Address Controls</span></span>](ip-address-controls.md) | <span data-ttu-id="45d00-109">Un controllo degli indirizzi IP (Internet Protocol) consente all'utente di immettere un indirizzo IP in un formato facilmente comprensibile.</span><span class="sxs-lookup"><span data-stu-id="45d00-109">An Internet Protocol (IP) address control allows the user to enter an IP address in an easily understood format.</span></span><br/> |



 

### <a name="macros"></a><span data-ttu-id="45d00-110">Macro</span><span class="sxs-lookup"><span data-stu-id="45d00-110">Macros</span></span>



| <span data-ttu-id="45d00-111">Argomento</span><span class="sxs-lookup"><span data-stu-id="45d00-111">Topic</span></span>                                         | <span data-ttu-id="45d00-112">Contenuto</span><span class="sxs-lookup"><span data-stu-id="45d00-112">Contents</span></span>                                                                                                                              |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45d00-113">**PRIMA \_ IPAddress**</span><span class="sxs-lookup"><span data-stu-id="45d00-113">**FIRST\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress)   | <span data-ttu-id="45d00-114">Estrae il valore del campo 0 da un indirizzo IP compresso recuperato con il messaggio [**IPM \_ GetAddress**](ipm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="45d00-114">Extracts the field 0 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |
| [<span data-ttu-id="45d00-115">**QUARTO \_ indirizzo IP**</span><span class="sxs-lookup"><span data-stu-id="45d00-115">**FOURTH\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) | <span data-ttu-id="45d00-116">Estrae il valore del campo 3 da un indirizzo IP compresso recuperato con il messaggio [**IPM \_ GetAddress**](ipm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="45d00-116">Extracts the field 3 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |
| [<span data-ttu-id="45d00-117">**MAKEIPADDRESS**</span><span class="sxs-lookup"><span data-stu-id="45d00-117">**MAKEIPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress)        | <span data-ttu-id="45d00-118">Comprime quattro valori di byte in un singolo LPARAM adatto per l'utilizzo con il messaggio di [**\_ Indirizzo IPM**](ipm-setaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="45d00-118">Packs four byte-values into a single LPARAM suitable for use with the [**IPM\_SETADDRESS**](ipm-setaddress.md) message.</span></span> <br/>  |
| [<span data-ttu-id="45d00-119">**MAKEIPRANGE**</span><span class="sxs-lookup"><span data-stu-id="45d00-119">**MAKEIPRANGE**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange)            | <span data-ttu-id="45d00-120">Comprime due valori di byte in un singolo LPARAM adatto per l'uso con il messaggio di [**\_ SetRange IPM**](ipm-setrange.md) .</span><span class="sxs-lookup"><span data-stu-id="45d00-120">Packs two byte-values into a single LPARAM suitable for use with the [**IPM\_SETRANGE**](ipm-setrange.md) message.</span></span> <br/>       |
| [<span data-ttu-id="45d00-121">**SECONDO \_ indirizzo IP**</span><span class="sxs-lookup"><span data-stu-id="45d00-121">**SECOND\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress) | <span data-ttu-id="45d00-122">Estrae il valore del campo 1 da un indirizzo IP compresso recuperato con il messaggio [**IPM \_ GetAddress**](ipm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="45d00-122">Extracts the field 1 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |
| [<span data-ttu-id="45d00-123">**TERZO \_ indirizzo IP**</span><span class="sxs-lookup"><span data-stu-id="45d00-123">**THIRD\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)   | <span data-ttu-id="45d00-124">Estrae il valore del campo 2 da un indirizzo IP compresso recuperato con il messaggio [**IPM \_ GetAddress**](ipm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="45d00-124">Extracts the field 2 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |



 

### <a name="messages"></a><span data-ttu-id="45d00-125">Messaggi</span><span class="sxs-lookup"><span data-stu-id="45d00-125">Messages</span></span>



| <span data-ttu-id="45d00-126">Argomento</span><span class="sxs-lookup"><span data-stu-id="45d00-126">Topic</span></span>                                         | <span data-ttu-id="45d00-127">Contenuto</span><span class="sxs-lookup"><span data-stu-id="45d00-127">Contents</span></span>                                                                                                                              |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45d00-128">**\_CLEARADDRESS IPM**</span><span class="sxs-lookup"><span data-stu-id="45d00-128">**IPM\_CLEARADDRESS**</span></span>](ipm-clearaddress.md) | <span data-ttu-id="45d00-129">Cancella il contenuto del controllo degli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="45d00-129">Clears the contents of the IP address control.</span></span> <br/>                                                                            |
| [<span data-ttu-id="45d00-130">**IPM \_ GETaddress**</span><span class="sxs-lookup"><span data-stu-id="45d00-130">**IPM\_GETADDRESS**</span></span>](ipm-getaddress.md)     | <span data-ttu-id="45d00-131">Ottiene i valori di indirizzo per tutti e quattro i campi nel controllo degli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="45d00-131">Gets the address values for all four fields in the IP address control.</span></span> <br/>                                                    |
| [<span data-ttu-id="45d00-132">**IPM \_ vuoto**</span><span class="sxs-lookup"><span data-stu-id="45d00-132">**IPM\_ISBLANK**</span></span>](ipm-isblank.md)           | <span data-ttu-id="45d00-133">Determina se tutti i campi nel controllo indirizzo IP sono vuoti.</span><span class="sxs-lookup"><span data-stu-id="45d00-133">Determines if all fields in the IP address control are blank.</span></span> <br/>                                                             |
| [<span data-ttu-id="45d00-134">**\_Indirizzo IPM**</span><span class="sxs-lookup"><span data-stu-id="45d00-134">**IPM\_SETADDRESS**</span></span>](ipm-setaddress.md)     | <span data-ttu-id="45d00-135">Imposta i valori di indirizzo per tutti e quattro i campi nel controllo degli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="45d00-135">Sets the address values for all four fields in the IP address control.</span></span> <br/>                                                    |
| [<span data-ttu-id="45d00-136">**\_SetFocus**</span><span class="sxs-lookup"><span data-stu-id="45d00-136">**IPM\_SETFOCUS**</span></span>](ipm-setfocus.md)         | <span data-ttu-id="45d00-137">Imposta lo stato attivo della tastiera sul campo specificato nel controllo degli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="45d00-137">Sets the keyboard focus to the specified field in the IP address control.</span></span> <span data-ttu-id="45d00-138">Tutto il testo in tale campo verrà selezionato.</span><span class="sxs-lookup"><span data-stu-id="45d00-138">All of the text in that field will be selected.</span></span> <br/> |
| [<span data-ttu-id="45d00-139">**\_SEtrange IPM**</span><span class="sxs-lookup"><span data-stu-id="45d00-139">**IPM\_SETRANGE**</span></span>](ipm-setrange.md)         | <span data-ttu-id="45d00-140">Imposta l'intervallo valido per il campo specificato nel controllo degli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="45d00-140">Sets the valid range for the specified field in the IP address control.</span></span> <br/>                                                   |



 

### <a name="notifications"></a><span data-ttu-id="45d00-141">Notifiche</span><span class="sxs-lookup"><span data-stu-id="45d00-141">Notifications</span></span>



| <span data-ttu-id="45d00-142">Argomento</span><span class="sxs-lookup"><span data-stu-id="45d00-142">Topic</span></span>                                     | <span data-ttu-id="45d00-143">Contenuto</span><span class="sxs-lookup"><span data-stu-id="45d00-143">Contents</span></span>                                                                                                                                                                                   |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45d00-144">IPN \_ FIELDCHANGED</span><span class="sxs-lookup"><span data-stu-id="45d00-144">IPN\_FIELDCHANGED</span></span>](ipn-fieldchanged.md) | <span data-ttu-id="45d00-145">Inviato quando l'utente modifica un campo nel controllo o lo sposta da un campo all'altro.</span><span class="sxs-lookup"><span data-stu-id="45d00-145">Sent when the user changes a field in the control or moves from one field to another.</span></span> <span data-ttu-id="45d00-146">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="45d00-146">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/> |



 

### <a name="structures"></a><span data-ttu-id="45d00-147">Strutture</span><span class="sxs-lookup"><span data-stu-id="45d00-147">Structures</span></span>



| <span data-ttu-id="45d00-148">Argomento</span><span class="sxs-lookup"><span data-stu-id="45d00-148">Topic</span></span>                              | <span data-ttu-id="45d00-149">Contenuto</span><span class="sxs-lookup"><span data-stu-id="45d00-149">Contents</span></span>                                                                                              |
|------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45d00-150">**NMIPADDRESS**</span><span class="sxs-lookup"><span data-stu-id="45d00-150">**NMIPADDRESS**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) | <span data-ttu-id="45d00-151">Contiene informazioni per il codice di notifica di [IPN \_ FIELDCHANGED](ipn-fieldchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="45d00-151">Contains information for the [IPN\_FIELDCHANGED](ipn-fieldchanged.md) notification code.</span></span> <br/> |



 

 

 





