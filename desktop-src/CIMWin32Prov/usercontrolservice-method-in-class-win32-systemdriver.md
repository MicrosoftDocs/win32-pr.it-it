---
description: Tenta di inviare un codice di controllo definito dall'utente a un servizio gestito da un driver di sistema.
ms.assetid: 62e66c35-f264-43d0-9e94-fb5e85f936e0
ms.tgt_platform: multiple
title: Metodo UserControlService della classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 99974206f6487d90e1660f5a64c1d00904912c66
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966301"
---
# <a name="usercontrolservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="b20b8-103">Metodo UserControlService della \_ classe SystemDriver Win32</span><span class="sxs-lookup"><span data-stu-id="b20b8-103">UserControlService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="b20b8-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UserControlService** tenta di inviare un codice di controllo definito dall'utente a un servizio gestito da un driver di sistema.</span><span class="sxs-lookup"><span data-stu-id="b20b8-104">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to a service managed by a system driver.</span></span>

<span data-ttu-id="b20b8-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="b20b8-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b20b8-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b20b8-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b20b8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b20b8-107">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="b20b8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b20b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b20b8-109">*ControlCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b20b8-109">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b20b8-110">Specifica i valori definiti (da 128 a 255) che forniscono i comandi di controllo specifici per un utente.</span><span class="sxs-lookup"><span data-stu-id="b20b8-110">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b20b8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b20b8-111">Return value</span></span>

<span data-ttu-id="b20b8-112">Restituisce un valore pari a 0 (zero) se la richiesta **UserControlService** è stata accettata, 1 (uno) se la richiesta non è supportata e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="b20b8-112">Returns a value of 0 (zero) if the **UserControlService** request was accepted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="b20b8-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b20b8-113">Requirements</span></span>



| <span data-ttu-id="b20b8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b20b8-114">Requirement</span></span> | <span data-ttu-id="b20b8-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b20b8-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b20b8-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b20b8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b20b8-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b20b8-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b20b8-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b20b8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b20b8-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b20b8-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b20b8-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b20b8-120">Namespace</span></span><br/>                | <span data-ttu-id="b20b8-121">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="b20b8-121">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b20b8-122">MOF</span><span class="sxs-lookup"><span data-stu-id="b20b8-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b20b8-123"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b20b8-123"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b20b8-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b20b8-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b20b8-125"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b20b8-125"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b20b8-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b20b8-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="b20b8-127">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b20b8-127">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b20b8-128">**\_SystemDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="b20b8-128">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

