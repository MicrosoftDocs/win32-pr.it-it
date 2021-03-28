---
description: Recupera le informazioni di sistema.
ms.assetid: 94C10DD6-FE49-4dd4-AEED-69B73A75EDEF
title: Metodo Shell. GetSystemInformation (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.GetSystemInformation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 2ad7a865ba6ac5b62bc8a9b5ac105c0ef166d574
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980626"
---
# <a name="shellgetsysteminformation-method"></a><span data-ttu-id="745ee-103">Shell. GetSystemInformation, metodo</span><span class="sxs-lookup"><span data-stu-id="745ee-103">Shell.GetSystemInformation method</span></span>

<span data-ttu-id="745ee-104">Recupera le informazioni di sistema.</span><span class="sxs-lookup"><span data-stu-id="745ee-104">Retrieves system information.</span></span>

## <a name="syntax"></a><span data-ttu-id="745ee-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="745ee-105">Syntax</span></span>


```JScript
retVal = Shell.GetSystemInformation(
  sName
)
```


```VB

Shell.GetSystemInformation( _
  ByVal sName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="745ee-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="745ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="745ee-107">*sName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="745ee-107">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="745ee-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="745ee-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="745ee-109">**Stringa** che specifica le informazioni di sistema richieste.</span><span class="sxs-lookup"><span data-stu-id="745ee-109">A **String** that specifies the system information that is being requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="745ee-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="745ee-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="745ee-111">JScript</span><span class="sxs-lookup"><span data-stu-id="745ee-111">JScript</span></span>

<span data-ttu-id="745ee-112">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="745ee-112">Type: **Variant**</span></span>

<span data-ttu-id="745ee-113">Restituisce il valore delle informazioni di sistema richieste.</span><span class="sxs-lookup"><span data-stu-id="745ee-113">Returns the value of the requested system information.</span></span> <span data-ttu-id="745ee-114">Il tipo restituito dipende dalle informazioni di sistema richieste.</span><span class="sxs-lookup"><span data-stu-id="745ee-114">The return type depends on which system information is requested.</span></span> <span data-ttu-id="745ee-115">Vedere la sezione Osservazioni per informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="745ee-115">See the Remarks section for details.</span></span>

### <a name="vb"></a><span data-ttu-id="745ee-116">VB</span><span class="sxs-lookup"><span data-stu-id="745ee-116">VB</span></span>

<span data-ttu-id="745ee-117">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="745ee-117">Type: **Variant**</span></span>

<span data-ttu-id="745ee-118">Restituisce il valore delle informazioni di sistema richieste.</span><span class="sxs-lookup"><span data-stu-id="745ee-118">Returns the value of the requested system information.</span></span> <span data-ttu-id="745ee-119">Il tipo restituito dipende dalle informazioni di sistema richieste.</span><span class="sxs-lookup"><span data-stu-id="745ee-119">The return type depends on which system information is requested.</span></span> <span data-ttu-id="745ee-120">Vedere la sezione Osservazioni per informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="745ee-120">See the Remarks section for details.</span></span>

## <a name="remarks"></a><span data-ttu-id="745ee-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="745ee-121">Remarks</span></span>

<span data-ttu-id="745ee-122">Questo metodo può essere utilizzato per richiedere molti valori di informazioni di sistema.</span><span class="sxs-lookup"><span data-stu-id="745ee-122">This method can be used to request many system information values.</span></span> <span data-ttu-id="745ee-123">La tabella seguente fornisce il valore *sName* usato per richiedere le informazioni e il tipo associato del valore restituito.</span><span class="sxs-lookup"><span data-stu-id="745ee-123">The following table gives the *sName* value that is used to request the information and the associated type of the returned value.</span></span>



<span data-ttu-id="745ee-124">*sName*</span><span class="sxs-lookup"><span data-stu-id="745ee-124">*sName*</span></span>

<span data-ttu-id="745ee-125">Tipo restituito</span><span class="sxs-lookup"><span data-stu-id="745ee-125">Return type</span></span>

<span data-ttu-id="745ee-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="745ee-126">Description</span></span>

<span data-ttu-id="745ee-127">DirectoryServiceAvailable</span><span class="sxs-lookup"><span data-stu-id="745ee-127">DirectoryServiceAvailable</span></span>

<span data-ttu-id="745ee-128">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="745ee-128">**Boolean**</span></span>

<span data-ttu-id="745ee-129">Impostare su **true** se il servizio directory è disponibile; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="745ee-129">Set to **true** if the directory service is available; otherwise, **false**.</span></span>

<span data-ttu-id="745ee-130">DoubleClickTime</span><span class="sxs-lookup"><span data-stu-id="745ee-130">DoubleClickTime</span></span>

<span data-ttu-id="745ee-131">**Integer**</span><span class="sxs-lookup"><span data-stu-id="745ee-131">**Integer**</span></span>

<span data-ttu-id="745ee-132">Tempo doppio clic, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="745ee-132">The double-click time, in milliseconds.</span></span>

<span data-ttu-id="745ee-133">ProcessorLevel</span><span class="sxs-lookup"><span data-stu-id="745ee-133">ProcessorLevel</span></span>

<span data-ttu-id="745ee-134">**Integer**</span><span class="sxs-lookup"><span data-stu-id="745ee-134">**Integer**</span></span>

<span data-ttu-id="745ee-135">**Windows Vista e versioni successive**.</span><span class="sxs-lookup"><span data-stu-id="745ee-135">**Windows Vista and later**.</span></span> <span data-ttu-id="745ee-136">Livello del processore.</span><span class="sxs-lookup"><span data-stu-id="745ee-136">The processor level.</span></span> <span data-ttu-id="745ee-137">Restituisce 3, 4 o 5 per i processori a livello di x386, x486 e Pentium, rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="745ee-137">Returns 3, 4, or 5, for x386, x486, and Pentium-level processors, respectively.</span></span>

<span data-ttu-id="745ee-138">ProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="745ee-138">ProcessorSpeed</span></span>

<span data-ttu-id="745ee-139">**Integer**</span><span class="sxs-lookup"><span data-stu-id="745ee-139">**Integer**</span></span>

<span data-ttu-id="745ee-140">Velocità del processore, in megahertz (MHz).</span><span class="sxs-lookup"><span data-stu-id="745ee-140">The processor speed, in megahertz (MHz).</span></span>

<span data-ttu-id="745ee-141">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="745ee-141">ProcessorArchitecture</span></span>

<span data-ttu-id="745ee-142">**Integer**</span><span class="sxs-lookup"><span data-stu-id="745ee-142">**Integer**</span></span>

<span data-ttu-id="745ee-143">Architettura del processore.</span><span class="sxs-lookup"><span data-stu-id="745ee-143">The processor architecture.</span></span> <span data-ttu-id="745ee-144">Per informazioni dettagliate, vedere la descrizione del membro **wProcessorArchitecture** della struttura [**delle \_ informazioni di sistema**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) .</span><span class="sxs-lookup"><span data-stu-id="745ee-144">For details, see the discussion of the **wProcessorArchitecture** member of the [**SYSTEM\_INFO**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span>

<span data-ttu-id="745ee-145">PhysicalMemoryInstalled</span><span class="sxs-lookup"><span data-stu-id="745ee-145">PhysicalMemoryInstalled</span></span>

<span data-ttu-id="745ee-146">**Integer**</span><span class="sxs-lookup"><span data-stu-id="745ee-146">**Integer**</span></span>

<span data-ttu-id="745ee-147">Quantità di memoria fisica installata, in byte.</span><span class="sxs-lookup"><span data-stu-id="745ee-147">The amount of physical memory installed, in bytes.</span></span>

<span data-ttu-id="745ee-148">Gli elementi seguenti sono validi solo in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="745ee-148">The following are valid only on Windows XP.</span></span>

<span data-ttu-id="745ee-149">\_Professional IsOS</span><span class="sxs-lookup"><span data-stu-id="745ee-149">IsOS\_Professional</span></span>

<span data-ttu-id="745ee-150">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="745ee-150">**Boolean**</span></span>

<span data-ttu-id="745ee-151">Impostare su **true** se il sistema operativo è Windows XP Professional Edition; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="745ee-151">Set to **true** if the operating system is Windows XP Professional Edition; otherwise, **false**.</span></span>

<span data-ttu-id="745ee-152">\_Personale IsOS</span><span class="sxs-lookup"><span data-stu-id="745ee-152">IsOS\_Personal</span></span>

<span data-ttu-id="745ee-153">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="745ee-153">**Boolean**</span></span>

<span data-ttu-id="745ee-154">Impostare su **true** se il sistema operativo è Windows XP Home Edition; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="745ee-154">Set to **true** if the operating system is Windows XP Home Edition; otherwise, **false**.</span></span>

<span data-ttu-id="745ee-155">Il codice seguente è valido solo in Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="745ee-155">The following is valid only on Windows XP and later.</span></span>

<span data-ttu-id="745ee-156">\_DomainMember IsOS</span><span class="sxs-lookup"><span data-stu-id="745ee-156">IsOS\_DomainMember</span></span>

<span data-ttu-id="745ee-157">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="745ee-157">**Boolean**</span></span>

<span data-ttu-id="745ee-158">Impostare su **true** se il computer è membro di un dominio. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="745ee-158">Set to **true** if the computer is a member of a domain; otherwise, **false**.</span></span>



 

<span data-ttu-id="745ee-159">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="745ee-159">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="745ee-160">Esempio</span><span class="sxs-lookup"><span data-stu-id="745ee-160">Examples</span></span>

<span data-ttu-id="745ee-161">Negli esempi seguenti viene illustrato l'utilizzo di **GetSystemInformation** per JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="745ee-161">The following examples show the use of **GetSystemInformation** for JScript and VBScript.</span></span>

<span data-ttu-id="745ee-162">JScript</span><span class="sxs-lookup"><span data-stu-id="745ee-162">JScript:</span></span>


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



<span data-ttu-id="745ee-163">VBScript</span><span class="sxs-lookup"><span data-stu-id="745ee-163">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="745ee-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="745ee-164">Requirements</span></span>



| <span data-ttu-id="745ee-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="745ee-165">Requirement</span></span> | <span data-ttu-id="745ee-166">Valore</span><span class="sxs-lookup"><span data-stu-id="745ee-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="745ee-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="745ee-167">Minimum supported client</span></span><br/> | <span data-ttu-id="745ee-168">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="745ee-168">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="745ee-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="745ee-169">Minimum supported server</span></span><br/> | <span data-ttu-id="745ee-170">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="745ee-170">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="745ee-171">Intestazione</span><span class="sxs-lookup"><span data-stu-id="745ee-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="745ee-172"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="745ee-172"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="745ee-173">IDL</span><span class="sxs-lookup"><span data-stu-id="745ee-173">IDL</span></span><br/>                      | <dl> <span data-ttu-id="745ee-174"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="745ee-174"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="745ee-175">DLL</span><span class="sxs-lookup"><span data-stu-id="745ee-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="745ee-176"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="745ee-176"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
