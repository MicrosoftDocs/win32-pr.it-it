---
description: "CPL_INQUIRE messaggio: inviato alla funzione CPlApplet di un'applicazione Pannello di controllo per richiedere informazioni su una finestra di dialogo che l'applicazione supporta."
title: CPL_INQUIRE messaggio (Cpl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: daca87b7-f1ee-40f4-95d2-3150b595151e
api_name:
- CPL_INQUIRE
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f9962ff94e8bf80041d7b61ecf97220d573131fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104469"
---
# <a name="cpl_inquire-message"></a><span data-ttu-id="c0f57-103">Messaggio \_ CPL INQUIRE</span><span class="sxs-lookup"><span data-stu-id="c0f57-103">CPL\_INQUIRE message</span></span>

<span data-ttu-id="c0f57-104">Inviato alla [**funzione CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) di un'Pannello di controllo per richiedere informazioni su una finestra di dialogo che l'applicazione supporta.</span><span class="sxs-lookup"><span data-stu-id="c0f57-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to request information about a dialog box that the application supports.</span></span>

## <a name="parameters"></a><span data-ttu-id="c0f57-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="c0f57-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0f57-106">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="c0f57-106">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="c0f57-107">Numero della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="c0f57-107">The dialog box number.</span></span> <span data-ttu-id="c0f57-108">Questo numero deve essere compreso nell'intervallo compreso tra zero e uno minore del valore restituito in risposta al messaggio [**\_ GETCOUNT CPL**](cpl-getcount.md) (CPL \_ GETCOUNT – 1).</span><span class="sxs-lookup"><span data-stu-id="c0f57-108">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="c0f57-109">*lpcpli*</span><span class="sxs-lookup"><span data-stu-id="c0f57-109">*lpcpli*</span></span> 
</dt> <dd>

<span data-ttu-id="c0f57-110">Indirizzo di una [**struttura CPLINFO.**](/windows/win32/api/cpl/ns-cpl-cplinfo)</span><span class="sxs-lookup"><span data-stu-id="c0f57-110">The address of a [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure.</span></span> <span data-ttu-id="c0f57-111">L'applicazione deve riempire questa struttura con identificatori di risorsa per l'icona, il nome breve, la descrizione e qualsiasi valore definito dall'utente associato alla finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="c0f57-111">The application must fill this structure with resource identifiers for the icon, short name, description, and any user-defined value associated with the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0f57-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c0f57-112">Return value</span></span>

<span data-ttu-id="c0f57-113">Se la [**funzione CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) elabora correttamente questo messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="c0f57-113">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0f57-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c0f57-114">Remarks</span></span>

<span data-ttu-id="c0f57-115">Il Pannello di controllo invia il messaggio **CPL \_ INQUIRE** una volta per ogni finestra di dialogo supportata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c0f57-115">The Control Panel sends the **CPL\_INQUIRE** message once for each dialog box supported by your application.</span></span> <span data-ttu-id="c0f57-116">Il Pannello di controllo invia anche un [**messaggio CPL \_ NEWINQUIRE**](cpl-newinquire.md) per ogni finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="c0f57-116">The Control Panel also sends a [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message for each dialog box.</span></span> <span data-ttu-id="c0f57-117">Questi messaggi vengono inviati immediatamente dopo il [**messaggio \_ GETCOUNT CPL.**](cpl-getcount.md)</span><span class="sxs-lookup"><span data-stu-id="c0f57-117">These messages are sent immediately after the [**CPL\_GETCOUNT**](cpl-getcount.md) message.</span></span> <span data-ttu-id="c0f57-118">Tuttavia, il sistema non garantisce l'ordine in cui vengono inviati i messaggi **CPL \_ INQUIRE** e **CPL \_ NEWINQUIRE.**</span><span class="sxs-lookup"><span data-stu-id="c0f57-118">However, the system does not guarantee the order in which the **CPL\_INQUIRE** and **CPL\_NEWINQUIRE** messages are sent.</span></span>

<span data-ttu-id="c0f57-119">È possibile eseguire l'inizializzazione per la finestra di dialogo quando si riceve **CPL \_ INQUIRE**.</span><span class="sxs-lookup"><span data-stu-id="c0f57-119">You can perform initialization for the dialog box when you receive **CPL\_INQUIRE**.</span></span> <span data-ttu-id="c0f57-120">Se è necessario allocare memoria, eseguire questa operazione in risposta al messaggio [**\_ CPL INIT.**](cpl-init.md)</span><span class="sxs-lookup"><span data-stu-id="c0f57-120">If you must allocate memory, do so in response to the [**CPL\_INIT**](cpl-init.md) message.</span></span>

<span data-ttu-id="c0f57-121">Il [**messaggio CPL \_ NEWINQUIRE**](cpl-newinquire.md) restituisce informazioni in un formato che il sistema non può memorizzare nella cache.</span><span class="sxs-lookup"><span data-stu-id="c0f57-121">The [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message returns information in a form that the system cannot cache.</span></span> <span data-ttu-id="c0f57-122">Per questo motivo, la maggior [**parte delle funzioni CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) deve elaborare **CPL \_ INQUIRE** e ignorare **CPL \_ NEWINQUIRE**.</span><span class="sxs-lookup"><span data-stu-id="c0f57-122">For this reason, most [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) functions should process **CPL\_INQUIRE** and ignore **CPL\_NEWINQUIRE**.</span></span>

<span data-ttu-id="c0f57-123">Le uniche applicazioni che devono usare [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) sono quelle che devono modificare l'icona o visualizzare le stringhe in base allo stato del computer.</span><span class="sxs-lookup"><span data-stu-id="c0f57-123">The only applications that should use [**CPL\_NEWINQUIRE**](cpl-newinquire.md) are those that need to change their icon or display strings based on the state of the computer.</span></span> <span data-ttu-id="c0f57-124">In questo caso, il gestore **CPL \_ INQUIRE** deve specificare il valore CPL DYNAMIC RES per i membri \_ \_ **idIcon**, **idName** o **idInfo** della struttura [**CPLINFO,**](/windows/win32/api/cpl/ns-cpl-cplinfo) anziché specificare un identificatore di risorsa valido.</span><span class="sxs-lookup"><span data-stu-id="c0f57-124">In this case, your **CPL\_INQUIRE** handler should specify the CPL\_DYNAMIC\_RES value for the **idIcon**, **idName**, or **idInfo** members of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure, rather than specifying a valid resource identifier.</span></span> <span data-ttu-id="c0f57-125">In questo modo il Pannello di controllo invia il messaggio **CPL \_ NEWINQUIRE** ogni volta che sono necessarie l'icona e le stringhe di visualizzazione, consentendo di specificare le informazioni in base allo stato corrente del computer.</span><span class="sxs-lookup"><span data-stu-id="c0f57-125">This causes the Control Panel to send the **CPL\_NEWINQUIRE** message each time it needs the icon and display strings, allowing you to specify information based on the current state of the computer.</span></span> <span data-ttu-id="c0f57-126">Questa operazione è notevolmente più lenta rispetto all'uso di informazioni memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="c0f57-126">This is significantly slower than using cached information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0f57-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0f57-127">Requirements</span></span>



| <span data-ttu-id="c0f57-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0f57-128">Requirement</span></span> | <span data-ttu-id="c0f57-129">Valore</span><span class="sxs-lookup"><span data-stu-id="c0f57-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c0f57-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0f57-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c0f57-131">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c0f57-131">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c0f57-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0f57-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c0f57-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c0f57-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c0f57-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c0f57-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0f57-135"><dt>Cpl.h</dt></span><span class="sxs-lookup"><span data-stu-id="c0f57-135"><dt>Cpl.h</dt></span></span> </dl> |



 

 
