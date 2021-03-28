---
description: Aggiunge un nuovo canale all'elenco di canali nel menu Preferiti di Windows Internet Explorer e alla barra del canale sul desktop.
title: Metodo ShellUIHelper. AddChannel (Exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddChannel
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b62e6e82-429a-4d41-96d4-cba639b611f5
ms.openlocfilehash: 93c62abd8f788f950e36bcfc5fa10f7c991a6410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995141"
---
# <a name="shelluihelperaddchannel-method"></a><span data-ttu-id="ce2ca-103">ShellUIHelper. AddChannel, metodo</span><span class="sxs-lookup"><span data-stu-id="ce2ca-103">ShellUIHelper.AddChannel method</span></span>

<span data-ttu-id="ce2ca-104">Aggiunge un nuovo canale all'elenco di canali nel menu **Preferiti** di Windows Internet Explorer e alla barra del **canale** sul desktop.</span><span class="sxs-lookup"><span data-stu-id="ce2ca-104">Adds a new channel to the list of channels in the Windows Internet Explorer **Favorites** menu and to the **Channel** bar on the desktop.</span></span>

> [!Note]  
> <span data-ttu-id="ce2ca-105">Questo metodo non è più supportato in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ce2ca-105">This method is no longer supported under Windows Vista.</span></span> <span data-ttu-id="ce2ca-106">In tale sistema operativo restituisce E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="ce2ca-106">Under that operating system, it returns E\_NOTIMPL.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ce2ca-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce2ca-107">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddChannel(
  sURL
)
```



## <a name="parameters"></a><span data-ttu-id="ce2ca-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce2ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce2ca-109">*surl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce2ca-109">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce2ca-110">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="ce2ca-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="ce2ca-111">Valore **stringa** che specifica l'URL del file CDF.</span><span class="sxs-lookup"><span data-stu-id="ce2ca-111">A **String** value that specifies the URL of the CDF file.</span></span>

> [!Note]  
> <span data-ttu-id="ce2ca-112">I collegamenti nel file CDF devono usare i protocolli HTTP, HTTPS o FTP.</span><span class="sxs-lookup"><span data-stu-id="ce2ca-112">The links in the CDF file must use HTTP, HTTPS, or FTP protocols.</span></span> <span data-ttu-id="ce2ca-113">Se il file CDF contiene altri protocolli, l'aggiunta del canale ha esito negativo e non viene visualizzata alcuna finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="ce2ca-113">If the CDF file contains any other protocol, the addition of the channel fails and no dialog box appears.</span></span>

 

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="ce2ca-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="ce2ca-114">Examples</span></span>

<span data-ttu-id="ce2ca-115">Nell'esempio seguente viene illustrato l'utilizzo corretto di questo metodo per JScript incorporato in HTML e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ce2ca-115">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="ce2ca-116">JScript</span><span class="sxs-lookup"><span data-stu-id="ce2ca-116">JScript:</span></span>


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
    function fnShellUIHelperAddChannelJ()
    {
        ShellUIHelper.AddChannel("https://www.microsoft.com/windows/cdf/g_stock.cdf");
    }
</script>

</head>
<body onload=fnShellUIHelperAddChannelJ()>
</body>
</html>
```



<span data-ttu-id="ce2ca-117">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="ce2ca-117">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddChannelVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddChannel ("https://www.microsoft.com/windows/cdf/g_stock.cdf")
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="ce2ca-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce2ca-118">Requirements</span></span>



| <span data-ttu-id="ce2ca-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce2ca-119">Requirement</span></span> | <span data-ttu-id="ce2ca-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ce2ca-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce2ca-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce2ca-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ce2ca-122">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ce2ca-122">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ce2ca-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce2ca-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ce2ca-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ce2ca-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ce2ca-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce2ca-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce2ca-126"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce2ca-126"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="ce2ca-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ce2ca-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce2ca-128"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="ce2ca-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
