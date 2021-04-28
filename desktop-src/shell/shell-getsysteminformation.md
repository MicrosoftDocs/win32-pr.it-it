---
description: 'Metodo Shell.GetSystemInformation: recupera le informazioni di sistema.'
ms.assetid: 94C10DD6-FE49-4dd4-AEED-69B73A75EDEF
title: Metodo Shell.GetSystemInformation (Shldisp.h)
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
ms.openlocfilehash: b9e021e767309007cfee2cfc78268fb7d7cea042
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104279"
---
# <a name="shellgetsysteminformation-method"></a><span data-ttu-id="55d42-103">Metodo Shell.GetSystemInformation</span><span class="sxs-lookup"><span data-stu-id="55d42-103">Shell.GetSystemInformation method</span></span>

<span data-ttu-id="55d42-104">Recupera le informazioni di sistema.</span><span class="sxs-lookup"><span data-stu-id="55d42-104">Retrieves system information.</span></span>

## <a name="syntax"></a><span data-ttu-id="55d42-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55d42-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="55d42-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="55d42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55d42-107">*sName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="55d42-107">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55d42-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="55d42-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="55d42-109">Valore **String** che specifica le informazioni di sistema richieste.</span><span class="sxs-lookup"><span data-stu-id="55d42-109">A **String** that specifies the system information that is being requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55d42-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="55d42-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="55d42-111">JScript</span><span class="sxs-lookup"><span data-stu-id="55d42-111">JScript</span></span>

<span data-ttu-id="55d42-112">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="55d42-112">Type: **Variant**</span></span>

<span data-ttu-id="55d42-113">Restituisce il valore delle informazioni di sistema richieste.</span><span class="sxs-lookup"><span data-stu-id="55d42-113">Returns the value of the requested system information.</span></span> <span data-ttu-id="55d42-114">Il tipo restituito dipende dalle informazioni di sistema richieste.</span><span class="sxs-lookup"><span data-stu-id="55d42-114">The return type depends on which system information is requested.</span></span> <span data-ttu-id="55d42-115">Vedere la sezione Osservazioni per informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="55d42-115">See the Remarks section for details.</span></span>

### <a name="vb"></a><span data-ttu-id="55d42-116">VB</span><span class="sxs-lookup"><span data-stu-id="55d42-116">VB</span></span>

<span data-ttu-id="55d42-117">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="55d42-117">Type: **Variant**</span></span>

<span data-ttu-id="55d42-118">Restituisce il valore delle informazioni di sistema richieste.</span><span class="sxs-lookup"><span data-stu-id="55d42-118">Returns the value of the requested system information.</span></span> <span data-ttu-id="55d42-119">Il tipo restituito dipende dalle informazioni di sistema richieste.</span><span class="sxs-lookup"><span data-stu-id="55d42-119">The return type depends on which system information is requested.</span></span> <span data-ttu-id="55d42-120">Vedere la sezione Osservazioni per informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="55d42-120">See the Remarks section for details.</span></span>

## <a name="remarks"></a><span data-ttu-id="55d42-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="55d42-121">Remarks</span></span>

<span data-ttu-id="55d42-122">Questo metodo può essere usato per richiedere molti valori di informazioni di sistema.</span><span class="sxs-lookup"><span data-stu-id="55d42-122">This method can be used to request many system information values.</span></span> <span data-ttu-id="55d42-123">Nella tabella seguente viene specificato *il valore sName* usato per richiedere le informazioni e il tipo associato del valore restituito.</span><span class="sxs-lookup"><span data-stu-id="55d42-123">The following table gives the *sName* value that is used to request the information and the associated type of the returned value.</span></span>



<span data-ttu-id="55d42-124">*sName*</span><span class="sxs-lookup"><span data-stu-id="55d42-124">*sName*</span></span>

<span data-ttu-id="55d42-125">Tipo restituito</span><span class="sxs-lookup"><span data-stu-id="55d42-125">Return type</span></span>

<span data-ttu-id="55d42-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55d42-126">Description</span></span>

<span data-ttu-id="55d42-127">DirectoryServiceAvailable</span><span class="sxs-lookup"><span data-stu-id="55d42-127">DirectoryServiceAvailable</span></span>

<span data-ttu-id="55d42-128">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="55d42-128">**Boolean**</span></span>

<span data-ttu-id="55d42-129">Impostare su **true se** il servizio directory è disponibile. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="55d42-129">Set to **true** if the directory service is available; otherwise, **false**.</span></span>

<span data-ttu-id="55d42-130">DoubleClickTime</span><span class="sxs-lookup"><span data-stu-id="55d42-130">DoubleClickTime</span></span>

<span data-ttu-id="55d42-131">**Integer**</span><span class="sxs-lookup"><span data-stu-id="55d42-131">**Integer**</span></span>

<span data-ttu-id="55d42-132">Tempo di doppio clic, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="55d42-132">The double-click time, in milliseconds.</span></span>

<span data-ttu-id="55d42-133">ProcessorLevel</span><span class="sxs-lookup"><span data-stu-id="55d42-133">ProcessorLevel</span></span>

<span data-ttu-id="55d42-134">**Integer**</span><span class="sxs-lookup"><span data-stu-id="55d42-134">**Integer**</span></span>

<span data-ttu-id="55d42-135">**Windows Vista e versioni successive.**</span><span class="sxs-lookup"><span data-stu-id="55d42-135">**Windows Vista and later**.</span></span> <span data-ttu-id="55d42-136">Livello del processore.</span><span class="sxs-lookup"><span data-stu-id="55d42-136">The processor level.</span></span> <span data-ttu-id="55d42-137">Restituisce 3, 4 o 5, rispettivamente per processori x386, x486 e Pentium.</span><span class="sxs-lookup"><span data-stu-id="55d42-137">Returns 3, 4, or 5, for x386, x486, and Pentium-level processors, respectively.</span></span>

