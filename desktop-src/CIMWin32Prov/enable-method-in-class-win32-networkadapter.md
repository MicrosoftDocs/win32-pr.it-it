---
description: Abilita la scheda di rete.
ms.assetid: ceb71e1b-5107-420f-a677-814307340469
ms.tgt_platform: multiple
title: Metodo Enable della classe Win32_NetworkAdapter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapter.Enable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7a7653d0bcda28ca333bc5c70bdcd69bce382787
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225609"
---
# <a name="enable-method-of-the-win32_networkadapter-class"></a><span data-ttu-id="e53f9-103">Metodo Enable della classe Win32 \_ NetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="e53f9-103">Enable method of the Win32\_NetworkAdapter class</span></span>

<span data-ttu-id="e53f9-104">Il metodo **enable Abilita** la scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="e53f9-104">The **Enable** method enables the network adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="e53f9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e53f9-105">Syntax</span></span>


```mof
uint32 Enable();
```



## <a name="parameters"></a><span data-ttu-id="e53f9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e53f9-106">Parameters</span></span>

<span data-ttu-id="e53f9-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e53f9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e53f9-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e53f9-108">Return value</span></span>

<span data-ttu-id="e53f9-109">Restituisce zero (0) per indicare l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="e53f9-109">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="e53f9-110">Qualsiasi altro numero indica un errore.</span><span class="sxs-lookup"><span data-stu-id="e53f9-110">Any other number indicates an error.</span></span> <span data-ttu-id="e53f9-111">Per i codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="e53f9-111">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="remarks"></a><span data-ttu-id="e53f9-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="e53f9-112">Remarks</span></span>

<span data-ttu-id="e53f9-113">È possibile che si verifichino problemi durante l'uso di questo metodo se l'applicazione non è amministratore ad accedere a privilidges.</span><span class="sxs-lookup"><span data-stu-id="e53f9-113">You may experience difficulty using this method if your application does not administrator access privilidges.</span></span>

## <a name="examples"></a><span data-ttu-id="e53f9-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="e53f9-114">Examples</span></span>

<span data-ttu-id="e53f9-115">Nell'esempio di script Visual Basic seguente viene abilitata la prima scheda di rete e viene visualizzato lo stato della proprietà **NetEnabled** .</span><span class="sxs-lookup"><span data-stu-id="e53f9-115">The following Visual Basic Script example enables the first network adapter and shows the status of the **NetEnabled** property.</span></span> <span data-ttu-id="e53f9-116">Per ulteriori informazioni, vedere [**SWbemObjectSet. ItemIndex**](/windows/desktop/wmisdk/swbemobjectset-itemindex).</span><span class="sxs-lookup"><span data-stu-id="e53f9-116">For more information, see [**SWbemObjectSet.ItemIndex**](/windows/desktop/wmisdk/swbemobjectset-itemindex).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colAdapters = _
    objWMIService.Execquery_
        ("Select * from Win32_NetworkAdapter Where NetEnabled=False")
For Each Adapter in colAdapters
    WScript.Echo Adapter.DeviceId & "    " & Adapter.Name
Next
errReturn = colAdapters.ItemIndex(0).Enable()
If errReturn <> 0 Then
    WScript.Echo "Enable Network adapter failed for adapter= "_
        & colAdapters.ItemIndex(0).DeviceId
Else 
    WScript.Echo "Enable Network adapter succeeded for adapter= "_
        & colAdapters.ItemIndex(0).DeviceId 
End If 
WScript.Echo "NetEnabled= " & colAdapters.ItemIndex(0).NetEnabled
```



## <a name="requirements"></a><span data-ttu-id="e53f9-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e53f9-117">Requirements</span></span>



| <span data-ttu-id="e53f9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e53f9-118">Requirement</span></span> | <span data-ttu-id="e53f9-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e53f9-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e53f9-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e53f9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e53f9-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e53f9-121">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e53f9-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e53f9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e53f9-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e53f9-123">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e53f9-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e53f9-124">Namespace</span></span><br/>                | <span data-ttu-id="e53f9-125">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="e53f9-125">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e53f9-126">MOF</span><span class="sxs-lookup"><span data-stu-id="e53f9-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e53f9-127"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e53f9-127"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e53f9-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e53f9-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e53f9-129"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e53f9-129"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e53f9-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e53f9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e53f9-131">**\_NetworkAdapter Win32**</span><span class="sxs-lookup"><span data-stu-id="e53f9-131">**Win32\_NetworkAdapter**</span></span>](win32-networkadapter.md)
</dt> <dt>

[<span data-ttu-id="e53f9-132">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="e53f9-132">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="e53f9-133">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="e53f9-133">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

