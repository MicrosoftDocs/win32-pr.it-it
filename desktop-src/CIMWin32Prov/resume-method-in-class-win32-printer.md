---
description: Riprende una coda di stampa sospesa.
ms.assetid: 6d6d21e9-f469-4e2c-9a89-3e9febe229fc
ms.tgt_platform: multiple
title: Metodo Resume della classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.Resume
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3eca8849fd1c5c449261dac1a9530f4da42e9482
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304577"
---
# <a name="resume-method-of-the-win32_printer-class"></a><span data-ttu-id="c0481-103">Metodo Resume della \_ classe Printer Win32</span><span class="sxs-lookup"><span data-stu-id="c0481-103">Resume method of the Win32\_Printer class</span></span>

<span data-ttu-id="c0481-104">Il metodo **Resume** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) riprende una coda di stampa sospesa.</span><span class="sxs-lookup"><span data-stu-id="c0481-104">The **Resume** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method resumes a paused print queue.</span></span>

<span data-ttu-id="c0481-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="c0481-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c0481-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c0481-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c0481-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0481-107">Syntax</span></span>


```mof
uint32 Resume();
```



## <a name="parameters"></a><span data-ttu-id="c0481-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c0481-108">Parameters</span></span>

<span data-ttu-id="c0481-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c0481-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c0481-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c0481-110">Return value</span></span>

<span data-ttu-id="c0481-111">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="c0481-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="c0481-112">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c0481-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c0481-113">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c0481-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c0481-114">**0**</span><span class="sxs-lookup"><span data-stu-id="c0481-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c0481-115">Operazione completata</span><span class="sxs-lookup"><span data-stu-id="c0481-115">Success</span></span>

</dd> <dt>

<span data-ttu-id="c0481-116">**5**</span><span class="sxs-lookup"><span data-stu-id="c0481-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="c0481-117">Accesso negato</span><span class="sxs-lookup"><span data-stu-id="c0481-117">Access Denied</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0481-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0481-118">Requirements</span></span>



| <span data-ttu-id="c0481-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0481-119">Requirement</span></span> | <span data-ttu-id="c0481-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c0481-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0481-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0481-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c0481-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0481-122">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="c0481-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0481-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c0481-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0481-124">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="c0481-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c0481-125">Namespace</span></span><br/>                | <span data-ttu-id="c0481-126">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="c0481-126">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="c0481-127">MOF</span><span class="sxs-lookup"><span data-stu-id="c0481-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0481-128"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0481-128"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0481-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c0481-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0481-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0481-130"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="c0481-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0481-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0481-132">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="c0481-132">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="c0481-133">**\_Stampante Win32**</span><span class="sxs-lookup"><span data-stu-id="c0481-133">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="c0481-134">**Pause (metodo)**</span><span class="sxs-lookup"><span data-stu-id="c0481-134">**Pause Method**</span></span>](pause-method-in-class-win32-printer.md)
</dt> </dl>

 

