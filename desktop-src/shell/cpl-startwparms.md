---
description: Inviato per notificare a CPlApplet che l'utente ha scelto l'icona associata a una determinata finestra di dialogo. CPlApplet dovrebbe visualizzare la finestra di dialogo corrispondente ed eseguire tutte le attività specificate dall'utente.
title: Messaggio CPL_STARTWPARMS (cpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 04ac5117-39c9-4d3f-b32d-8f8d2b515be1
api_name:
- CPL_STARTWPARMS
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 790779c1c45acbc211fe36e28b2e55d5ae2e60da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966523"
---
# <a name="cpl_startwparms-message"></a><span data-ttu-id="f1663-104">\_Messaggio STARTWPARMS cpl</span><span class="sxs-lookup"><span data-stu-id="f1663-104">CPL\_STARTWPARMS message</span></span>

<span data-ttu-id="f1663-105">Inviato per notificare a [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) che l'utente ha scelto l'icona associata a una determinata finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="f1663-105">Sent to notify [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) that the user has chosen the icon associated with a given dialog box.</span></span> <span data-ttu-id="f1663-106">**CPlApplet** dovrebbe visualizzare la finestra di dialogo corrispondente ed eseguire tutte le attività specificate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="f1663-106">**CPlApplet** should display the corresponding dialog box and carry out any user-specified tasks.</span></span>

## <a name="parameters"></a><span data-ttu-id="f1663-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1663-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1663-108">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="f1663-108">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="f1663-109">Numero della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="f1663-109">The dialog box number.</span></span> <span data-ttu-id="f1663-110">Questo numero deve essere compreso tra zero e uno minore del valore restituito in risposta al messaggio [**cpl \_ GetCount**](cpl-getcount.md) (cpl \_ GetCount-1).</span><span class="sxs-lookup"><span data-stu-id="f1663-110">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="f1663-111">*lpszExtra*</span><span class="sxs-lookup"><span data-stu-id="f1663-111">*lpszExtra*</span></span> 
</dt> <dd>

<span data-ttu-id="f1663-112">Stringa con direzioni aggiuntive per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f1663-112">A string with additional directions for execution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1663-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f1663-113">Return value</span></span>

<span data-ttu-id="f1663-114">Restituisce **true** se il messaggio è stato gestito; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="f1663-114">Returns **TRUE** if the message was handled, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1663-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="f1663-115">Remarks</span></span>

<span data-ttu-id="f1663-116">**Cpl \_ STARTWPARMS** è simile a [**cpl \_ DBLCLK**](cpl-dblclk.md) ma consente di passare una stringa a [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) anziché a un valore **int**. È possibile utilizzare questa stringa come metodo flessibile per fornire indicazioni dettagliate per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f1663-116">**CPL\_STARTWPARMS** is similar to [**CPL\_DBLCLK**](cpl-dblclk.md) but allows you to pass a string to [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) instead of an **int**. You can use this string as a flexible way to provide detailed directions for execution.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1663-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1663-117">Requirements</span></span>



| <span data-ttu-id="f1663-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1663-118">Requirement</span></span> | <span data-ttu-id="f1663-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f1663-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f1663-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1663-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f1663-121">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f1663-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="f1663-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1663-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f1663-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f1663-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f1663-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f1663-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1663-125"><dt>Cpl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1663-125"><dt>Cpl.h</dt></span></span> </dl> |



 

 
