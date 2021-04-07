---
description: Inserisce il servizio rappresentato dall' \_ oggetto PrinterDriver Win32 nello stato interrotto.
ms.assetid: 0e730fe6-ff9f-4866-a255-be6d372f2d7d
ms.tgt_platform: multiple
title: Metodo StopService della classe Win32_PrinterDriver (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: faed7e9ed22ddcacbd8720e589463fd9a75fd87a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049197"
---
# <a name="stopservice-method-of-the-win32_printerdriver-class"></a><span data-ttu-id="11739-103">Metodo StopService della \_ classe PrinterDriver Win32</span><span class="sxs-lookup"><span data-stu-id="11739-103">StopService method of the Win32\_PrinterDriver class</span></span>

<span data-ttu-id="11739-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** posiziona il servizio rappresentato dall' [**oggetto \_ PrinterDriver Win32**](win32-printerdriver.md) nello stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="11739-104">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method places the service represented by the [**Win32\_PrinterDriver**](win32-printerdriver.md) object in the stopped state.</span></span>

<span data-ttu-id="11739-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="11739-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="11739-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="11739-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="11739-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="11739-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="11739-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="11739-108">Parameters</span></span>

<span data-ttu-id="11739-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="11739-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="11739-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="11739-110">Return value</span></span>

<span data-ttu-id="11739-111">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="11739-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="11739-112">Per i valori diversi da quelli elencati nell'elenco seguente, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants).</span><span class="sxs-lookup"><span data-stu-id="11739-112">For values different from those listed in the following list, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants).</span></span>

<dl> <dt>

<span data-ttu-id="11739-113">**0**</span><span class="sxs-lookup"><span data-stu-id="11739-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="11739-114">Il servizio è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="11739-114">Service successfully stopped.</span></span>

</dd> <dt>

<span data-ttu-id="11739-115">**1**</span><span class="sxs-lookup"><span data-stu-id="11739-115">**1**</span></span>
</dt> <dd>

<span data-ttu-id="11739-116">Richiesta non supportata.</span><span class="sxs-lookup"><span data-stu-id="11739-116">Request not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11739-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11739-117">Requirements</span></span>



| <span data-ttu-id="11739-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="11739-118">Requirement</span></span> | <span data-ttu-id="11739-119">Valore</span><span class="sxs-lookup"><span data-stu-id="11739-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="11739-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11739-120">Minimum supported client</span></span><br/> | <span data-ttu-id="11739-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11739-121">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="11739-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11739-122">Minimum supported server</span></span><br/> | <span data-ttu-id="11739-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11739-123">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="11739-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="11739-124">Namespace</span></span><br/>                | <span data-ttu-id="11739-125">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="11739-125">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="11739-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11739-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="11739-127"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="11739-127"><dt>Sdoias.h</dt></span></span> </dl>           |
| <span data-ttu-id="11739-128">MOF</span><span class="sxs-lookup"><span data-stu-id="11739-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11739-129"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11739-129"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="11739-130">DLL</span><span class="sxs-lookup"><span data-stu-id="11739-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11739-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11739-131"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="11739-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11739-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11739-133">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="11739-133">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="11739-134">**\_PrinterDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="11739-134">**Win32\_PrinterDriver**</span></span>](win32-printerdriver.md)
</dt> </dl>

 

