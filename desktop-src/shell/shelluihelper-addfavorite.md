---
description: Visualizza l'interfaccia utente predefinita per la creazione di un elemento preferito. L'interfaccia utente viene inizializzata sui parametri specificati.
title: Metodo ShellUIHelper. AddFavorite (Exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddFavorite
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b30e776e-642c-4599-b83f-ef15bc0b23d2
ms.openlocfilehash: a5c3cae52f0ad18c1f2ddf6cf91759d1c6daf6c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980722"
---
# <a name="shelluihelperaddfavorite-method"></a><span data-ttu-id="5d6f4-104">ShellUIHelper. AddFavorite, metodo</span><span class="sxs-lookup"><span data-stu-id="5d6f4-104">ShellUIHelper.AddFavorite method</span></span>

<span data-ttu-id="5d6f4-105">Visualizza l'interfaccia utente predefinita per la creazione di un elemento preferito.</span><span class="sxs-lookup"><span data-stu-id="5d6f4-105">Displays the default user interface for creating a favorite item.</span></span> <span data-ttu-id="5d6f4-106">L'interfaccia utente viene inizializzata sui parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="5d6f4-106">The user interface is initialized to the specified parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d6f4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5d6f4-107">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddFavorite(
  sURL,
  [ vTitle ]
)
```



## <a name="parameters"></a><span data-ttu-id="5d6f4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5d6f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d6f4-109">*surl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5d6f4-109">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d6f4-110">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="5d6f4-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="5d6f4-111">Valore **stringa** che specifica l'URL dell'elemento da aggiungere alla cartella **Preferiti** .</span><span class="sxs-lookup"><span data-stu-id="5d6f4-111">A **String** value that specifies the URL of the item to be added to the **Favorites** folder.</span></span>

</dd> <dt>

<span data-ttu-id="5d6f4-112">*vTitle* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="5d6f4-112">*vTitle* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5d6f4-113">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="5d6f4-113">Type: \**Variant\** _</span></span>

<span data-ttu-id="5d6f4-114">Valore _ *Variant*\* che specifica il nome dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="5d6f4-114">A _ *Variant*\* value that specifies the name of the item.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="5d6f4-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="5d6f4-115">Examples</span></span>

<span data-ttu-id="5d6f4-116">Nell'esempio seguente viene illustrato l'utilizzo corretto di questo metodo per JScript incorporato in HTML e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5d6f4-116">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="5d6f4-117">JScript</span><span class="sxs-lookup"><span data-stu-id="5d6f4-117">JScript:</span></span>


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
    function fnShellUIHelperAddFavoriteJ()
    {
        ShellUIHelper.AddFavorite("https://www.msn.com", "MSN Home Page");
    }
</script>

</head>
<body onload=fnShellUIHelperAddFavoriteJ()>
</body>
</html>
```



<span data-ttu-id="5d6f4-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="5d6f4-118">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddFavoriteVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddFavorite "https://www.msn.com", "MSN Home Page"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="5d6f4-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d6f4-119">Requirements</span></span>



| <span data-ttu-id="5d6f4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d6f4-120">Requirement</span></span> | <span data-ttu-id="5d6f4-121">Valore</span><span class="sxs-lookup"><span data-stu-id="5d6f4-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d6f4-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d6f4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5d6f4-123">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5d6f4-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5d6f4-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d6f4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5d6f4-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5d6f4-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5d6f4-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5d6f4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d6f4-127"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d6f4-127"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="5d6f4-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5d6f4-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d6f4-129"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="5d6f4-129"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
