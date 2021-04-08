---
title: Proprietà IVMVirtualPC DefaultVMConfigurationPath (VPCCOMInterfaces. h)
description: Directory predefinita in cui cercare i file di configurazione delle macchine virtuali disponibili.
ms.assetid: 9ae63198-e3f6-4dcb-8edb-85adfbbdca26
keywords:
- Proprietà DefaultVMConfigurationPath Virtual PC
- Proprietà DefaultVMConfigurationPath Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, proprietà DefaultVMConfigurationPath
topic_type:
- apiref
api_name:
- IVMVirtualPC.DefaultVMConfigurationPath
- IVMVirtualPC.get_DefaultVMConfigurationPath
- IVMVirtualPC.put_DefaultVMConfigurationPath
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e13fc2323cb15bdbeb8c42e61810a376e49b3988
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742730"
---
# <a name="ivmvirtualpcdefaultvmconfigurationpath-property"></a><span data-ttu-id="650bc-106">IVMVirtualPC::D Proprietà efaultVMConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="650bc-106">IVMVirtualPC::DefaultVMConfigurationPath property</span></span>

<span data-ttu-id="650bc-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="650bc-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="650bc-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="650bc-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="650bc-109">Recupera e imposta la directory predefinita in cui cercare i file di configurazione delle macchine virtuali disponibili.</span><span class="sxs-lookup"><span data-stu-id="650bc-109">Retrieves and sets the default directory to be searched for available virtual machine configuration files.</span></span>

<span data-ttu-id="650bc-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="650bc-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="650bc-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="650bc-111">Syntax</span></span>


```C++
HRESULT put_DefaultVMConfigurationPath(
  [in]          BSTR configurationPath
);

HRESULT get_DefaultVMConfigurationPath(
  [out, retval] BSTR *configurationPath
);
```



## <a name="property-value"></a><span data-ttu-id="650bc-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="650bc-112">Property value</span></span>

<span data-ttu-id="650bc-113">Specifica il percorso della directory per i file di configurazione predefiniti della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="650bc-113">Specifies the directory path for the default virtual machine configuration files.</span></span> <span data-ttu-id="650bc-114">Nella stringa di percorso, una barra rovesciata ( \) può apparire immediatamente prima del carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="650bc-114">In the path string, a backslash (\) may appear immediately before the terminating null character.</span></span>

## <a name="error-codes"></a><span data-ttu-id="650bc-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="650bc-115">Error codes</span></span>



| <span data-ttu-id="650bc-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="650bc-116">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="650bc-117">Significato</span><span class="sxs-lookup"><span data-stu-id="650bc-117">Meaning</span></span>                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="650bc-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="650bc-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="650bc-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="650bc-119">The operation was successful.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="650bc-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="650bc-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="650bc-121">Il parametro *configurationPath* è **null**.</span><span class="sxs-lookup"><span data-stu-id="650bc-121">The *configurationPath* parameter is **NULL**.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="650bc-122"><dt>HRESULT \_ DA \_ Win32 (file degli errori \_ \_ non \_ trovato)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="650bc-122"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="650bc-123">Il sistema non è in grado di trovare la directory specificata dal parametro *configurationPath* .</span><span class="sxs-lookup"><span data-stu-id="650bc-123">The system cannot find the directory specified by the *configurationPath* parameter.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="650bc-124"><dt>HRESULT \_ DA \_ Win32 ( \_ percorso errore \_ non \_ trovato)</dt> <dt>0 x 80070003</dt></span><span class="sxs-lookup"><span data-stu-id="650bc-124"><dt>HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="650bc-125">Il sistema non è in grado di trovare il percorso specificato dal parametro *configurationPath* .</span><span class="sxs-lookup"><span data-stu-id="650bc-125">The system cannot find the path specified by the *configurationPath* parameter.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="650bc-126"><dt>HRESULT \_ DA \_ Win32 (errore \_ nome non valido \_ )</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="650bc-126"><dt>HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="650bc-127">Il parametro *configurationPath* contiene un carattere non valido (uno dei seguenti: " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="650bc-127">The *configurationPath* parameter contains an invalid character (one of the following: "\*?<>/\|":").</span></span><br/>                                   |
| <dl> <span data-ttu-id="650bc-128"><dt>HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="650bc-128"><dt>HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="650bc-129">Il parametro *configurationPath* specifica un percorso vuoto o relativo.</span><span class="sxs-lookup"><span data-stu-id="650bc-129">The *configurationPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="650bc-130">È necessario specificare un percorso assoluto.</span><span class="sxs-lookup"><span data-stu-id="650bc-130">An absolute path is required.</span></span><br/>                                          |
| <dl> <span data-ttu-id="650bc-131"><dt>HRESULT \_ Da \_ Win32 (overflow del buffer degli errori \_ \_ )</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="650bc-131"><dt>HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="650bc-132">Il percorso specificato dal parametro *configurationPath* è troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="650bc-132">The path specified by the *configurationPath* parameter is too long.</span></span> <span data-ttu-id="650bc-133">La lunghezza del percorso deve essere minore di **Max \_ path** (260) caratteri.</span><span class="sxs-lookup"><span data-stu-id="650bc-133">The length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="650bc-134"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="650bc-134"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="650bc-135">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="650bc-135">An unexpected error has occurred.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="650bc-136"><dt>Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="650bc-136"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="650bc-137">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="650bc-137">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                          |



## <a name="remarks"></a><span data-ttu-id="650bc-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="650bc-138">Remarks</span></span>

<span data-ttu-id="650bc-139">Per impostazione predefinita, il valore di questa proprietà è impostato sulla directory seguente: "% LocalAppData% \\ Microsoft \\ Windows Virtual PC \\ macchine virtuali \\ ".</span><span class="sxs-lookup"><span data-stu-id="650bc-139">By default, this property value is set to the following directory: "%LocalAppData%\\Microsoft\\Windows Virtual PC\\Virtual Machines\\".</span></span>

## <a name="requirements"></a><span data-ttu-id="650bc-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="650bc-140">Requirements</span></span>



| <span data-ttu-id="650bc-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="650bc-141">Requirement</span></span> | <span data-ttu-id="650bc-142">Valore</span><span class="sxs-lookup"><span data-stu-id="650bc-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="650bc-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="650bc-143">Minimum supported client</span></span><br/> | <span data-ttu-id="650bc-144">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="650bc-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="650bc-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="650bc-145">Minimum supported server</span></span><br/> | <span data-ttu-id="650bc-146">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="650bc-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="650bc-147">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="650bc-147">End of client support</span></span><br/>    | <span data-ttu-id="650bc-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="650bc-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="650bc-149">Prodotto</span><span class="sxs-lookup"><span data-stu-id="650bc-149">Product</span></span><br/>                  | <span data-ttu-id="650bc-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="650bc-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="650bc-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="650bc-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="650bc-152"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="650bc-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="650bc-153">IID</span><span class="sxs-lookup"><span data-stu-id="650bc-153">IID</span></span><br/>                      | <span data-ttu-id="650bc-154">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="650bc-154">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="650bc-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="650bc-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="650bc-156">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="650bc-156">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

