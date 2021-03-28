---
description: Inviato alla funzione CPlApplet di un'applicazione del pannello di controllo per recuperare il numero di finestre di dialogo supportate dall'applicazione.
title: Messaggio CPL_GETCOUNT (cpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6b88b56c-aad7-4144-ab95-15d7eef21861
api_name:
- CPL_GETCOUNT
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3bf8980fa29841d3c5341daeeccf26cea05db80c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525392"
---
# <a name="cpl_getcount-message"></a><span data-ttu-id="2ae11-103">\_Messaggio cpl GETcount</span><span class="sxs-lookup"><span data-stu-id="2ae11-103">CPL\_GETCOUNT message</span></span>

<span data-ttu-id="2ae11-104">Inviato alla funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) di un'applicazione del pannello di controllo per recuperare il numero di finestre di dialogo supportate dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2ae11-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to retrieve the number of dialog boxes supported by the application.</span></span>

## <a name="parameters"></a><span data-ttu-id="2ae11-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="2ae11-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ae11-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ae11-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2ae11-107">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2ae11-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2ae11-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ae11-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2ae11-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2ae11-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ae11-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2ae11-110">Return value</span></span>

<span data-ttu-id="2ae11-111">La funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) restituisce il numero di finestre di dialogo supportate dall'applicazione del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="2ae11-111">The [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function returns the number of dialog boxes that the Control Panel application supports.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ae11-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ae11-112">Remarks</span></span>

<span data-ttu-id="2ae11-113">Questo messaggio viene inviato immediatamente dopo il messaggio [**cpl \_ init**](cpl-init.md) .</span><span class="sxs-lookup"><span data-stu-id="2ae11-113">This message is sent immediately after the [**CPL\_INIT**](cpl-init.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ae11-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ae11-114">Requirements</span></span>



| <span data-ttu-id="2ae11-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ae11-115">Requirement</span></span> | <span data-ttu-id="2ae11-116">Valore</span><span class="sxs-lookup"><span data-stu-id="2ae11-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2ae11-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ae11-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2ae11-118">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2ae11-118">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2ae11-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ae11-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2ae11-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2ae11-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2ae11-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2ae11-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ae11-122"><dt>Cpl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ae11-122"><dt>Cpl.h</dt></span></span> </dl> |



 

 
