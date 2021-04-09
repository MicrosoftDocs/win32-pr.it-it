---
title: Proprietà TerminalServerPort di IVMGuestOS
description: Porta utilizzata da Servizi Desktop remoto nel sistema operativo guest.
ms.assetid: 25a9114a-0992-4a9d-997a-37138d389970
keywords:
- Proprietà TerminalServerPort Virtual PC
- Proprietà TerminalServerPort Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà TerminalServerPort
topic_type:
- apiref
api_name:
- IVMGuestOS.TerminalServerPort
- IVMGuestOS.get_TerminalServerPort
api_location:
- IVMGuestOS.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64415057eeeb91bfb85b664f5cbb44a66546005
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121195"
---
# <a name="ivmguestosterminalserverport-property"></a><span data-ttu-id="76acf-106">Proprietà IVMGuestOS:: TerminalServerPort</span><span class="sxs-lookup"><span data-stu-id="76acf-106">IVMGuestOS::TerminalServerPort property</span></span>

<span data-ttu-id="76acf-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="76acf-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="76acf-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="76acf-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="76acf-109">Porta utilizzata da Servizi Desktop remoto (precedentemente nota come servizi Terminal) nel sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="76acf-109">Port used by Remote Desktop Services (formerly known as Terminal Services) in the guest operating system.</span></span>

<span data-ttu-id="76acf-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="76acf-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="76acf-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76acf-111">Syntax</span></span>


```C++
HRESULT get_TerminalServerPort(
  [out, retval] long *tsPort = 3389
);
```



## <a name="property-value"></a><span data-ttu-id="76acf-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="76acf-112">Property value</span></span>

<span data-ttu-id="76acf-113">Restituisce la porta utilizzata da Servizi Desktop remoto nel sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="76acf-113">Returns the port used by Remote Desktop Services in the guest operating system.</span></span>



| <span data-ttu-id="76acf-114">Valore</span><span class="sxs-lookup"><span data-stu-id="76acf-114">Value</span></span>                                                                              | <span data-ttu-id="76acf-115">Significato</span><span class="sxs-lookup"><span data-stu-id="76acf-115">Meaning</span></span>                                       |
|------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="76acf-116"><dt>3389</dt></span><span class="sxs-lookup"><span data-stu-id="76acf-116"><dt>3389</dt></span></span> </dl>    | <span data-ttu-id="76acf-117">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="76acf-117">Default value</span></span><br/>                      |
| <dl> <span data-ttu-id="76acf-118"><dt>1 65535</dt></span><span class="sxs-lookup"><span data-stu-id="76acf-118"><dt>1 65535</dt></span></span> </dl> | <span data-ttu-id="76acf-119">Intervallo valido</span><span class="sxs-lookup"><span data-stu-id="76acf-119">Valid range</span></span><br/>                        |
| <dl> <span data-ttu-id="76acf-120"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="76acf-120"><dt>0</dt></span></span> </dl>       | <span data-ttu-id="76acf-121">Il valore di porta valido non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="76acf-121">Valid port value is not available.</span></span><br/> |



 

## <a name="error-codes"></a><span data-ttu-id="76acf-122">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="76acf-122">Error codes</span></span>



| <span data-ttu-id="76acf-123">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="76acf-123">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="76acf-124">Significato</span><span class="sxs-lookup"><span data-stu-id="76acf-124">Meaning</span></span>                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="76acf-125"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="76acf-125"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="76acf-126">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="76acf-126">The operation was successful.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="76acf-127"><dt>S \_ FALSE</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="76acf-127"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="76acf-128">Servizi Desktop remoto non è ancora inizializzato nel sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="76acf-128">Remote Desktop Services is not yet initialized in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="76acf-129"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="76acf-129"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="76acf-130">Il parametro *tsPort* è **null**.</span><span class="sxs-lookup"><span data-stu-id="76acf-130">The *tsPort* parameter is **NULL**.</span></span><br/>                                           |
| <dl> <span data-ttu-id="76acf-131"><dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="76acf-131"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="76acf-132">La macchina virtuale non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="76acf-132">The virtual machine is not running.</span></span><br/>                                           |
| <dl> <span data-ttu-id="76acf-133"><dt>Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="76acf-133"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="76acf-134">I componenti di integrazione non sono installati in questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="76acf-134">Integration components are not installed in this virtual machine.</span></span><br/>             |
| <dl> <span data-ttu-id="76acf-135"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="76acf-135"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="76acf-136">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="76acf-136">An unexpected error has occurred.</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="76acf-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="76acf-137">Remarks</span></span>

<span data-ttu-id="76acf-138">Il valore di questa proprietà non è valido a meno che la proprietà [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) non sia **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="76acf-138">The value of this property is not valid unless the [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) property is **VARIANT\_TRUE**.</span></span>

<span data-ttu-id="76acf-139">Se la proprietà [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) è **Variant \_ false** a causa di un errore di connessione sulla porta, il valore restituito dalla proprietà **TerminalServerPort** contiene il valore di errore.</span><span class="sxs-lookup"><span data-stu-id="76acf-139">If the [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) property is **VARIANT\_FALSE** due to a connection error on the port, then the value returned by the **TerminalServerPort** property contains the error value.</span></span>

## <a name="requirements"></a><span data-ttu-id="76acf-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76acf-140">Requirements</span></span>



| <span data-ttu-id="76acf-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="76acf-141">Requirement</span></span> | <span data-ttu-id="76acf-142">Valore</span><span class="sxs-lookup"><span data-stu-id="76acf-142">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="76acf-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76acf-143">Minimum supported client</span></span><br/> | <span data-ttu-id="76acf-144">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="76acf-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="76acf-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76acf-145">Minimum supported server</span></span><br/> | <span data-ttu-id="76acf-146">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="76acf-146">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="76acf-147">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="76acf-147">End of client support</span></span><br/>    | <span data-ttu-id="76acf-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="76acf-148">Windows 7</span></span><br/>                                                                      |
| <span data-ttu-id="76acf-149">IDL</span><span class="sxs-lookup"><span data-stu-id="76acf-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="76acf-150"><dt>IVMGuestOS. idl</dt></span><span class="sxs-lookup"><span data-stu-id="76acf-150"><dt>IVMGuestOS.idl</dt></span></span> </dl> |
| <span data-ttu-id="76acf-151">IID</span><span class="sxs-lookup"><span data-stu-id="76acf-151">IID</span></span><br/>                      | <span data-ttu-id="76acf-152">IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="76acf-152">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="76acf-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76acf-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76acf-154">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="76acf-154">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

