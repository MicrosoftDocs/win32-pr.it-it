---
description: Inviato alla funzione CPlApplet di un'applicazione del pannello di controllo quando l'utente fa doppio clic sull'icona di una finestra di dialogo supportata dall'applicazione.
title: Messaggio CPL_DBLCLK (cpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 68d74372-2fc2-45ed-8f77-574b943d28fa
api_name:
- CPL_DBLCLK
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d6c67204c7b4fae5275e50d428a0371af4cf2e2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993725"
---
# <a name="cpl_dblclk-message"></a><span data-ttu-id="5f134-103">\_Messaggio DBLCLK cpl</span><span class="sxs-lookup"><span data-stu-id="5f134-103">CPL\_DBLCLK message</span></span>

<span data-ttu-id="5f134-104">Inviato alla funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) di un'applicazione del pannello di controllo quando l'utente fa doppio clic sull'icona di una finestra di dialogo supportata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5f134-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application when the user double-clicks the icon of a dialog box supported by the application.</span></span>

## <a name="parameters"></a><span data-ttu-id="5f134-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="5f134-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f134-106">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="5f134-106">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="5f134-107">Numero della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="5f134-107">The dialog box number.</span></span> <span data-ttu-id="5f134-108">Questo numero deve essere compreso tra zero e uno minore del valore restituito in risposta al messaggio [**cpl \_ GetCount**](cpl-getcount.md) (cpl \_ GetCount-1).</span><span class="sxs-lookup"><span data-stu-id="5f134-108">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="5f134-109">*lData*</span><span class="sxs-lookup"><span data-stu-id="5f134-109">*lData*</span></span> 
</dt> <dd>

<span data-ttu-id="5f134-110">Valore che l'applicazione del pannello di controllo è stata caricata nel membro **lpData** della struttura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) o [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) per la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="5f134-110">The value that the Control Panel application loaded into the **lpData** member of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) or [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure for the dialog box.</span></span> <span data-ttu-id="5f134-111">L'applicazione carica il membro **lpData** in risposta al messaggio [**cpl \_ Inquirer**](cpl-inquire.md) o [**cpl \_ NEWINQUIRE**](cpl-newinquire.md) .</span><span class="sxs-lookup"><span data-stu-id="5f134-111">The application loads the **lpData** member in response to the [**CPL\_INQUIRE**](cpl-inquire.md) or [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f134-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5f134-112">Return value</span></span>

<span data-ttu-id="5f134-113">Se la funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) elabora questo messaggio correttamente, il valore restituito è zero; in caso contrario, è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="5f134-113">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, the return value is zero; otherwise, it is nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f134-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f134-114">Remarks</span></span>

<span data-ttu-id="5f134-115">In risposta a questo messaggio, un'applicazione del pannello di controllo deve visualizzare la finestra di dialogo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="5f134-115">In response to this message, a Control Panel application must display the corresponding dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f134-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f134-116">Requirements</span></span>



| <span data-ttu-id="5f134-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f134-117">Requirement</span></span> | <span data-ttu-id="5f134-118">Valore</span><span class="sxs-lookup"><span data-stu-id="5f134-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5f134-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f134-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5f134-120">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5f134-120">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="5f134-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f134-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5f134-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5f134-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5f134-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f134-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f134-124"><dt>Cpl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f134-124"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f134-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f134-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f134-126">**\_selezione cpl**</span><span class="sxs-lookup"><span data-stu-id="5f134-126">**CPL\_SELECT**</span></span>](cpl-select.md)
</dt> </dl>

 

 
