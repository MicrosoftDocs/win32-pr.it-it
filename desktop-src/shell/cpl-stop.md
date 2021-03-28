---
description: Inviato alla funzione CPlApplet di un'applicazione del pannello di controllo quando si chiude l'applicazione di controllo del pannello di controllo. L'applicazione di controllo Invia il messaggio una volta per ogni finestra di dialogo supportata dall'applicazione.
title: Messaggio CPL_STOP (cpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4f632b91-8200-42a3-90cc-a98889704ca4
api_name:
- CPL_STOP
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 78f8926d85b35b8cf5e55188c6cd76b014b3c4c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977338"
---
# <a name="cpl_stop-message"></a><span data-ttu-id="ebcd3-104">\_Messaggio di arresto cpl</span><span class="sxs-lookup"><span data-stu-id="ebcd3-104">CPL\_STOP message</span></span>

<span data-ttu-id="ebcd3-105">Inviato alla funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) di un'applicazione del pannello di controllo quando si chiude l'applicazione di controllo del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="ebcd3-105">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application when the controlling application of the Control Panel closes.</span></span> <span data-ttu-id="ebcd3-106">L'applicazione di controllo Invia il messaggio una volta per ogni finestra di dialogo supportata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ebcd3-106">The controlling application sends the message once for each dialog box that the application supports.</span></span>

## <a name="parameters"></a><span data-ttu-id="ebcd3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ebcd3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebcd3-108">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="ebcd3-108">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="ebcd3-109">Numero della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="ebcd3-109">The dialog box number.</span></span>

</dd> <dt>

<span data-ttu-id="ebcd3-110">*lData*</span><span class="sxs-lookup"><span data-stu-id="ebcd3-110">*lData*</span></span> 
</dt> <dd>

<span data-ttu-id="ebcd3-111">Valore che l'applicazione del pannello di controllo è stata caricata nel membro **lpData** della struttura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) o [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) per la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="ebcd3-111">The value that the Control Panel application loaded into the **lpData** member of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) or [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure for the dialog box.</span></span> <span data-ttu-id="ebcd3-112">L'applicazione carica il membro **lpData** in risposta al messaggio [**cpl \_ Inquirer**](cpl-inquire.md) o [**cpl \_ NEWINQUIRE**](cpl-newinquire.md) .</span><span class="sxs-lookup"><span data-stu-id="ebcd3-112">The application loads the **lpData** member in response to the [**CPL\_INQUIRE**](cpl-inquire.md) or [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebcd3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ebcd3-113">Return value</span></span>

<span data-ttu-id="ebcd3-114">Se la funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) elabora correttamente questo messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="ebcd3-114">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebcd3-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="ebcd3-115">Remarks</span></span>

<span data-ttu-id="ebcd3-116">In risposta a questo messaggio, un'applicazione del pannello di controllo deve eseguire la pulizia per la finestra di dialogo specificata.</span><span class="sxs-lookup"><span data-stu-id="ebcd3-116">In response to this message, a Control Panel application must perform cleanup for the given dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebcd3-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ebcd3-117">Requirements</span></span>



| <span data-ttu-id="ebcd3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebcd3-118">Requirement</span></span> | <span data-ttu-id="ebcd3-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ebcd3-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ebcd3-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebcd3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ebcd3-121">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ebcd3-121">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ebcd3-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebcd3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ebcd3-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ebcd3-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ebcd3-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ebcd3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebcd3-125"><dt>Cpl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebcd3-125"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebcd3-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ebcd3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebcd3-127">**\_uscita cpl**</span><span class="sxs-lookup"><span data-stu-id="ebcd3-127">**CPL\_EXIT**</span></span>](cpl-exit.md)
</dt> <dt>

[<span data-ttu-id="ebcd3-128">**\_conteggio cpl**</span><span class="sxs-lookup"><span data-stu-id="ebcd3-128">**CPL\_GETCOUNT**</span></span>](cpl-getcount.md)
</dt> </dl>

 

 
