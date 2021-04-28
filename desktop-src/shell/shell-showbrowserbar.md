---
description: 'Metodo Shell.ShowBrowserBar: visualizza una barra del browser.'
ms.assetid: 203636D2-54D3-4163-B9AC-39213D6F4203
title: Metodo Shell.ShowBrowserBar (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShowBrowserBar
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d19cd5b98ce39470860cc481ab05e4bb41adc9a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083725"
---
# <a name="shellshowbrowserbar-method"></a><span data-ttu-id="277bc-103">Metodo Shell.ShowBrowserBar</span><span class="sxs-lookup"><span data-stu-id="277bc-103">Shell.ShowBrowserBar method</span></span>

<span data-ttu-id="277bc-104">Visualizza una barra del browser.</span><span class="sxs-lookup"><span data-stu-id="277bc-104">Displays a browser bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="277bc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="277bc-105">Syntax</span></span>


```JScript
retVal = Shell.ShowBrowserBar(
  sCLSID,
  vShow
)
```


```VB

Shell.ShowBrowserBar( _
  ByVal sCLSID As BSTR, _
  ByVal vShow As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="277bc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="277bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="277bc-107">*sCLSID* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="277bc-107">*sCLSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="277bc-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="277bc-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="277bc-109">Valore **String** contenente il formato stringa del CLSID della barra del browser da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="277bc-109">A **String** that contains the string form of the CLSID of the browser bar to be displayed.</span></span> <span data-ttu-id="277bc-110">L'oggetto deve essere registrato come oggetto barra di Explorer con una categoria di \_ componenti CATID InfoBand.</span><span class="sxs-lookup"><span data-stu-id="277bc-110">The object must be registered as an Explorer Bar object with a CATID\_InfoBand component category.</span></span> <span data-ttu-id="277bc-111">Per altre informazioni, vedere [Creating Custom Explorer Bars, Tool Bands, and Desk Bands](band-objects.md).</span><span class="sxs-lookup"><span data-stu-id="277bc-111">For further information, see [Creating Custom Explorer Bars, Tool Bands, and Desk Bands](band-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="277bc-112">*vShow* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="277bc-112">*vShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="277bc-113">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="277bc-113">Type: **Variant**</span></span>

<span data-ttu-id="277bc-114">Impostare su **true per** visualizzare la barra del browser o **su false** per nasconderla.</span><span class="sxs-lookup"><span data-stu-id="277bc-114">Set to **true** to show the browser bar or **false** to hide it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="277bc-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="277bc-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="277bc-116">JScript</span><span class="sxs-lookup"><span data-stu-id="277bc-116">JScript</span></span>

<span data-ttu-id="277bc-117">Tipo: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="277bc-117">Type: **Variant\***</span></span>

<span data-ttu-id="277bc-118">Restituisce **true se** ha esito positivo; in caso contrario, **false.**</span><span class="sxs-lookup"><span data-stu-id="277bc-118">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="277bc-119">VB</span><span class="sxs-lookup"><span data-stu-id="277bc-119">VB</span></span>

<span data-ttu-id="277bc-120">Tipo: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="277bc-120">Type: **Variant\***</span></span>

<span data-ttu-id="277bc-121">Restituisce **true se** ha esito positivo; in caso contrario, **false.**</span><span class="sxs-lookup"><span data-stu-id="277bc-121">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="277bc-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="277bc-122">Remarks</span></span>

<span data-ttu-id="277bc-123">È possibile visualizzare una delle barre di Explorer standard impostando il *parametro sCLSID* sul CLSID di tale barra di Explorer.</span><span class="sxs-lookup"><span data-stu-id="277bc-123">You can display one of the standard Explorer Bars by setting the *sCLSID* parameter to the CLSID of that Explorer Bar.</span></span> <span data-ttu-id="277bc-124">Le barre di Explorer standard e le relative stringhe CLSID sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="277bc-124">The standard Explorer Bars and their CLSID strings are as follows:</span></span>



| <span data-ttu-id="277bc-125">Barra di Explorer</span><span class="sxs-lookup"><span data-stu-id="277bc-125">Explorer Bar</span></span> | <span data-ttu-id="277bc-126">Stringa CLSID</span><span class="sxs-lookup"><span data-stu-id="277bc-126">CLSID string</span></span>                           |
|--------------|----------------------------------------|
| <span data-ttu-id="277bc-127">Preferiti</span><span class="sxs-lookup"><span data-stu-id="277bc-127">Favorites</span></span>    | <span data-ttu-id="277bc-128">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="277bc-128">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="277bc-129">Cartelle</span><span class="sxs-lookup"><span data-stu-id="277bc-129">Folders</span></span>      | <span data-ttu-id="277bc-130">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="277bc-130">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="277bc-131">Cronologia</span><span class="sxs-lookup"><span data-stu-id="277bc-131">History</span></span>      | <span data-ttu-id="277bc-132">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="277bc-132">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="277bc-133">Cerca</span><span class="sxs-lookup"><span data-stu-id="277bc-133">Search</span></span>       | <span data-ttu-id="277bc-134">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span><span class="sxs-lookup"><span data-stu-id="277bc-134">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span></span> |



 

<span data-ttu-id="277bc-135">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="277bc-135">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="277bc-136">Esempio</span><span class="sxs-lookup"><span data-stu-id="277bc-136">Examples</span></span>

<span data-ttu-id="277bc-137">Gli esempi seguenti illustrano l'uso di **Shell.ShowBrowserBar** per visualizzare la **barra del** browser Preferiti.</span><span class="sxs-lookup"><span data-stu-id="277bc-137">The following examples show the use of **Shell.ShowBrowserBar** to display the **Favorites** browser bar.</span></span> <span data-ttu-id="277bc-138">L'utilizzo è illustrato per JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="277bc-138">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="277bc-139">Jscript:</span><span class="sxs-lookup"><span data-stu-id="277bc-139">JScript:</span></span>


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



<span data-ttu-id="277bc-140">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="277bc-140">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="277bc-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="277bc-141">Requirements</span></span>



| <span data-ttu-id="277bc-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="277bc-142">Requirement</span></span> | <span data-ttu-id="277bc-143">Valore</span><span class="sxs-lookup"><span data-stu-id="277bc-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="277bc-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="277bc-144">Minimum supported client</span></span><br/> | <span data-ttu-id="277bc-145">Solo app desktop windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="277bc-145">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="277bc-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="277bc-146">Minimum supported server</span></span><br/> | <span data-ttu-id="277bc-147">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="277bc-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="277bc-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="277bc-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="277bc-149"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="277bc-149"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="277bc-150">Idl</span><span class="sxs-lookup"><span data-stu-id="277bc-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="277bc-151"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="277bc-151"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="277bc-152">DLL</span><span class="sxs-lookup"><span data-stu-id="277bc-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="277bc-153"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="277bc-153"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
