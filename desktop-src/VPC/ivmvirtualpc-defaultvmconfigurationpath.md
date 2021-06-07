---
title: Proprietà IVMVirtualPC DefaultVMConfigurationPath (VPCCOMInterfaces.h)
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
ms.openlocfilehash: 09f6370dfb868ec386e05f361240a74412f13a7d
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387637"
---
# <a name="ivmvirtualpcdefaultvmconfigurationpath-property"></a><span data-ttu-id="8c375-106">Proprietà IVMVirtualPC::D efaultVMConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="8c375-106">IVMVirtualPC::DefaultVMConfigurationPath property</span></span>

<span data-ttu-id="8c375-107">\[Virtual PC Windows non è più disponibile per l'uso a Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8c375-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8c375-108">Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]</span><span class="sxs-lookup"><span data-stu-id="8c375-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8c375-109">Recupera e imposta la directory predefinita in cui cercare i file di configurazione delle macchine virtuali disponibili.</span><span class="sxs-lookup"><span data-stu-id="8c375-109">Retrieves and sets the default directory to be searched for available virtual machine configuration files.</span></span>

<span data-ttu-id="8c375-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="8c375-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c375-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c375-111">Syntax</span></span>


```C++
HRESULT put_DefaultVMConfigurationPath(
  [in]          BSTR configurationPath
);

HRESULT get_DefaultVMConfigurationPath(
  [out, retval] BSTR *configurationPath
);
```



## <a name="property-value"></a><span data-ttu-id="8c375-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="8c375-112">Property value</span></span>

<span data-ttu-id="8c375-113">Specifica il percorso della directory per i file di configurazione predefiniti della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8c375-113">Specifies the directory path for the default virtual machine configuration files.</span></span> <span data-ttu-id="8c375-114">Nella stringa di percorso, una barra rovesciata ( ) può essere visualizzata \\ immediatamente prima del carattere Null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="8c375-114">In the path string, a backslash (\\) may appear immediately before the terminating null character.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8c375-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="8c375-115">Error codes</span></span>



| <span data-ttu-id="8c375-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="8c375-116">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="8c375-117">Significato</span><span class="sxs-lookup"><span data-stu-id="8c375-117">Meaning</span></span>                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8c375-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8c375-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="8c375-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="8c375-119">The operation was successful.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="8c375-120"><dt>E \_ Puntatore</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="8c375-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="8c375-121">Il *parametro configurationPath* è **NULL.**</span><span class="sxs-lookup"><span data-stu-id="8c375-121">The *configurationPath* parameter is **NULL**.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="8c375-122"><dt>HRESULT \_ DA \_ WIN32(FILE \_ DI ERRORE NON \_ \_ TROVATO) 0X80070002</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8c375-122"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="8c375-123">Il sistema non riesce a trovare la directory specificata dal *parametro configurationPath.*</span><span class="sxs-lookup"><span data-stu-id="8c375-123">The system cannot find the directory specified by the *configurationPath* parameter.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="8c375-124"><dt>HRESULT \_ FROM \_ WIN32(ERROR \_ PATH NOT \_ \_ FOUND) 0X80070003</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8c375-124"><dt>HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="8c375-125">Il sistema non riesce a trovare il percorso specificato dal *parametro configurationPath.*</span><span class="sxs-lookup"><span data-stu-id="8c375-125">The system cannot find the path specified by the *configurationPath* parameter.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="8c375-126"><dt>HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="8c375-126"><dt>HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="8c375-127">Il *parametro configurationPath* contiene un carattere non valido (uno dei seguenti: " \* ?<>/ \| ":").</span><span class="sxs-lookup"><span data-stu-id="8c375-127">The *configurationPath* parameter contains an invalid character (one of the following: "\*?<>/\|":").</span></span><br/>                                   |
| <dl> <span data-ttu-id="8c375-128"><dt>HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="8c375-128"><dt>HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="8c375-129">Il *parametro configurationPath* specifica un percorso vuoto o relativo.</span><span class="sxs-lookup"><span data-stu-id="8c375-129">The *configurationPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="8c375-130">È necessario un percorso assoluto.</span><span class="sxs-lookup"><span data-stu-id="8c375-130">An absolute path is required.</span></span><br/>                                          |
| <dl> <span data-ttu-id="8c375-131"><dt>HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="8c375-131"><dt>HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="8c375-132">Il percorso specificato dal *parametro configurationPath* è troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="8c375-132">The path specified by the *configurationPath* parameter is too long.</span></span> <span data-ttu-id="8c375-133">La lunghezza del percorso deve essere minore di **MAX \_ PATH** (260 caratteri).</span><span class="sxs-lookup"><span data-stu-id="8c375-133">The length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="8c375-134"><dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8c375-134"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="8c375-135">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="8c375-135">An unexpected error has occurred.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="8c375-136"><dt>Macchina virtuale \_ E \_ \_ VIRTUALIZZAZIONE HARDWARE \_ DISABILITATA</dt> <dt>0XA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="8c375-136"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="8c375-137">Il processore non supporta le estensioni haV (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="8c375-137">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                          |



## <a name="remarks"></a><span data-ttu-id="8c375-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c375-138">Remarks</span></span>

<span data-ttu-id="8c375-139">Per impostazione predefinita, questo valore della proprietà è impostato sulla directory seguente: "%LocalAppData% \\ Microsoft Windows Virtual PC Virtual \\ \\ \\ Machines".</span><span class="sxs-lookup"><span data-stu-id="8c375-139">By default, this property value is set to the following directory: "%LocalAppData%\\Microsoft\\Windows Virtual PC\\Virtual Machines\\".</span></span>

## <a name="requirements"></a><span data-ttu-id="8c375-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c375-140">Requirements</span></span>



| <span data-ttu-id="8c375-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c375-141">Requirement</span></span> | <span data-ttu-id="8c375-142">Valore</span><span class="sxs-lookup"><span data-stu-id="8c375-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c375-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c375-143">Minimum supported client</span></span><br/> | <span data-ttu-id="8c375-144">Solo app desktop di Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c375-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8c375-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c375-145">Minimum supported server</span></span><br/> | <span data-ttu-id="8c375-146">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8c375-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8c375-147">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="8c375-147">End of client support</span></span><br/>    | <span data-ttu-id="8c375-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8c375-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8c375-149">Prodotto</span><span class="sxs-lookup"><span data-stu-id="8c375-149">Product</span></span><br/>                  | <span data-ttu-id="8c375-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8c375-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8c375-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8c375-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c375-152"><dt>VPCCOMInterfaces.h</dt></span><span class="sxs-lookup"><span data-stu-id="8c375-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8c375-153">IID</span><span class="sxs-lookup"><span data-stu-id="8c375-153">IID</span></span><br/>                      | <span data-ttu-id="8c375-154">IID IVMVirtualPC è definito come \_ 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="8c375-154">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="8c375-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c375-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c375-156">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="8c375-156">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

