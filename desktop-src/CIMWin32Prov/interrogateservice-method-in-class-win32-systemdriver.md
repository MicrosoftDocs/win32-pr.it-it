---
description: Richiede che il servizio driver di sistema aggiorni lo stato a Service Manager.
ms.assetid: 350d9044-39fd-436f-ab15-b30324b2b2e9
ms.tgt_platform: multiple
title: Metodo InterrogateService della classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.InterrogateService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 666a261dfe3fac7dd62e6253c5eb4804b3a55677
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126480"
---
# <a name="interrogateservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="93dc7-103">Metodo InterrogateService della \_ classe SystemDriver Win32</span><span class="sxs-lookup"><span data-stu-id="93dc7-103">InterrogateService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="93dc7-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **InterrogateService** richiede che il servizio driver di sistema aggiorni lo stato a Service Manager.</span><span class="sxs-lookup"><span data-stu-id="93dc7-104">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the system driver service update its state to the service manager.</span></span>

<span data-ttu-id="93dc7-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="93dc7-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="93dc7-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="93dc7-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="93dc7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93dc7-107">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="93dc7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="93dc7-108">Parameters</span></span>

<span data-ttu-id="93dc7-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="93dc7-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="93dc7-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93dc7-110">Return value</span></span>

<span data-ttu-id="93dc7-111">Restituisce un valore pari a 0 (zero) se la richiesta **InterrogateService** è stata accettata, 1 (uno) se la richiesta non è supportata e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="93dc7-111">Returns a value of 0 (zero) if the **InterrogateService** request was accepted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="93dc7-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93dc7-112">Requirements</span></span>



| <span data-ttu-id="93dc7-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="93dc7-113">Requirement</span></span> | <span data-ttu-id="93dc7-114">Valore</span><span class="sxs-lookup"><span data-stu-id="93dc7-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93dc7-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93dc7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="93dc7-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93dc7-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="93dc7-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93dc7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="93dc7-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93dc7-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="93dc7-119">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="93dc7-119">Namespace</span></span><br/>                | <span data-ttu-id="93dc7-120">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="93dc7-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="93dc7-121">MOF</span><span class="sxs-lookup"><span data-stu-id="93dc7-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93dc7-122"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93dc7-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="93dc7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="93dc7-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93dc7-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93dc7-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93dc7-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93dc7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93dc7-126">**\_SystemDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="93dc7-126">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> <dt>

<span data-ttu-id="93dc7-127">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="93dc7-127">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="93dc7-128">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="93dc7-128">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

