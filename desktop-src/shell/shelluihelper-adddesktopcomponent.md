---
description: Aggiunge un elemento a Microsoft Active Desktop.
title: Metodo ShellUIHelper.AddDesktopComponent (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddDesktopComponent
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 41634a89-15b9-41c8-ba3f-4bf19b786f6f
ms.openlocfilehash: 2edaa79bd62dcee40e4f197700d2128cb0b2070d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842462"
---
# <a name="shelluihelperadddesktopcomponent-method"></a><span data-ttu-id="c2e53-103">Metodo ShellUIHelper.AddDesktopComponent</span><span class="sxs-lookup"><span data-stu-id="c2e53-103">ShellUIHelper.AddDesktopComponent method</span></span>

<span data-ttu-id="c2e53-104">Aggiunge un elemento a Microsoft Active Desktop.</span><span class="sxs-lookup"><span data-stu-id="c2e53-104">Adds an item to the Microsoft Active Desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2e53-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2e53-105">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddDesktopComponent(
  sURL,
  sType,
  [ Left ],
  [ Top ],
  [ Width ],
  [ Height ]
)
```



## <a name="parameters"></a><span data-ttu-id="c2e53-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2e53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2e53-107">*sURL* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c2e53-107">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2e53-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="c2e53-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="c2e53-109">Valore **String** che specifica l'URL del nuovo elemento preferito.</span><span class="sxs-lookup"><span data-stu-id="c2e53-109">A **String** value that specifies the URL of the new favorite item.</span></span>

</dd> <dt>

<span data-ttu-id="c2e53-110">*sType* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c2e53-110">*sType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2e53-111">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="c2e53-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="c2e53-112">Valore **String** che specifica il tipo di elemento aggiunto.</span><span class="sxs-lookup"><span data-stu-id="c2e53-112">A **String** value that specifies the type of item being added.</span></span> <span data-ttu-id="c2e53-113">Può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c2e53-113">This can be one of the following values.</span></span>

<dt>



 <span data-ttu-id="c2e53-114">(immagine)</span><span class="sxs-lookup"><span data-stu-id="c2e53-114">(image)</span></span>


</dt> <dd>

<span data-ttu-id="c2e53-115">Il componente è un'immagine.</span><span class="sxs-lookup"><span data-stu-id="c2e53-115">The component is an image.</span></span>

</dd> <dt>



 <span data-ttu-id="c2e53-116">(sito Web)</span><span class="sxs-lookup"><span data-stu-id="c2e53-116">(website)</span></span>


</dt> <dd>

<span data-ttu-id="c2e53-117">Il componente è un sito Web.</span><span class="sxs-lookup"><span data-stu-id="c2e53-117">The component is a website.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c2e53-118">*A sinistra* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c2e53-118">*Left* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c2e53-119">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="c2e53-119">Type: **Variant**</span></span>

<span data-ttu-id="c2e53-120">Posizione del bordo sinistro del componente, in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="c2e53-120">The position of the left edge of the component, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="c2e53-121">*In alto* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c2e53-121">*Top* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c2e53-122">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="c2e53-122">Type: **Variant**</span></span>

<span data-ttu-id="c2e53-123">Posizione del bordo superiore del componente, in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="c2e53-123">The position of the top edge of the component, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="c2e53-124">*Larghezza* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c2e53-124">*Width* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c2e53-125">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="c2e53-125">Type: **Variant**</span></span>

<span data-ttu-id="c2e53-126">Larghezza del componente, in unità dello schermo.</span><span class="sxs-lookup"><span data-stu-id="c2e53-126">The width of the component, in screen units.</span></span>

</dd> <dt>

<span data-ttu-id="c2e53-127">*Altezza* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c2e53-127">*Height* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c2e53-128">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="c2e53-128">Type: **Variant**</span></span>

<span data-ttu-id="c2e53-129">Altezza del componente, in unità dello schermo.</span><span class="sxs-lookup"><span data-stu-id="c2e53-129">The height of the component, in screen units.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="c2e53-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="c2e53-130">Examples</span></span>

<span data-ttu-id="c2e53-131">Nell'esempio seguente viene illustrato l'utilizzo corretto di questo metodo per JScript incorporato in HTML e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c2e53-131">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="c2e53-132">Jscript:</span><span class="sxs-lookup"><span data-stu-id="c2e53-132">JScript:</span></span>


```JScript
<html>
<head>
<title></title>

<object id="ShellUIHelper"
        classid="CLSID:64AB4BB7-111E-11d1-8F79-00C04FC2FBE1"
        width=0
        height=0
        VIEWASTEXT>
</object>

<script language="JavaScript">
    function fnShellUIHelperAddDesktopComponentJ()
    {
        ShellUIHelper.AddDesktopComponent("https://www.microsoft.com/", "website");
    }
</script>

</head>
<body onload=fnShellUIHelperAddDesktopComponentJ()>
</body>
</html>
```



<span data-ttu-id="c2e53-133">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="c2e53-133">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddDesktopComponentVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddDesktopComponent "https://www.microsoft.com/", "website"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c2e53-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2e53-134">Requirements</span></span>



| <span data-ttu-id="c2e53-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2e53-135">Requirement</span></span> | <span data-ttu-id="c2e53-136">Valore</span><span class="sxs-lookup"><span data-stu-id="c2e53-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2e53-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2e53-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c2e53-138">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c2e53-138">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c2e53-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2e53-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c2e53-140">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c2e53-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c2e53-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c2e53-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2e53-142"><dt>Exdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="c2e53-142"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="c2e53-143">DLL</span><span class="sxs-lookup"><span data-stu-id="c2e53-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2e53-144"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="c2e53-144"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
