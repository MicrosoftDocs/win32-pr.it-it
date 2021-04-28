---
description: "CPL_NEWINQUIRE messaggio: inviato alla funzione CPlApplet di un'applicazione Pannello di controllo per richiedere informazioni su una finestra di dialogo che l'applicazione supporta."
title: CPL_NEWINQUIRE messaggio (Cpl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: af52889c-7180-4690-8ed1-a0eb0a9dff35
api_name:
- CPL_NEWINQUIRE
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 90c5adf31c01fbab1b62aafd0714d165092f4e23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104439"
---
# <a name="cpl_newinquire-message"></a><span data-ttu-id="44a14-103">CPL \_ NEWINQUIRE message</span><span class="sxs-lookup"><span data-stu-id="44a14-103">CPL\_NEWINQUIRE message</span></span>

<span data-ttu-id="44a14-104">Inviato alla funzione [**CPlApplet di**](/windows/win32/api/cpl/nc-cpl-applet_proc) un'Pannello di controllo per richiedere informazioni su una finestra di dialogo che l'applicazione supporta.</span><span class="sxs-lookup"><span data-stu-id="44a14-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to request information about a dialog box that the application supports.</span></span>

## <a name="parameters"></a><span data-ttu-id="44a14-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="44a14-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44a14-106">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="44a14-106">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="44a14-107">Numero della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="44a14-107">The dialog box number.</span></span> <span data-ttu-id="44a14-108">Questo numero deve essere compreso nell'intervallo da zero a uno minore del valore restituito in risposta al messaggio [**\_ GETCOUNT CPL**](cpl-getcount.md) (CPL \_ GETCOUNT – 1).</span><span class="sxs-lookup"><span data-stu-id="44a14-108">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="44a14-109">*lpncpli*</span><span class="sxs-lookup"><span data-stu-id="44a14-109">*lpncpli*</span></span> 
</dt> <dd>

<span data-ttu-id="44a14-110">Indirizzo di una [**struttura NEWCPLINFO.**](/windows/win32/api/cpl/ns-cpl-newcplinfoa)</span><span class="sxs-lookup"><span data-stu-id="44a14-110">The address of a [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure.</span></span> <span data-ttu-id="44a14-111">L Pannello di controllo appalto dovrebbe riempire questa struttura con informazioni sulla finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="44a14-111">The Control Panel application should fill this structure with information about the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44a14-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="44a14-112">Return value</span></span>

<span data-ttu-id="44a14-113">Se la [**funzione CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) elabora correttamente questo messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="44a14-113">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="44a14-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="44a14-114">Remarks</span></span>

<span data-ttu-id="44a14-115">Per ottenere prestazioni migliori, la maggior parte delle applicazioni deve **ignorare CPL \_ NEWINQUIRE** ed elaborare invece il [**messaggio \_ CPL INQUIRE.**](cpl-inquire.md)</span><span class="sxs-lookup"><span data-stu-id="44a14-115">For better performance, most applications should ignore **CPL\_NEWINQUIRE** and process the [**CPL\_INQUIRE**](cpl-inquire.md) message instead.</span></span>

<span data-ttu-id="44a14-116">Il Pannello di controllo invia il messaggio **CPL \_ NEWINQUIRE** una volta per ogni finestra di dialogo supportata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="44a14-116">The Control Panel sends the **CPL\_NEWINQUIRE** message once for each dialog box supported by your application.</span></span> <span data-ttu-id="44a14-117">Il Pannello di controllo invia anche un [**messaggio CPL \_ INQUIRE**](cpl-inquire.md) per ogni finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="44a14-117">The Control Panel also sends a [**CPL\_INQUIRE**](cpl-inquire.md) message for each dialog box.</span></span> <span data-ttu-id="44a14-118">Questi messaggi vengono inviati immediatamente dopo il [**messaggio \_ GETCOUNT CPL.**](cpl-getcount.md)</span><span class="sxs-lookup"><span data-stu-id="44a14-118">These messages are sent immediately after the [**CPL\_GETCOUNT**](cpl-getcount.md) message.</span></span> <span data-ttu-id="44a14-119">Tuttavia, il sistema non garantisce l'ordine in cui vengono inviati i messaggi **CPL \_ INQUIRE** e **CPL \_ NEWINQUIRE.**</span><span class="sxs-lookup"><span data-stu-id="44a14-119">However, the system does not guarantee the order in which the **CPL\_INQUIRE** and **CPL\_NEWINQUIRE** messages are sent.</span></span>

<span data-ttu-id="44a14-120">È possibile eseguire l'inizializzazione per la finestra di dialogo quando si riceve [**CPL \_ INQUIRE**](cpl-inquire.md).</span><span class="sxs-lookup"><span data-stu-id="44a14-120">You can perform initialization for the dialog box when you receive [**CPL\_INQUIRE**](cpl-inquire.md).</span></span> <span data-ttu-id="44a14-121">Se è necessario allocare memoria, eseguire questa operazione in risposta al [**messaggio \_ CPL INIT.**](cpl-init.md)</span><span class="sxs-lookup"><span data-stu-id="44a14-121">If you must allocate memory, do so in response to the [**CPL\_INIT**](cpl-init.md) message.</span></span>

<span data-ttu-id="44a14-122">[**Libreria CPL \_ INQUIRE**](cpl-inquire.md) è il messaggio preferito.</span><span class="sxs-lookup"><span data-stu-id="44a14-122">[**CPL\_INQUIRE**](cpl-inquire.md) is the preferred message.</span></span> <span data-ttu-id="44a14-123">Ciò è dovuto al **fatto che CPL \_ NEWINQUIRE restituisce** informazioni in un formato che il sistema non può memorizzare nella cache.</span><span class="sxs-lookup"><span data-stu-id="44a14-123">This is because **CPL\_NEWINQUIRE** returns information in a form that the system cannot cache.</span></span> <span data-ttu-id="44a14-124">Di conseguenza, le applicazioni che elaborano **CPL \_ NEWINQUIRE** devono essere caricate ogni volta che il Pannello di controllo necessita delle informazioni, con conseguente riduzione significativa delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="44a14-124">Consequently, applications that process **CPL\_NEWINQUIRE** must be loaded each time the Control Panel needs the information, resulting in a significant reduction in performance.</span></span>

<span data-ttu-id="44a14-125">Le uniche applicazioni che devono usare **CPL \_ NEWINQUIRE** sono quelle che devono modificare l'icona o visualizzare le stringhe in base allo stato del computer.</span><span class="sxs-lookup"><span data-stu-id="44a14-125">The only applications that should use **CPL\_NEWINQUIRE** are those that need to change their icon or display strings based on the state of the computer.</span></span> <span data-ttu-id="44a14-126">In questo caso, il gestore [**CPL \_ INQUIRE**](cpl-inquire.md) deve specificare il valore CPL DYNAMIC RES per i membri \_ \_ **idIcon**, **idName** o **idInfo** della struttura [**CPLINFO,**](/windows/win32/api/cpl/ns-cpl-cplinfo) anziché specificare un identificatore di risorsa valido.</span><span class="sxs-lookup"><span data-stu-id="44a14-126">In this case, your [**CPL\_INQUIRE**](cpl-inquire.md) handler should specify the CPL\_DYNAMIC\_RES value for the **idIcon**, **idName**, or **idInfo** members of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure, rather than specifying a valid resource identifier.</span></span> <span data-ttu-id="44a14-127">In questo modo il Pannello di controllo invia il messaggio **CPL \_ NEWINQUIRE** ogni volta che sono necessarie l'icona e le stringhe di visualizzazione, consentendo di specificare le informazioni in base allo stato corrente del computer.</span><span class="sxs-lookup"><span data-stu-id="44a14-127">This causes the Control Panel to send the **CPL\_NEWINQUIRE** message each time it needs the icon and display strings, allowing you to specify information based on the current state of the computer.</span></span> <span data-ttu-id="44a14-128">Naturalmente, questa operazione è notevolmente più lenta rispetto all'uso di informazioni memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="44a14-128">Of course, this is significantly slower than using cached information.</span></span>

## <a name="requirements"></a><span data-ttu-id="44a14-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44a14-129">Requirements</span></span>



| <span data-ttu-id="44a14-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="44a14-130">Requirement</span></span> | <span data-ttu-id="44a14-131">Valore</span><span class="sxs-lookup"><span data-stu-id="44a14-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="44a14-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44a14-132">Minimum supported client</span></span><br/> | <span data-ttu-id="44a14-133">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="44a14-133">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="44a14-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44a14-134">Minimum supported server</span></span><br/> | <span data-ttu-id="44a14-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="44a14-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="44a14-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="44a14-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="44a14-137"><dt>Cpl.h</dt></span><span class="sxs-lookup"><span data-stu-id="44a14-137"><dt>Cpl.h</dt></span></span> </dl> |



 

 
