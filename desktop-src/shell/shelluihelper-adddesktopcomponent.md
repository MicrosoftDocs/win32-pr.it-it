---
description: Aggiunge un elemento a Microsoft Active Desktop.
title: Metodo ShellUIHelper. AddDesktopComponent (Exdisp. h)
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
ms.openlocfilehash: d5234a0b43ea25c8ac931dc14ec90f7a6696ddfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980591"
---
# <a name="shelluihelperadddesktopcomponent-method"></a><span data-ttu-id="001ba-103">ShellUIHelper. AddDesktopComponent, metodo</span><span class="sxs-lookup"><span data-stu-id="001ba-103">ShellUIHelper.AddDesktopComponent method</span></span>

<span data-ttu-id="001ba-104">Aggiunge un elemento a Microsoft Active Desktop.</span><span class="sxs-lookup"><span data-stu-id="001ba-104">Adds an item to the Microsoft Active Desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="001ba-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="001ba-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="001ba-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="001ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="001ba-107">*surl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="001ba-107">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="001ba-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="001ba-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="001ba-109">Valore **stringa** che specifica l'URL del nuovo elemento preferito.</span><span class="sxs-lookup"><span data-stu-id="001ba-109">A **String** value that specifies the URL of the new favorite item.</span></span>

</dd> <dt>

<span data-ttu-id="001ba-110">*sPrevista* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="001ba-110">*sType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="001ba-111">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="001ba-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="001ba-112">Valore **stringa** che specifica il tipo di elemento da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="001ba-112">A **String** value that specifies the type of item being added.</span></span> <span data-ttu-id="001ba-113">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="001ba-113">This can be one of the following values.</span></span>

<dt>



 <span data-ttu-id="001ba-114">immagine</span><span class="sxs-lookup"><span data-stu-id="001ba-114">(image)</span></span>


</dt> <dd>

<span data-ttu-id="001ba-115">Il componente è un'immagine.</span><span class="sxs-lookup"><span data-stu-id="001ba-115">The component is an image.</span></span>

</dd> <dt>



 <span data-ttu-id="001ba-116">sito Web</span><span class="sxs-lookup"><span data-stu-id="001ba-116">(website)</span></span>


</dt> <dd>

<span data-ttu-id="001ba-117">Il componente è un sito Web.</span><span class="sxs-lookup"><span data-stu-id="001ba-117">The component is a website.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="001ba-118">A *sinistra* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="001ba-118">*Left* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="001ba-119">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="001ba-119">Type: **Variant**</span></span>

<span data-ttu-id="001ba-120">Posizione del bordo sinistro del componente, in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="001ba-120">The position of the left edge of the component, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="001ba-121">In *alto* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="001ba-121">*Top* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="001ba-122">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="001ba-122">Type: **Variant**</span></span>

<span data-ttu-id="001ba-123">Posizione del bordo superiore del componente, in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="001ba-123">The position of the top edge of the component, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="001ba-124">*Larghezza* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="001ba-124">*Width* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="001ba-125">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="001ba-125">Type: **Variant**</span></span>

<span data-ttu-id="001ba-126">Larghezza del componente, in unità dello schermo.</span><span class="sxs-lookup"><span data-stu-id="001ba-126">The width of the component, in screen units.</span></span>

</dd> <dt>

<span data-ttu-id="001ba-127">*Altezza* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="001ba-127">*Height* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="001ba-128">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="001ba-128">Type: **Variant**</span></span>

<span data-ttu-id="001ba-129">Altezza del componente, in unità dello schermo.</span><span class="sxs-lookup"><span data-stu-id="001ba-129">The height of the component, in screen units.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="001ba-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="001ba-130">Examples</span></span>

<span data-ttu-id="001ba-131">Nell'esempio seguente viene illustrato l'utilizzo corretto di questo metodo per JScript incorporato in HTML e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="001ba-131">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="001ba-132">JScript</span><span class="sxs-lookup"><span data-stu-id="001ba-132">JScript:</span></span>


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



<span data-ttu-id="001ba-133">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="001ba-133">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddDesktopComponentVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddDesktopComponent "https://www.microsoft.com/", "website"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="001ba-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="001ba-134">Requirements</span></span>



| <span data-ttu-id="001ba-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="001ba-135">Requirement</span></span> | <span data-ttu-id="001ba-136">Valore</span><span class="sxs-lookup"><span data-stu-id="001ba-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="001ba-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="001ba-137">Minimum supported client</span></span><br/> | <span data-ttu-id="001ba-138">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="001ba-138">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="001ba-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="001ba-139">Minimum supported server</span></span><br/> | <span data-ttu-id="001ba-140">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="001ba-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="001ba-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="001ba-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="001ba-142"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="001ba-142"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="001ba-143">DLL</span><span class="sxs-lookup"><span data-stu-id="001ba-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="001ba-144"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="001ba-144"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
