---
description: È possibile usare il metodo AddAsString dell'oggetto SWbemPrivilegeSet per aggiungere un privilegio a una raccolta SWbemPrivilegeSet usando una stringa di privilegio.
ms.assetid: 729ed4e3-2c5c-4bb4-acc6-cf9ad0d5eaf1
ms.tgt_platform: multiple
title: Metodo SWbemPrivilegeSet. AddAsString (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b3a740141b14766080a09d01b36b5c0202351eda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318502"
---
# <a name="swbemprivilegesetaddasstring-method"></a><span data-ttu-id="8d4f8-103">SWbemPrivilegeSet. AddAsString, metodo</span><span class="sxs-lookup"><span data-stu-id="8d4f8-103">SWbemPrivilegeSet.AddAsString method</span></span>

<span data-ttu-id="8d4f8-104">È possibile usare il metodo **AddAsString** dell'oggetto [**SWbemPrivilegeSet**](swbemprivilegeset.md) per aggiungere un privilegio a una raccolta **SWbemPrivilegeSet** usando una stringa di privilegio.</span><span class="sxs-lookup"><span data-stu-id="8d4f8-104">You can use the **AddAsString** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object to add a privilege to an **SWbemPrivilegeSet** collection using a privilege string.</span></span> <span data-ttu-id="8d4f8-105">Utilizzare questo metodo per aggiungere un privilegio o per abilitare un privilegio per gli oggetti [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="8d4f8-105">Use this method to add a privilege or to enable a privilege for [**SWbemSecurity**](swbemsecurity.md) objects.</span></span> <span data-ttu-id="8d4f8-106">Vedere [esecuzione di operazioni con privilegi tramite VBScript](executing-privileged-operations-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="8d4f8-106">See [Executing Privileged Operations Using VBScript](executing-privileged-operations-using-vbscript.md).</span></span>

<span data-ttu-id="8d4f8-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="8d4f8-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8d4f8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d4f8-108">Syntax</span></span>


```VB
objPrivilege = .AddAsString( _
  ByVal strPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a><span data-ttu-id="8d4f8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8d4f8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d4f8-110">*strPrivilege*</span><span class="sxs-lookup"><span data-stu-id="8d4f8-110">*strPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="8d4f8-111">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8d4f8-111">Required.</span></span> <span data-ttu-id="8d4f8-112">Una delle stringhe dei privilegi.</span><span class="sxs-lookup"><span data-stu-id="8d4f8-112">One of the privilege strings.</span></span> <span data-ttu-id="8d4f8-113">Per un elenco completo di queste stringhe e delle costanti WMI associate, vedere [**costanti Privilege**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="8d4f8-113">For a complete list of these strings and the associated WMI constants, see [**Privilege Constants**](privilege-constants.md).</span></span> <span data-ttu-id="8d4f8-114">Ogni stringa di privilegio rappresenta un privilegio specifico.</span><span class="sxs-lookup"><span data-stu-id="8d4f8-114">Every privilege string represents a specific privilege.</span></span> <span data-ttu-id="8d4f8-115">Ad esempio, per aggiungere il privilegio utilizzato da per arrestare un computer, utilizzare la stringa **SeShutdownPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="8d4f8-115">For example, to add the privilege that use to shut down a computer system, use the **SeShutdownPrivilege** string.</span></span>

</dd> <dt>

<span data-ttu-id="8d4f8-116">*bIsEnabled* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="8d4f8-116">*bIsEnabled* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8d4f8-117">Valore booleano che Abilita o Disabilita questo privilegio.</span><span class="sxs-lookup"><span data-stu-id="8d4f8-117">Boolean value that enables or disables this privilege.</span></span> <span data-ttu-id="8d4f8-118">Il valore predefinito è **True**.</span><span class="sxs-lookup"><span data-stu-id="8d4f8-118">The default value is **True**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d4f8-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8d4f8-119">Return value</span></span>

<span data-ttu-id="8d4f8-120">Se ha esito positivo, questo metodo restituisce un oggetto [**SWbemPrivilege**](swbemprivilege.md) che rappresenta il nuovo privilegio.</span><span class="sxs-lookup"><span data-stu-id="8d4f8-120">If successful, this method returns an [**SWbemPrivilege**](swbemprivilege.md) object that represents the new privilege.</span></span> <span data-ttu-id="8d4f8-121">In caso contrario, viene restituito un oggetto null.</span><span class="sxs-lookup"><span data-stu-id="8d4f8-121">Otherwise, a null object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8d4f8-122">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="8d4f8-122">Error codes</span></span>

<span data-ttu-id="8d4f8-123">Al termine del metodo **AddAsString** , l'oggetto **Err** può contenere il codice di errore riportato nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="8d4f8-123">Upon the completion of the **AddAsString** method, the **Err** object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="8d4f8-124">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="8d4f8-124">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="8d4f8-125">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="8d4f8-125">Unspecified error.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="8d4f8-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="8d4f8-126">Examples</span></span>

<span data-ttu-id="8d4f8-127">L'esempio di codice VBScript seguente crea una nuova porta per un server di stampa usando [**Win32 \_ TCPIPPrinterPort**](/windows/desktop/CIMWin32Prov/win32-tcpipprinterport).</span><span class="sxs-lookup"><span data-stu-id="8d4f8-127">The following VBScript code example creates a new port for a print server using [**Win32\_TCPIPPrinterPort**](/windows/desktop/CIMWin32Prov/win32-tcpipprinterport).</span></span> <span data-ttu-id="8d4f8-128">Per questa operazione è necessario **SeLoadDriverPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="8d4f8-128">The **SeLoadDriverPrivilege** is required for this operation.</span></span> <span data-ttu-id="8d4f8-129">Vedere [esecuzione di operazioni con privilegi](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="8d4f8-129">See [Executing Privileged Operations](executing-privileged-operations.md).</span></span>


```VB
Set objWMIService = GetObject("Winmgmts:")
objWMIService.Security_.Privileges. _
    AddAsString "SeLoadDriverPrivilege", True
Set objNewPort = objWMIService.Get _
    ("Win32_TCPIPPrinterPort").SpawnInstance_
objNewPort.Name = "IP_111.222.111.11"
objNewPort.Protocol = 1
objNewPort.HostAddress = "111.222.111.11"
objNewPort.PortNumber = "9999"
objNewPort.SNMPEnabled = False
objNewPort.Put_
```



<span data-ttu-id="8d4f8-130">Un esempio di codice che usa questo metodo è descritto anche nell'argomento [**SWbemPrivilegeSet**](swbemprivilegeset.md) .</span><span class="sxs-lookup"><span data-stu-id="8d4f8-130">A code example using this method is also described in the [**SWbemPrivilegeSet**](swbemprivilegeset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d4f8-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d4f8-131">Requirements</span></span>



| <span data-ttu-id="8d4f8-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d4f8-132">Requirement</span></span> | <span data-ttu-id="8d4f8-133">Valore</span><span class="sxs-lookup"><span data-stu-id="8d4f8-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d4f8-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d4f8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="8d4f8-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d4f8-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8d4f8-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d4f8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="8d4f8-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d4f8-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8d4f8-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8d4f8-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d4f8-139"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d4f8-139"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8d4f8-140">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="8d4f8-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="8d4f8-141"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8d4f8-141"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8d4f8-142">DLL</span><span class="sxs-lookup"><span data-stu-id="8d4f8-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d4f8-143"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d4f8-143"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8d4f8-144">CLSID</span><span class="sxs-lookup"><span data-stu-id="8d4f8-144">CLSID</span></span><br/>                    | <span data-ttu-id="8d4f8-145">\_SWBEMPRIVILEGESET CLSID</span><span class="sxs-lookup"><span data-stu-id="8d4f8-145">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="8d4f8-146">IID</span><span class="sxs-lookup"><span data-stu-id="8d4f8-146">IID</span></span><br/>                      | <span data-ttu-id="8d4f8-147">\_ISWBEMPRIVILEGESET IID</span><span class="sxs-lookup"><span data-stu-id="8d4f8-147">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="8d4f8-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d4f8-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d4f8-149">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="8d4f8-149">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="8d4f8-150">**SWbemPrivilegeSet. Add**</span><span class="sxs-lookup"><span data-stu-id="8d4f8-150">**SWbemPrivilegeSet.Add**</span></span>](swbemprivilegeset-add.md)
</dt> <dt>

[<span data-ttu-id="8d4f8-151">**SWbemPrivilegeSet. Remove**</span><span class="sxs-lookup"><span data-stu-id="8d4f8-151">**SWbemPrivilegeSet.Remove**</span></span>](swbemprivilegeset-remove.md)
</dt> <dt>

[<span data-ttu-id="8d4f8-152">**WbemPrivilegeEnum**</span><span class="sxs-lookup"><span data-stu-id="8d4f8-152">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="8d4f8-153">**Costanti Privilege**</span><span class="sxs-lookup"><span data-stu-id="8d4f8-153">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> <dt>

[<span data-ttu-id="8d4f8-154">Esecuzione di operazioni con privilegi</span><span class="sxs-lookup"><span data-stu-id="8d4f8-154">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="8d4f8-155">Esecuzione di operazioni con privilegi tramite VBScript</span><span class="sxs-lookup"><span data-stu-id="8d4f8-155">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

