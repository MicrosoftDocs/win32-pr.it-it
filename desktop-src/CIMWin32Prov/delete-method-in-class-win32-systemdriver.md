---
description: Metodo Delete della classe Win32_SystemDriver- Eliminazione&\# 8194; Il metodo della classe WMI elimina un servizio esistente.
ms.assetid: 5e437d36-3582-448c-b568-45f7fb13b096
ms.tgt_platform: multiple
title: Metodo Delete della classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e1b7435a1bca561b19e7d85299413f88f1ae76c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097089"
---
# <a name="delete-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="055d8-103">Metodo Delete della classe SystemDriver Win32 \_</span><span class="sxs-lookup"><span data-stu-id="055d8-103">Delete method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="055d8-104">Il **metodo delete** della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) elimina un servizio esistente.</span><span class="sxs-lookup"><span data-stu-id="055d8-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes an existing service.</span></span>

<span data-ttu-id="055d8-105">Questo argomento usa Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="055d8-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="055d8-106">Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="055d8-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="055d8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="055d8-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="055d8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="055d8-108">Parameters</span></span>

<span data-ttu-id="055d8-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="055d8-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="055d8-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="055d8-110">Return value</span></span>

<span data-ttu-id="055d8-111">Restituisce il valore 0 (zero) se il servizio è stato eliminato correttamente, 1 (uno) se la richiesta non è supportata e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="055d8-111">Returns a value of 0 (zero) if the service was successfully deleted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="055d8-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="055d8-112">Requirements</span></span>



| <span data-ttu-id="055d8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="055d8-113">Requirement</span></span> | <span data-ttu-id="055d8-114">Valore</span><span class="sxs-lookup"><span data-stu-id="055d8-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="055d8-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="055d8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="055d8-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="055d8-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="055d8-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="055d8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="055d8-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="055d8-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="055d8-119">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="055d8-119">Namespace</span></span><br/>                | <span data-ttu-id="055d8-120">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="055d8-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="055d8-121">MOF</span><span class="sxs-lookup"><span data-stu-id="055d8-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="055d8-122"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="055d8-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="055d8-123">DLL</span><span class="sxs-lookup"><span data-stu-id="055d8-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="055d8-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="055d8-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="055d8-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="055d8-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="055d8-126">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="055d8-126">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="055d8-127">**Win32 \_ SystemDriver**</span><span class="sxs-lookup"><span data-stu-id="055d8-127">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

