---
description: Inviato alla funzione CPlApplet di un'applicazione del pannello di controllo per richiedere informazioni su una finestra di dialogo supportata dall'applicazione.
title: Messaggio CPL_NEWINQUIRE (cpl. h)
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
ms.openlocfilehash: 72992d4ea867bc091c29feaa99cc1a22c2a02b2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977346"
---
# <a name="cpl_newinquire-message"></a><span data-ttu-id="8360d-103">\_Messaggio NEWINQUIRE cpl</span><span class="sxs-lookup"><span data-stu-id="8360d-103">CPL\_NEWINQUIRE message</span></span>

<span data-ttu-id="8360d-104">Inviato alla funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) di un'applicazione del pannello di controllo per richiedere informazioni su una finestra di dialogo supportata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8360d-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to request information about a dialog box that the application supports.</span></span>

## <a name="parameters"></a><span data-ttu-id="8360d-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="8360d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8360d-106">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="8360d-106">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="8360d-107">Numero della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="8360d-107">The dialog box number.</span></span> <span data-ttu-id="8360d-108">Questo numero deve essere compreso tra zero e uno minore del valore restituito in risposta al messaggio [**cpl \_ GetCount**](cpl-getcount.md) (cpl \_ GetCount-1).</span><span class="sxs-lookup"><span data-stu-id="8360d-108">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="8360d-109">*lpncpli*</span><span class="sxs-lookup"><span data-stu-id="8360d-109">*lpncpli*</span></span> 
</dt> <dd>

<span data-ttu-id="8360d-110">Indirizzo di una struttura [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) .</span><span class="sxs-lookup"><span data-stu-id="8360d-110">The address of a [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure.</span></span> <span data-ttu-id="8360d-111">L'applicazione del pannello di controllo deve riempire questa struttura con le informazioni sulla finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="8360d-111">The Control Panel application should fill this structure with information about the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8360d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8360d-112">Return value</span></span>

<span data-ttu-id="8360d-113">Se la funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) elabora correttamente questo messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="8360d-113">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8360d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8360d-114">Remarks</span></span>

<span data-ttu-id="8360d-115">Per ottenere prestazioni ottimali, la maggior parte delle applicazioni deve ignorare **cpl \_ NEWINQUIRE** ed elaborare invece il messaggio [**cpl \_ Inquirer**](cpl-inquire.md) .</span><span class="sxs-lookup"><span data-stu-id="8360d-115">For better performance, most applications should ignore **CPL\_NEWINQUIRE** and process the [**CPL\_INQUIRE**](cpl-inquire.md) message instead.</span></span>

<span data-ttu-id="8360d-116">Il pannello di controllo Invia il messaggio **\_ NEWINQUIRE cpl** una volta per ogni finestra di dialogo supportata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8360d-116">The Control Panel sends the **CPL\_NEWINQUIRE** message once for each dialog box supported by your application.</span></span> <span data-ttu-id="8360d-117">Il pannello di controllo Invia anche un messaggio di [**\_ richiesta cpl**](cpl-inquire.md) per ogni finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="8360d-117">The Control Panel also sends a [**CPL\_INQUIRE**](cpl-inquire.md) message for each dialog box.</span></span> <span data-ttu-id="8360d-118">Questi messaggi vengono inviati immediatamente dopo il messaggio [**cpl \_ GetCount**](cpl-getcount.md) .</span><span class="sxs-lookup"><span data-stu-id="8360d-118">These messages are sent immediately after the [**CPL\_GETCOUNT**](cpl-getcount.md) message.</span></span> <span data-ttu-id="8360d-119">Tuttavia, il sistema non garantisce l'ordine in cui vengono inviati i messaggi **cpl \_ Inquirer** e **cpl \_ NEWINQUIRE** .</span><span class="sxs-lookup"><span data-stu-id="8360d-119">However, the system does not guarantee the order in which the **CPL\_INQUIRE** and **CPL\_NEWINQUIRE** messages are sent.</span></span>

