---
description: Il metodo StartService posiziona il servizio nello stato started.
ms.assetid: 0f221db1-29ad-4071-98d3-6d06e4f5e026
ms.tgt_platform: multiple
title: Metodo StartService della classe Win32_PrinterDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44e6fedb9e1d0edd9f355c654c7fe2cd25760ec7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304878"
---
# <a name="startservice-method-of-the-win32_printerdriver-class"></a><span data-ttu-id="450cd-103">Metodo StartService della \_ classe PrinterDriver Win32</span><span class="sxs-lookup"><span data-stu-id="450cd-103">StartService method of the Win32\_PrinterDriver class</span></span>

<span data-ttu-id="450cd-104">Il metodo **StartService** posiziona il servizio nello stato started.</span><span class="sxs-lookup"><span data-stu-id="450cd-104">The **StartService** method places the service in the started state.</span></span>

<span data-ttu-id="450cd-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="450cd-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="450cd-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="450cd-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="450cd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="450cd-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="450cd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="450cd-108">Parameters</span></span>

<span data-ttu-id="450cd-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="450cd-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="450cd-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="450cd-110">Return value</span></span>

<span data-ttu-id="450cd-111">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="450cd-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="450cd-112">Per i valori diversi da quelli elencati nell'elenco seguente, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants).</span><span class="sxs-lookup"><span data-stu-id="450cd-112">For values different from those listed in the following list, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants).</span></span>

<dl> <dt>

<span data-ttu-id="450cd-113">**0**</span><span class="sxs-lookup"><span data-stu-id="450cd-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="450cd-114">Il servizio è stato avviato correttamente.</span><span class="sxs-lookup"><span data-stu-id="450cd-114">Service successfully started.</span></span>

</dd> <dt>

<span data-ttu-id="450cd-115">**1**</span><span class="sxs-lookup"><span data-stu-id="450cd-115">**1**</span></span>
</dt> <dd>

<span data-ttu-id="450cd-116">Richiesta non supportata.</span><span class="sxs-lookup"><span data-stu-id="450cd-116">Request not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="450cd-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="450cd-117">Requirements</span></span>



| <span data-ttu-id="450cd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="450cd-118">Requirement</span></span> | <span data-ttu-id="450cd-119">Valore</span><span class="sxs-lookup"><span data-stu-id="450cd-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="450cd-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="450cd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="450cd-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="450cd-121">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="450cd-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="450cd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="450cd-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="450cd-123">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="450cd-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="450cd-124">Namespace</span></span><br/>                | <span data-ttu-id="450cd-125">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="450cd-125">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="450cd-126">MOF</span><span class="sxs-lookup"><span data-stu-id="450cd-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="450cd-127"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="450cd-127"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="450cd-128">DLL</span><span class="sxs-lookup"><span data-stu-id="450cd-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="450cd-129"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="450cd-129"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="450cd-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="450cd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="450cd-131">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="450cd-131">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="450cd-132">**\_PrinterDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="450cd-132">**Win32\_PrinterDriver**</span></span>](win32-printerdriver.md)
</dt> </dl>

 