<span data-ttu-id="55d42-138">ProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="55d42-138">ProcessorSpeed</span></span>

<span data-ttu-id="55d42-139">**Integer**</span><span class="sxs-lookup"><span data-stu-id="55d42-139">**Integer**</span></span>

<span data-ttu-id="55d42-140">Velocità del processore, in megahertz (MHz).</span><span class="sxs-lookup"><span data-stu-id="55d42-140">The processor speed, in megahertz (MHz).</span></span>

<span data-ttu-id="55d42-141">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="55d42-141">ProcessorArchitecture</span></span>

<span data-ttu-id="55d42-142">**Integer**</span><span class="sxs-lookup"><span data-stu-id="55d42-142">**Integer**</span></span>

<span data-ttu-id="55d42-143">Architettura del processore.</span><span class="sxs-lookup"><span data-stu-id="55d42-143">The processor architecture.</span></span> <span data-ttu-id="55d42-144">Per informazioni dettagliate, vedere la discussione sul **membro wProcessorArchitecture** della [**struttura SYSTEM \_ INFO.**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info)</span><span class="sxs-lookup"><span data-stu-id="55d42-144">For details, see the discussion of the **wProcessorArchitecture** member of the [**SYSTEM\_INFO**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span>

<span data-ttu-id="55d42-145">PhysicalMemoryInstalled</span><span class="sxs-lookup"><span data-stu-id="55d42-145">PhysicalMemoryInstalled</span></span>

<span data-ttu-id="55d42-146">**Integer**</span><span class="sxs-lookup"><span data-stu-id="55d42-146">**Integer**</span></span>

<span data-ttu-id="55d42-147">Quantità di memoria fisica installata, in byte.</span><span class="sxs-lookup"><span data-stu-id="55d42-147">The amount of physical memory installed, in bytes.</span></span>

<span data-ttu-id="55d42-148">Gli elementi seguenti sono validi solo in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="55d42-148">The following are valid only on Windows XP.</span></span>

<span data-ttu-id="55d42-149">IsOS \_ Professional</span><span class="sxs-lookup"><span data-stu-id="55d42-149">IsOS\_Professional</span></span>

<span data-ttu-id="55d42-150">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="55d42-150">**Boolean**</span></span>

<span data-ttu-id="55d42-151">Impostare su **true se** il sistema operativo è Windows XP Professional Edition; in caso contrario, **false.**</span><span class="sxs-lookup"><span data-stu-id="55d42-151">Set to **true** if the operating system is Windows XP Professional Edition; otherwise, **false**.</span></span>

<span data-ttu-id="55d42-152">IsOS \_ Personal</span><span class="sxs-lookup"><span data-stu-id="55d42-152">IsOS\_Personal</span></span>

<span data-ttu-id="55d42-153">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="55d42-153">**Boolean**</span></span>

<span data-ttu-id="55d42-154">Impostare su **true se** il sistema operativo è Windows XP Home Edition; in caso contrario, **false.**</span><span class="sxs-lookup"><span data-stu-id="55d42-154">Set to **true** if the operating system is Windows XP Home Edition; otherwise, **false**.</span></span>

<span data-ttu-id="55d42-155">Quanto segue è valido solo in Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="55d42-155">The following is valid only on Windows XP and later.</span></span>

<span data-ttu-id="55d42-156">IsOS \_ DomainMember</span><span class="sxs-lookup"><span data-stu-id="55d42-156">IsOS\_DomainMember</span></span>

<span data-ttu-id="55d42-157">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="55d42-157">**Boolean**</span></span>

<span data-ttu-id="55d42-158">Impostare su **true** se il computer è membro di un dominio; in caso contrario, **false.**</span><span class="sxs-lookup"><span data-stu-id="55d42-158">Set to **true** if the computer is a member of a domain; otherwise, **false**.</span></span>



 

<span data-ttu-id="55d42-159">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="55d42-159">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="55d42-160">Esempio</span><span class="sxs-lookup"><span data-stu-id="55d42-160">Examples</span></span>

<span data-ttu-id="55d42-161">Gli esempi seguenti illustrano l'uso **di GetSystemInformation** per JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="55d42-161">The following examples show the use of **GetSystemInformation** for JScript and VBScript.</span></span>

<span data-ttu-id="55d42-162">Jscript:</span><span class="sxs-lookup"><span data-stu-id="55d42-162">JScript:</span></span>


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



<span data-ttu-id="55d42-163">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="55d42-163">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="55d42-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55d42-164">Requirements</span></span>



| <span data-ttu-id="55d42-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="55d42-165">Requirement</span></span> | <span data-ttu-id="55d42-166">Valore</span><span class="sxs-lookup"><span data-stu-id="55d42-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55d42-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55d42-167">Minimum supported client</span></span><br/> | <span data-ttu-id="55d42-168">Solo app desktop windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="55d42-168">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="55d42-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55d42-169">Minimum supported server</span></span><br/> | <span data-ttu-id="55d42-170">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="55d42-170">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="55d42-171">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55d42-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="55d42-172"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="55d42-172"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="55d42-173">Idl</span><span class="sxs-lookup"><span data-stu-id="55d42-173">IDL</span></span><br/>                      | <dl> <span data-ttu-id="55d42-174"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="55d42-174"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="55d42-175">DLL</span><span class="sxs-lookup"><span data-stu-id="55d42-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55d42-176"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="55d42-176"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
