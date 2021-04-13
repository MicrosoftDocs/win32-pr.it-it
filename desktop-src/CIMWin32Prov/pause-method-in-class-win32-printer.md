---
description: Mette in pausa la coda di stampa.
ms.assetid: 0f425318-a7c0-4bba-bb44-e7635fa3ca03
ms.tgt_platform: multiple
title: Metodo pause della classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.Pause
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12d7e84351d77730b580242a58b38d7506af451a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401500"
---
# <a name="pause-method-of-the-win32_printer-class"></a><span data-ttu-id="e8355-103">Metodo pause della \_ classe Printer Win32</span><span class="sxs-lookup"><span data-stu-id="e8355-103">Pause method of the Win32\_Printer class</span></span>

<span data-ttu-id="e8355-104">Il metodo **Sospendi** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) sospende la coda di stampa.</span><span class="sxs-lookup"><span data-stu-id="e8355-104">The **Pause** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method pauses the print queue.</span></span> <span data-ttu-id="e8355-105">Nessun processo è in grado di stampare finché la coda non viene ripresa.</span><span class="sxs-lookup"><span data-stu-id="e8355-105">No jobs can print until the queue is resumed.</span></span>

<span data-ttu-id="e8355-106">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="e8355-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e8355-107">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e8355-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e8355-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8355-108">Syntax</span></span>


```mof
uint32 Pause();
```



## <a name="parameters"></a><span data-ttu-id="e8355-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8355-109">Parameters</span></span>

<span data-ttu-id="e8355-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e8355-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e8355-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8355-111">Return value</span></span>

<span data-ttu-id="e8355-112">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="e8355-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="e8355-113">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="e8355-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="e8355-114">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="e8355-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="e8355-115">**0**</span><span class="sxs-lookup"><span data-stu-id="e8355-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="e8355-116">Operazione completata</span><span class="sxs-lookup"><span data-stu-id="e8355-116">Success</span></span>

</dd> <dt>

<span data-ttu-id="e8355-117">**5**</span><span class="sxs-lookup"><span data-stu-id="e8355-117">**5**</span></span>
</dt> <dd>

<span data-ttu-id="e8355-118">Accesso negato</span><span class="sxs-lookup"><span data-stu-id="e8355-118">Access Denied</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8355-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8355-119">Requirements</span></span>



| <span data-ttu-id="e8355-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8355-120">Requirement</span></span> | <span data-ttu-id="e8355-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e8355-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8355-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8355-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e8355-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8355-123">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="e8355-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8355-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e8355-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8355-125">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="e8355-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e8355-126">Namespace</span></span><br/>                | <span data-ttu-id="e8355-127">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="e8355-127">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="e8355-128">MOF</span><span class="sxs-lookup"><span data-stu-id="e8355-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8355-129"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8355-129"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="e8355-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e8355-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8355-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8355-131"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="e8355-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8355-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8355-133">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="e8355-133">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="e8355-134">**\_Stampante Win32**</span><span class="sxs-lookup"><span data-stu-id="e8355-134">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="e8355-135">**Metodo Resume**</span><span class="sxs-lookup"><span data-stu-id="e8355-135">**Resume method**</span></span>](resume-method-in-class-win32-printer.md)
</dt> </dl>

 

