---
description: 'Metodo IShellDispatch2.GetSystemInformation: recupera le informazioni di sistema.'
ms.assetid: 57c066e3-080f-4ecc-b56e-877f0569e901
title: Metodo IShellDispatch2.GetSystemInformation (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.GetSystemInformation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a81ac091dc1905c1cbcd2c41575c907ce957e60c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117109"
---
# <a name="ishelldispatch2getsysteminformation-method"></a><span data-ttu-id="6ed24-103">Metodo IShellDispatch2.GetSystemInformation</span><span class="sxs-lookup"><span data-stu-id="6ed24-103">IShellDispatch2.GetSystemInformation method</span></span>

<span data-ttu-id="6ed24-104">Recupera le informazioni di sistema.</span><span class="sxs-lookup"><span data-stu-id="6ed24-104">Retrieves system information.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ed24-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6ed24-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.GetSystemInformation(
  sName
)
```


```VB

IShellDispatch2.GetSystemInformation( _
  ByVal sName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="6ed24-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6ed24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ed24-107">*sName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6ed24-107">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ed24-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="6ed24-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="6ed24-109">Valore **String** che specifica le informazioni di sistema richieste.</span><span class="sxs-lookup"><span data-stu-id="6ed24-109">A **String** that specifies the system information that is being requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ed24-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6ed24-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="6ed24-111">JScript</span><span class="sxs-lookup"><span data-stu-id="6ed24-111">JScript</span></span>

<span data-ttu-id="6ed24-112">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="6ed24-112">Type: **Variant**</span></span>

<span data-ttu-id="6ed24-113">Restituisce il valore delle informazioni di sistema richieste.</span><span class="sxs-lookup"><span data-stu-id="6ed24-113">Returns the value of the requested system information.</span></span> <span data-ttu-id="6ed24-114">Il tipo restituito dipende dalle informazioni di sistema richieste.</span><span class="sxs-lookup"><span data-stu-id="6ed24-114">The return type depends on which system information is requested.</span></span> <span data-ttu-id="6ed24-115">Vedere la sezione Osservazioni per informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="6ed24-115">See the Remarks section for details.</span></span>

### <a name="vb"></a><span data-ttu-id="6ed24-116">VB</span><span class="sxs-lookup"><span data-stu-id="6ed24-116">VB</span></span>

<span data-ttu-id="6ed24-117">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="6ed24-117">Type: **Variant**</span></span>

<span data-ttu-id="6ed24-118">Restituisce il valore delle informazioni di sistema richieste.</span><span class="sxs-lookup"><span data-stu-id="6ed24-118">Returns the value of the requested system information.</span></span> <span data-ttu-id="6ed24-119">Il tipo restituito dipende dalle informazioni di sistema richieste.</span><span class="sxs-lookup"><span data-stu-id="6ed24-119">The return type depends on which system information is requested.</span></span> <span data-ttu-id="6ed24-120">Vedere la sezione Osservazioni per informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="6ed24-120">See the Remarks section for details.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ed24-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="6ed24-121">Remarks</span></span>

<span data-ttu-id="6ed24-122">Questo metodo viene implementato e accessibile tramite il [**metodo Shell.GetSystemInformation.**](./shell-getsysteminformation.md)</span><span class="sxs-lookup"><span data-stu-id="6ed24-122">This method is implemented and accessed through the [**Shell.GetSystemInformation**](./shell-getsysteminformation.md) method.</span></span>

<span data-ttu-id="6ed24-123">Questo metodo può essere usato per richiedere molti valori di informazioni di sistema.</span><span class="sxs-lookup"><span data-stu-id="6ed24-123">This method can be used to request many system information values.</span></span> <span data-ttu-id="6ed24-124">Nella tabella seguente viene specificato *il valore sName* usato per richiedere le informazioni e il tipo associato del valore restituito.</span><span class="sxs-lookup"><span data-stu-id="6ed24-124">The following table gives the *sName* value that is used to request the information and the associated type of the returned value.</span></span>



<span data-ttu-id="6ed24-125">*sName*</span><span class="sxs-lookup"><span data-stu-id="6ed24-125">*sName*</span></span>

<span data-ttu-id="6ed24-126">Tipo restituito</span><span class="sxs-lookup"><span data-stu-id="6ed24-126">Return type</span></span>

<span data-ttu-id="6ed24-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ed24-127">Description</span></span>

<span data-ttu-id="6ed24-128">DirectoryServiceAvailable</span><span class="sxs-lookup"><span data-stu-id="6ed24-128">DirectoryServiceAvailable</span></span>

<span data-ttu-id="6ed24-129">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="6ed24-129">**Boolean**</span></span>

<span data-ttu-id="6ed24-130">Impostare su **true se** il servizio directory è disponibile. in caso contrario, **false.**</span><span class="sxs-lookup"><span data-stu-id="6ed24-130">Set to **true** if the directory service is available; otherwise, **false**.</span></span>

<span data-ttu-id="6ed24-131">DoubleClickTime</span><span class="sxs-lookup"><span data-stu-id="6ed24-131">DoubleClickTime</span></span>

<span data-ttu-id="6ed24-132">**Integer**</span><span class="sxs-lookup"><span data-stu-id="6ed24-132">**Integer**</span></span>

<span data-ttu-id="6ed24-133">Tempo di doppio clic, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="6ed24-133">The double-click time, in milliseconds.</span></span>

<span data-ttu-id="6ed24-134">ProcessorLevel</span><span class="sxs-lookup"><span data-stu-id="6ed24-134">ProcessorLevel</span></span>

<span data-ttu-id="6ed24-135">**Integer**</span><span class="sxs-lookup"><span data-stu-id="6ed24-135">**Integer**</span></span>

<span data-ttu-id="6ed24-136">**Windows Vista e versioni successive.**</span><span class="sxs-lookup"><span data-stu-id="6ed24-136">**Windows Vista and later**.</span></span> <span data-ttu-id="6ed24-137">Livello del processore.</span><span class="sxs-lookup"><span data-stu-id="6ed24-137">The processor level.</span></span> <span data-ttu-id="6ed24-138">Restituisce rispettivamente 3, 4 o 5 per i processori x386, x486 e Pentium.</span><span class="sxs-lookup"><span data-stu-id="6ed24-138">Returns 3, 4, or 5, for x386, x486, and Pentium-level processors, respectively.</span></span>

<span data-ttu-id="6ed24-139">ProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="6ed24-139">ProcessorSpeed</span></span>

<span data-ttu-id="6ed24-140">**Integer**</span><span class="sxs-lookup"><span data-stu-id="6ed24-140">**Integer**</span></span>

<span data-ttu-id="6ed24-141">Velocità del processore, in megahertz (MHz).</span><span class="sxs-lookup"><span data-stu-id="6ed24-141">The processor speed, in megahertz (MHz).</span></span>

<span data-ttu-id="6ed24-142">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="6ed24-142">ProcessorArchitecture</span></span>

<span data-ttu-id="6ed24-143">**Integer**</span><span class="sxs-lookup"><span data-stu-id="6ed24-143">**Integer**</span></span>

<span data-ttu-id="6ed24-144">Architettura del processore.</span><span class="sxs-lookup"><span data-stu-id="6ed24-144">The processor architecture.</span></span> <span data-ttu-id="6ed24-145">Per informazioni dettagliate, vedere la discussione sul **membro wProcessorArchitecture** della [**struttura SYSTEM \_ INFO.**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info)</span><span class="sxs-lookup"><span data-stu-id="6ed24-145">For details, see the discussion of the **wProcessorArchitecture** member of the [**SYSTEM\_INFO**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span>

<span data-ttu-id="6ed24-146">PhysicalMemoryInstalled</span><span class="sxs-lookup"><span data-stu-id="6ed24-146">PhysicalMemoryInstalled</span></span>

<span data-ttu-id="6ed24-147">**Integer**</span><span class="sxs-lookup"><span data-stu-id="6ed24-147">**Integer**</span></span>

<span data-ttu-id="6ed24-148">Quantità di memoria fisica installata, in byte.</span><span class="sxs-lookup"><span data-stu-id="6ed24-148">The amount of physical memory installed, in bytes.</span></span>

<span data-ttu-id="6ed24-149">Gli elementi seguenti sono validi solo in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6ed24-149">The following are valid only on Windows XP.</span></span>

<span data-ttu-id="6ed24-150">IsOS \_ Professional</span><span class="sxs-lookup"><span data-stu-id="6ed24-150">IsOS\_Professional</span></span>

<span data-ttu-id="6ed24-151">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="6ed24-151">**Boolean**</span></span>

<span data-ttu-id="6ed24-152">Impostare su **true se** il sistema operativo è Windows XP Professional Edition; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="6ed24-152">Set to **true** if the operating system is Windows XP Professional Edition; otherwise, **false**.</span></span>

<span data-ttu-id="6ed24-153">IsOS \_ Personal</span><span class="sxs-lookup"><span data-stu-id="6ed24-153">IsOS\_Personal</span></span>

<span data-ttu-id="6ed24-154">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="6ed24-154">**Boolean**</span></span>

<span data-ttu-id="6ed24-155">Impostare su **true se** il sistema operativo è Windows XP Home Edition; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="6ed24-155">Set to **true** if the operating system is Windows XP Home Edition; otherwise, **false**.</span></span>

<span data-ttu-id="6ed24-156">Quanto segue è valido solo in Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6ed24-156">The following is valid only on Windows XP and later.</span></span>

<span data-ttu-id="6ed24-157">Membro di dominio IsOS \_</span><span class="sxs-lookup"><span data-stu-id="6ed24-157">IsOS\_DomainMember</span></span>

<span data-ttu-id="6ed24-158">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="6ed24-158">**Boolean**</span></span>

<span data-ttu-id="6ed24-159">Impostare su **true se** il computer è membro di un dominio. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="6ed24-159">Set to **true** if the computer is a member of a domain; otherwise, **false**.</span></span>



 

<span data-ttu-id="6ed24-160">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6ed24-160">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="6ed24-161">Esempio</span><span class="sxs-lookup"><span data-stu-id="6ed24-161">Examples</span></span>

<span data-ttu-id="6ed24-162">Gli esempi seguenti illustrano l'uso **di GetSystemInformation** per JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="6ed24-162">The following examples show the use of **GetSystemInformation** for JScript and VBScript.</span></span>

<span data-ttu-id="6ed24-163">Jscript:</span><span class="sxs-lookup"><span data-stu-id="6ed24-163">JScript:</span></span>


```JScript
<script language="JavaScript">
    function fnGetSystemInformationJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;

        vReturn = objShell.GetSystemInformation("ProcessorLevel");
        document.write(vReturn);
    }
</script>
```



<span data-ttu-id="6ed24-164">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="6ed24-164">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnGetSystemInformationVB()
        dim objShell
        dim vReturn

        set objShell = CreateObject("shell.application")

        vReturn = objShell.GetSystemInformation("ProcessorLevel")
        document.write(vReturn)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="6ed24-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ed24-165">Requirements</span></span>



| <span data-ttu-id="6ed24-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ed24-166">Requirement</span></span> | <span data-ttu-id="6ed24-167">Valore</span><span class="sxs-lookup"><span data-stu-id="6ed24-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ed24-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ed24-168">Minimum supported client</span></span><br/> | <span data-ttu-id="6ed24-169">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6ed24-169">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6ed24-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ed24-170">Minimum supported server</span></span><br/> | <span data-ttu-id="6ed24-171">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6ed24-171">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6ed24-172">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6ed24-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ed24-173"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="6ed24-173"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="6ed24-174">Idl</span><span class="sxs-lookup"><span data-stu-id="6ed24-174">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6ed24-175"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="6ed24-175"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="6ed24-176">DLL</span><span class="sxs-lookup"><span data-stu-id="6ed24-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ed24-177"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="6ed24-177"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
