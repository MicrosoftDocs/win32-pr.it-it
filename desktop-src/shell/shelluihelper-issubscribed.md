---
description: Indica se un URL specificato è sottoscritto.
title: Metodo ShellUIHelper. IsValid (Exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.IsSubscribed
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: fcf23352-6603-4b17-9c3b-b353cca1c003
ms.openlocfilehash: 2085f38e5f91f13a2f67ff4f22b003b533249386
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050175"
---
# <a name="shelluihelperissubscribed-method"></a><span data-ttu-id="647e6-103">Metodo ShellUIHelper. IsValid</span><span class="sxs-lookup"><span data-stu-id="647e6-103">ShellUIHelper.IsSubscribed method</span></span>

<span data-ttu-id="647e6-104">Indica se un URL specificato è sottoscritto.</span><span class="sxs-lookup"><span data-stu-id="647e6-104">Indicates whether a specified URL is subscribed to.</span></span>

## <a name="syntax"></a><span data-ttu-id="647e6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="647e6-105">Syntax</span></span>


```JScript
bRetVal = ShellUIHelper.IsSubscribed(
  sURL
)
```



## <a name="parameters"></a><span data-ttu-id="647e6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="647e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="647e6-107">*surl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="647e6-107">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="647e6-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="647e6-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="647e6-109">Valore **stringa** che specifica l'URL.</span><span class="sxs-lookup"><span data-stu-id="647e6-109">A **String** value that specifies the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="647e6-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="647e6-110">Return value</span></span>

<span data-ttu-id="647e6-111">Tipo: \**Boolean \** _</span><span class="sxs-lookup"><span data-stu-id="647e6-111">Type: \**Boolean\** _</span></span>

<span data-ttu-id="647e6-112">_ *true*\* se l'URL è sottoscritto; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="647e6-112">_ *true*\* if the URL is subscribed to; otherwise, **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="647e6-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="647e6-113">Examples</span></span>

<span data-ttu-id="647e6-114">Nell'esempio seguente viene illustrato l'utilizzo corretto di questo metodo per JScript incorporato in HTML e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="647e6-114">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="647e6-115">JScript</span><span class="sxs-lookup"><span data-stu-id="647e6-115">JScript:</span></span>


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
    function fnShellUIHelperIsSubscribedJ()
    {
        var bReturn;
        
        bReturn = ShellUIHelper.IsSubscribed("https://www.microsoft.com/");
        alert(bReturn);
    }
</script>

</head>
<body onload=fnShellUIHelperIsSubscribedJ()>
</body>
</html>
```



<span data-ttu-id="647e6-116">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="647e6-116">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperIsSubscribedVB()
    Dim objShellUIHelper As ShellUIHelper
    Dim bReturn          As Boolean
    
    Set objShellUIHelper = New ShellUIHelper
        bReturn = objShellUIHelper.IsSubscribed("https://www.microsoft.com/")
        Debug.Print bReturn
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="647e6-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="647e6-117">Requirements</span></span>



| <span data-ttu-id="647e6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="647e6-118">Requirement</span></span> | <span data-ttu-id="647e6-119">Valore</span><span class="sxs-lookup"><span data-stu-id="647e6-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="647e6-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="647e6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="647e6-121">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="647e6-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="647e6-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="647e6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="647e6-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="647e6-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="647e6-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="647e6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="647e6-125"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="647e6-125"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="647e6-126">DLL</span><span class="sxs-lookup"><span data-stu-id="647e6-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="647e6-127"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="647e6-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
