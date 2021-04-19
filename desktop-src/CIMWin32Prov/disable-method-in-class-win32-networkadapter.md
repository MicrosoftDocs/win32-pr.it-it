---
description: Disabilita la scheda di rete.
ms.assetid: 6b328d7c-a9ef-4c9b-bc32-13fa2e0f65eb
ms.tgt_platform: multiple
title: Metodo Disable della classe Win32_NetworkAdapter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapter.Disable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a9c6b1a506310460d9131709092b739f68986e02
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304699"
---
# <a name="disable-method-of-the-win32_networkadapter-class"></a><span data-ttu-id="81e0c-103">Metodo Disable della classe Win32 \_ NetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="81e0c-103">Disable method of the Win32\_NetworkAdapter class</span></span>

<span data-ttu-id="81e0c-104">Il metodo **Disable Disabilita** la scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="81e0c-104">The **Disable** method disables the network adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="81e0c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81e0c-105">Syntax</span></span>


```mof
uint32 Disable();
```



## <a name="parameters"></a><span data-ttu-id="81e0c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="81e0c-106">Parameters</span></span>

<span data-ttu-id="81e0c-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="81e0c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="81e0c-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="81e0c-108">Return value</span></span>

<span data-ttu-id="81e0c-109">Restituisce zero (0) per indicare l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="81e0c-109">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="81e0c-110">Qualsiasi altro numero indica un errore.</span><span class="sxs-lookup"><span data-stu-id="81e0c-110">Any other number indicates an error.</span></span> <span data-ttu-id="81e0c-111">Per i codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="81e0c-111">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="81e0c-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81e0c-112">Requirements</span></span>



| <span data-ttu-id="81e0c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="81e0c-113">Requirement</span></span> | <span data-ttu-id="81e0c-114">Valore</span><span class="sxs-lookup"><span data-stu-id="81e0c-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81e0c-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81e0c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="81e0c-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81e0c-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="81e0c-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81e0c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="81e0c-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81e0c-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="81e0c-119">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="81e0c-119">Namespace</span></span><br/>                | <span data-ttu-id="81e0c-120">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="81e0c-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="81e0c-121">MOF</span><span class="sxs-lookup"><span data-stu-id="81e0c-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81e0c-122"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81e0c-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="81e0c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="81e0c-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81e0c-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81e0c-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81e0c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81e0c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81e0c-126">**\_NetworkAdapter Win32**</span><span class="sxs-lookup"><span data-stu-id="81e0c-126">**Win32\_NetworkAdapter**</span></span>](win32-networkadapter.md)
</dt> <dt>

[<span data-ttu-id="81e0c-127">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="81e0c-127">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="81e0c-128">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="81e0c-128">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