<span data-ttu-id="8360d-120">È possibile eseguire l'inizializzazione per la finestra di dialogo quando si riceve la [**\_ richiesta di cpl**](cpl-inquire.md).</span><span class="sxs-lookup"><span data-stu-id="8360d-120">You can perform initialization for the dialog box when you receive [**CPL\_INQUIRE**](cpl-inquire.md).</span></span> <span data-ttu-id="8360d-121">Se è necessario allocare memoria, eseguire questa operazione in risposta al messaggio [**cpl \_ init**](cpl-init.md) .</span><span class="sxs-lookup"><span data-stu-id="8360d-121">If you must allocate memory, do so in response to the [**CPL\_INIT**](cpl-init.md) message.</span></span>

<span data-ttu-id="8360d-122">[**Cpl \_ DOMANDi**](cpl-inquire.md) è il messaggio preferito.</span><span class="sxs-lookup"><span data-stu-id="8360d-122">[**CPL\_INQUIRE**](cpl-inquire.md) is the preferred message.</span></span> <span data-ttu-id="8360d-123">Questo perché **cpl \_ NEWINQUIRE** restituisce informazioni in un modulo che il sistema non è in grado di memorizzare nella cache.</span><span class="sxs-lookup"><span data-stu-id="8360d-123">This is because **CPL\_NEWINQUIRE** returns information in a form that the system cannot cache.</span></span> <span data-ttu-id="8360d-124">Di conseguenza, le applicazioni che elaborano **cpl \_ NEWINQUIRE** devono essere caricate ogni volta che il pannello di controllo necessita di informazioni, causando una riduzione significativa delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="8360d-124">Consequently, applications that process **CPL\_NEWINQUIRE** must be loaded each time the Control Panel needs the information, resulting in a significant reduction in performance.</span></span>

<span data-ttu-id="8360d-125">Le uniche applicazioni che devono usare **cpl \_ NEWINQUIRE** sono quelle che devono modificare l'icona o visualizzare le stringhe in base allo stato del computer.</span><span class="sxs-lookup"><span data-stu-id="8360d-125">The only applications that should use **CPL\_NEWINQUIRE** are those that need to change their icon or display strings based on the state of the computer.</span></span> <span data-ttu-id="8360d-126">In questo caso, il gestore delle [**\_ richieste cpl**](cpl-inquire.md) deve specificare il \_ \_ valore res dinamico cpl per i membri **idIcon**, **idName** o **idInfo** della struttura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) , anziché specificare un identificatore di risorsa valido.</span><span class="sxs-lookup"><span data-stu-id="8360d-126">In this case, your [**CPL\_INQUIRE**](cpl-inquire.md) handler should specify the CPL\_DYNAMIC\_RES value for the **idIcon**, **idName**, or **idInfo** members of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure, rather than specifying a valid resource identifier.</span></span> <span data-ttu-id="8360d-127">In questo modo, il pannello di controllo invierà il messaggio **cpl \_ NEWINQUIRE** ogni volta che è necessaria l'icona e le stringhe di visualizzazione, consentendo di specificare le informazioni in base allo stato corrente del computer.</span><span class="sxs-lookup"><span data-stu-id="8360d-127">This causes the Control Panel to send the **CPL\_NEWINQUIRE** message each time it needs the icon and display strings, allowing you to specify information based on the current state of the computer.</span></span> <span data-ttu-id="8360d-128">Naturalmente, questo è molto più lento rispetto all'uso delle informazioni memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="8360d-128">Of course, this is significantly slower than using cached information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8360d-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8360d-129">Requirements</span></span>



| <span data-ttu-id="8360d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8360d-130">Requirement</span></span> | <span data-ttu-id="8360d-131">Valore</span><span class="sxs-lookup"><span data-stu-id="8360d-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8360d-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8360d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8360d-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8360d-133">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8360d-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8360d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8360d-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8360d-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8360d-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8360d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="8360d-137"><dt>Cpl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8360d-137"><dt>Cpl.h</dt></span></span> </dl> |



 

 
