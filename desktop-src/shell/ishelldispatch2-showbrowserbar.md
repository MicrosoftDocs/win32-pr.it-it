---
description: Visualizza una barra del browser.
ms.assetid: 5776370c-3bbf-449b-a8fe-2dbc7d89dd25
title: Metodo IShellDispatch2. ShowBrowserBar (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ShowBrowserBar
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e1df729401dd12b8221ba98a3b81ea65569113e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978015"
---
# <a name="ishelldispatch2showbrowserbar-method"></a><span data-ttu-id="8023b-103">IShellDispatch2. ShowBrowserBar, metodo</span><span class="sxs-lookup"><span data-stu-id="8023b-103">IShellDispatch2.ShowBrowserBar method</span></span>

<span data-ttu-id="8023b-104">Visualizza una barra del browser.</span><span class="sxs-lookup"><span data-stu-id="8023b-104">Displays a browser bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="8023b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8023b-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.ShowBrowserBar(
  sCLSID,
  vShow
)
```


```VB

IShellDispatch2.ShowBrowserBar( _
  ByVal sCLSID As BSTR, _
  ByVal vShow As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="8023b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8023b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8023b-107">*sCLSID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8023b-107">*sCLSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8023b-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="8023b-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="8023b-109">**Stringa** che contiene il formato stringa del CLSID della barra del browser da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="8023b-109">A **String** that contains the string form of the CLSID of the browser bar to be displayed.</span></span> <span data-ttu-id="8023b-110">L'oggetto deve essere registrato come oggetto della barra di Explorer con una \_ categoria di componenti INFOBAND CATID.</span><span class="sxs-lookup"><span data-stu-id="8023b-110">The object must be registered as an Explorer Bar object with a CATID\_InfoBand component category.</span></span> <span data-ttu-id="8023b-111">Per ulteriori informazioni, vedere [creazione di barre di esplorazione personalizzate, bande di strumenti e bande della scrivania](band-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8023b-111">For further information, see [Creating Custom Explorer Bars, Tool Bands, and Desk Bands](band-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="8023b-112">*vShow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8023b-112">*vShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8023b-113">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="8023b-113">Type: **Variant**</span></span>

<span data-ttu-id="8023b-114">Impostare su **true** per visualizzare la barra del browser o **false** per nasconderla.</span><span class="sxs-lookup"><span data-stu-id="8023b-114">Set to **true** to show the browser bar or **false** to hide it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8023b-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8023b-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="8023b-116">JScript</span><span class="sxs-lookup"><span data-stu-id="8023b-116">JScript</span></span>

<span data-ttu-id="8023b-117">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="8023b-117">Type: \**Variant\** _</span></span>

<span data-ttu-id="8023b-118">Restituisce _ *true*\* se ha esito positivo; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="8023b-118">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="8023b-119">VB</span><span class="sxs-lookup"><span data-stu-id="8023b-119">VB</span></span>

<span data-ttu-id="8023b-120">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="8023b-120">Type: \**Variant\** _</span></span>

<span data-ttu-id="8023b-121">Restituisce _ *true*\* se ha esito positivo; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="8023b-121">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8023b-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="8023b-122">Remarks</span></span>

<span data-ttu-id="8023b-123">Questo metodo viene implementato e accessibile tramite il metodo [**Shell. ShowBrowserBar**](./shell-showbrowserbar.md) .</span><span class="sxs-lookup"><span data-stu-id="8023b-123">This method is implemented and accessed through the [**Shell.ShowBrowserBar**](./shell-showbrowserbar.md) method.</span></span>

<span data-ttu-id="8023b-124">È possibile visualizzare una delle barre di Explorer standard impostando il parametro *sCLSID* sul CLSID della barra di Explorer.</span><span class="sxs-lookup"><span data-stu-id="8023b-124">You can display one of the standard Explorer Bars by setting the *sCLSID* parameter to the CLSID of that Explorer Bar.</span></span> <span data-ttu-id="8023b-125">Le barre di Explorer standard e le relative stringhe CLSID sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="8023b-125">The standard Explorer Bars and their CLSID strings are as follows:</span></span>



| <span data-ttu-id="8023b-126">Barra di Explorer</span><span class="sxs-lookup"><span data-stu-id="8023b-126">Explorer Bar</span></span> | <span data-ttu-id="8023b-127">Stringa CLSID</span><span class="sxs-lookup"><span data-stu-id="8023b-127">CLSID string</span></span>                           |
|--------------|----------------------------------------|
| <span data-ttu-id="8023b-128">Preferiti</span><span class="sxs-lookup"><span data-stu-id="8023b-128">Favorites</span></span>    | <span data-ttu-id="8023b-129">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="8023b-129">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="8023b-130">Cartelle</span><span class="sxs-lookup"><span data-stu-id="8023b-130">Folders</span></span>      | <span data-ttu-id="8023b-131">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="8023b-131">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="8023b-132">Cronologia</span><span class="sxs-lookup"><span data-stu-id="8023b-132">History</span></span>      | <span data-ttu-id="8023b-133">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="8023b-133">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="8023b-134">Cerca</span><span class="sxs-lookup"><span data-stu-id="8023b-134">Search</span></span>       | <span data-ttu-id="8023b-135">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span><span class="sxs-lookup"><span data-stu-id="8023b-135">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span></span> |



 

<span data-ttu-id="8023b-136">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8023b-136">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="8023b-137">Esempio</span><span class="sxs-lookup"><span data-stu-id="8023b-137">Examples</span></span>

<span data-ttu-id="8023b-138">Negli esempi seguenti viene illustrato l'utilizzo di **ShowBrowserBar** per visualizzare la barra del browser **Preferiti** .</span><span class="sxs-lookup"><span data-stu-id="8023b-138">The following examples show the use of **ShowBrowserBar** to display the **Favorites** browser bar.</span></span> <span data-ttu-id="8023b-139">L'utilizzo viene visualizzato per JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="8023b-139">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="8023b-140">JScript</span><span class="sxs-lookup"><span data-stu-id="8023b-140">JScript:</span></span>


```JScript
<script language="JavaScript">
    function fnShowBrowserBarJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true);
    }
</script>
```



<span data-ttu-id="8023b-141">VBScript</span><span class="sxs-lookup"><span data-stu-id="8023b-141">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShowBrowserBarVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="8023b-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8023b-142">Requirements</span></span>



| <span data-ttu-id="8023b-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="8023b-143">Requirement</span></span> | <span data-ttu-id="8023b-144">Valore</span><span class="sxs-lookup"><span data-stu-id="8023b-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8023b-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8023b-145">Minimum supported client</span></span><br/> | <span data-ttu-id="8023b-146">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8023b-146">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8023b-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8023b-147">Minimum supported server</span></span><br/> | <span data-ttu-id="8023b-148">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8023b-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8023b-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8023b-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="8023b-150"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8023b-150"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="8023b-151">IDL</span><span class="sxs-lookup"><span data-stu-id="8023b-151">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8023b-152"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8023b-152"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="8023b-153">DLL</span><span class="sxs-lookup"><span data-stu-id="8023b-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8023b-154"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="8023b-154"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
