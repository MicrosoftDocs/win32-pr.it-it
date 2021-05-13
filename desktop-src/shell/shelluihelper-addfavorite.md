---
description: Visualizza l'interfaccia utente predefinita per la creazione di un elemento preferito. L'interfaccia utente viene inizializzata sui parametri specificati.
title: Metodo ShellUIHelper.AddFavorite (Exdisp.h)
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
ms.openlocfilehash: 2ce6fa0a71bb2ab995e510f06b4403c78bebcc60
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842452"
---
# <a name="shelluihelperaddfavorite-method"></a><span data-ttu-id="dbfa9-104">Metodo ShellUIHelper.AddFavorite</span><span class="sxs-lookup"><span data-stu-id="dbfa9-104">ShellUIHelper.AddFavorite method</span></span>

<span data-ttu-id="dbfa9-105">Visualizza l'interfaccia utente predefinita per la creazione di un elemento preferito.</span><span class="sxs-lookup"><span data-stu-id="dbfa9-105">Displays the default user interface for creating a favorite item.</span></span> <span data-ttu-id="dbfa9-106">L'interfaccia utente viene inizializzata sui parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="dbfa9-106">The user interface is initialized to the specified parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbfa9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dbfa9-107">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddFavorite(
  sURL,
  [ vTitle ]
)
```



## <a name="parameters"></a><span data-ttu-id="dbfa9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dbfa9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbfa9-109">*sURL* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="dbfa9-109">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbfa9-110">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="dbfa9-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="dbfa9-111">Valore **String** che specifica l'URL dell'elemento da aggiungere alla **cartella** Preferiti.</span><span class="sxs-lookup"><span data-stu-id="dbfa9-111">A **String** value that specifies the URL of the item to be added to the **Favorites** folder.</span></span>

</dd> <dt>

<span data-ttu-id="dbfa9-112">*vTitle* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="dbfa9-112">*vTitle* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dbfa9-113">Tipo: **\* Variante**</span><span class="sxs-lookup"><span data-stu-id="dbfa9-113">Type: **Variant\***</span></span>

<span data-ttu-id="dbfa9-114">Valore **Variant** che specifica il nome dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="dbfa9-114">A **Variant** value that specifies the name of the item.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="dbfa9-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="dbfa9-115">Examples</span></span>

<span data-ttu-id="dbfa9-116">L'esempio seguente illustra l'utilizzo corretto di questo metodo per JScript incorporato in HTML e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="dbfa9-116">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="dbfa9-117">Jscript:</span><span class="sxs-lookup"><span data-stu-id="dbfa9-117">JScript:</span></span>


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



<span data-ttu-id="dbfa9-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="dbfa9-118">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddFavoriteVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddFavorite "https://www.msn.com", "MSN Home Page"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="dbfa9-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dbfa9-119">Requirements</span></span>



| <span data-ttu-id="dbfa9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbfa9-120">Requirement</span></span> | <span data-ttu-id="dbfa9-121">Valore</span><span class="sxs-lookup"><span data-stu-id="dbfa9-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbfa9-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dbfa9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dbfa9-123">Solo app desktop di Windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="dbfa9-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="dbfa9-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dbfa9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dbfa9-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dbfa9-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dbfa9-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dbfa9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbfa9-127"><dt>Exdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="dbfa9-127"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="dbfa9-128">DLL</span><span class="sxs-lookup"><span data-stu-id="dbfa9-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbfa9-129"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="dbfa9-129"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
