---
description: 'Metodo IShellDispatch2.ShowBrowserBar: visualizza una barra del browser.'
ms.assetid: 5776370c-3bbf-449b-a8fe-2dbc7d89dd25
title: Metodo IShellDispatch2.ShowBrowserBar (Shldisp.h)
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
ms.openlocfilehash: 7143b55ae59c8fca845d256ddc1f79e69672364b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116939"
---
# <a name="ishelldispatch2showbrowserbar-method"></a><span data-ttu-id="f5b0e-103">Metodo IShellDispatch2.ShowBrowserBar</span><span class="sxs-lookup"><span data-stu-id="f5b0e-103">IShellDispatch2.ShowBrowserBar method</span></span>

<span data-ttu-id="f5b0e-104">Visualizza una barra del browser.</span><span class="sxs-lookup"><span data-stu-id="f5b0e-104">Displays a browser bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5b0e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5b0e-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="f5b0e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5b0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5b0e-107">*sCLSID* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f5b0e-107">*sCLSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5b0e-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="f5b0e-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="f5b0e-109">Valore **String** contenente il formato stringa del CLSID della barra del browser da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="f5b0e-109">A **String** that contains the string form of the CLSID of the browser bar to be displayed.</span></span> <span data-ttu-id="f5b0e-110">L'oggetto deve essere registrato come oggetto barra di Explorer con una categoria di \_ componenti CATID InfoBand.</span><span class="sxs-lookup"><span data-stu-id="f5b0e-110">The object must be registered as an Explorer Bar object with a CATID\_InfoBand component category.</span></span> <span data-ttu-id="f5b0e-111">Per altre informazioni, vedere [Creating Custom Explorer Bars, Tool Bands, and Desk Bands](band-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f5b0e-111">For further information, see [Creating Custom Explorer Bars, Tool Bands, and Desk Bands](band-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5b0e-112">*vShow* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f5b0e-112">*vShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5b0e-113">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="f5b0e-113">Type: **Variant**</span></span>

<span data-ttu-id="f5b0e-114">Impostare su **true per** visualizzare la barra del browser o **su false** per nasconderla.</span><span class="sxs-lookup"><span data-stu-id="f5b0e-114">Set to **true** to show the browser bar or **false** to hide it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5b0e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5b0e-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="f5b0e-116">JScript</span><span class="sxs-lookup"><span data-stu-id="f5b0e-116">JScript</span></span>

<span data-ttu-id="f5b0e-117">Tipo: **\* Variante**</span><span class="sxs-lookup"><span data-stu-id="f5b0e-117">Type: **Variant\***</span></span>

<span data-ttu-id="f5b0e-118">Restituisce **true se** ha esito positivo; in caso contrario, **false.**</span><span class="sxs-lookup"><span data-stu-id="f5b0e-118">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="f5b0e-119">VB</span><span class="sxs-lookup"><span data-stu-id="f5b0e-119">VB</span></span>

<span data-ttu-id="f5b0e-120">Tipo: **\* Variante**</span><span class="sxs-lookup"><span data-stu-id="f5b0e-120">Type: **Variant\***</span></span>

<span data-ttu-id="f5b0e-121">Restituisce **true se** ha esito positivo; in caso contrario, **false.**</span><span class="sxs-lookup"><span data-stu-id="f5b0e-121">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5b0e-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5b0e-122">Remarks</span></span>

<span data-ttu-id="f5b0e-123">Questo metodo viene implementato e accessibile tramite il [**metodo Shell.ShowBrowserBar.**](./shell-showbrowserbar.md)</span><span class="sxs-lookup"><span data-stu-id="f5b0e-123">This method is implemented and accessed through the [**Shell.ShowBrowserBar**](./shell-showbrowserbar.md) method.</span></span>

<span data-ttu-id="f5b0e-124">È possibile visualizzare una delle barre di Explorer standard impostando il *parametro sCLSID* sul CLSID di tale barra di Explorer.</span><span class="sxs-lookup"><span data-stu-id="f5b0e-124">You can display one of the standard Explorer Bars by setting the *sCLSID* parameter to the CLSID of that Explorer Bar.</span></span> <span data-ttu-id="f5b0e-125">Le barre di Explorer standard e le relative stringhe CLSID sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="f5b0e-125">The standard Explorer Bars and their CLSID strings are as follows:</span></span>



| <span data-ttu-id="f5b0e-126">Barra di Explorer</span><span class="sxs-lookup"><span data-stu-id="f5b0e-126">Explorer Bar</span></span> | <span data-ttu-id="f5b0e-127">Stringa CLSID</span><span class="sxs-lookup"><span data-stu-id="f5b0e-127">CLSID string</span></span>                           |
|--------------|----------------------------------------|
| <span data-ttu-id="f5b0e-128">Preferiti</span><span class="sxs-lookup"><span data-stu-id="f5b0e-128">Favorites</span></span>    | <span data-ttu-id="f5b0e-129">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="f5b0e-129">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="f5b0e-130">Cartelle</span><span class="sxs-lookup"><span data-stu-id="f5b0e-130">Folders</span></span>      | <span data-ttu-id="f5b0e-131">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="f5b0e-131">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="f5b0e-132">Cronologia</span><span class="sxs-lookup"><span data-stu-id="f5b0e-132">History</span></span>      | <span data-ttu-id="f5b0e-133">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="f5b0e-133">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="f5b0e-134">Cerca</span><span class="sxs-lookup"><span data-stu-id="f5b0e-134">Search</span></span>       | <span data-ttu-id="f5b0e-135">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span><span class="sxs-lookup"><span data-stu-id="f5b0e-135">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span></span> |



 

<span data-ttu-id="f5b0e-136">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f5b0e-136">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="f5b0e-137">Esempio</span><span class="sxs-lookup"><span data-stu-id="f5b0e-137">Examples</span></span>

<span data-ttu-id="f5b0e-138">Gli esempi seguenti illustrano l'uso **di ShowBrowserBar** per visualizzare la **barra del** browser Preferiti.</span><span class="sxs-lookup"><span data-stu-id="f5b0e-138">The following examples show the use of **ShowBrowserBar** to display the **Favorites** browser bar.</span></span> <span data-ttu-id="f5b0e-139">L'utilizzo è illustrato per JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="f5b0e-139">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="f5b0e-140">Jscript:</span><span class="sxs-lookup"><span data-stu-id="f5b0e-140">JScript:</span></span>


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



<span data-ttu-id="f5b0e-141">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="f5b0e-141">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="f5b0e-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5b0e-142">Requirements</span></span>



| <span data-ttu-id="f5b0e-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5b0e-143">Requirement</span></span> | <span data-ttu-id="f5b0e-144">Valore</span><span class="sxs-lookup"><span data-stu-id="f5b0e-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b0e-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5b0e-145">Minimum supported client</span></span><br/> | <span data-ttu-id="f5b0e-146">Solo app desktop windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f5b0e-146">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f5b0e-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5b0e-147">Minimum supported server</span></span><br/> | <span data-ttu-id="f5b0e-148">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f5b0e-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f5b0e-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5b0e-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5b0e-150"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="f5b0e-150"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="f5b0e-151">Idl</span><span class="sxs-lookup"><span data-stu-id="f5b0e-151">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f5b0e-152"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="f5b0e-152"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="f5b0e-153">DLL</span><span class="sxs-lookup"><span data-stu-id="f5b0e-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5b0e-154"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="f5b0e-154"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
