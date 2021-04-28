---
description: 'Metodo IShellDispatch4.ExplorerPolicy: ottiene il valore per un criterio Internet Explorer Windows specificato.'
ms.assetid: 490c3e18-b606-456a-9016-dc4f7bad2bc3
title: Metodo IShellDispatch4.ExplorerPolicy (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.ExplorerPolicy
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4a03d61905bdb1f2b16de11cc604625d8e71a7ea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116829"
---
# <a name="ishelldispatch4explorerpolicy-method"></a><span data-ttu-id="1379c-103">Metodo IShellDispatch4.ExplorerPolicy</span><span class="sxs-lookup"><span data-stu-id="1379c-103">IShellDispatch4.ExplorerPolicy method</span></span>

<span data-ttu-id="1379c-104">Ottiene il valore per un criterio di Internet Explorer Windows specificato.</span><span class="sxs-lookup"><span data-stu-id="1379c-104">Gets the value for a specified Windows Internet Explorer policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="1379c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1379c-105">Syntax</span></span>


```JScript
retVal = IShellDispatch4.ExplorerPolicy(
  bstrPolicyName
)
```


```VB

IShellDispatch4.ExplorerPolicy( _
  ByVal bstrPolicyName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="1379c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1379c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1379c-107">*bstrPolicyName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1379c-107">*bstrPolicyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1379c-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="1379c-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="1379c-109">Valore **String** che specifica il nome dei criteri.</span><span class="sxs-lookup"><span data-stu-id="1379c-109">A **String** that specifies the name of the policy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1379c-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1379c-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="1379c-111">JScript</span><span class="sxs-lookup"><span data-stu-id="1379c-111">JScript</span></span>

<span data-ttu-id="1379c-112">Tipo: **\* Variante**</span><span class="sxs-lookup"><span data-stu-id="1379c-112">Type: **Variant\***</span></span>

<span data-ttu-id="1379c-113">Valore associato al nome del criterio specificato.</span><span class="sxs-lookup"><span data-stu-id="1379c-113">The value associated with the specified policy name.</span></span>

### <a name="vb"></a><span data-ttu-id="1379c-114">VB</span><span class="sxs-lookup"><span data-stu-id="1379c-114">VB</span></span>

<span data-ttu-id="1379c-115">Tipo: **\* Variante**</span><span class="sxs-lookup"><span data-stu-id="1379c-115">Type: **Variant\***</span></span>

<span data-ttu-id="1379c-116">Valore associato al nome del criterio specificato.</span><span class="sxs-lookup"><span data-stu-id="1379c-116">The value associated with the specified policy name.</span></span>

## <a name="remarks"></a><span data-ttu-id="1379c-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="1379c-117">Remarks</span></span>

<span data-ttu-id="1379c-118">Gli amministratori di rete possono controllare e gestire l'ambiente di elaborazione degli utenti impostando criteri.</span><span class="sxs-lookup"><span data-stu-id="1379c-118">Network Administrators can control and manage the computing environment of their users by setting policies.</span></span>

<span data-ttu-id="1379c-119">Il nome del valore specificato deve essere all'interno **della sottochiave HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Policies** \\ **Explorer.**</span><span class="sxs-lookup"><span data-stu-id="1379c-119">The specified value name must be within the **HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Policies**\\**Explorer** subkey.</span></span> <span data-ttu-id="1379c-120">Se il nome del valore non esiste, il metodo restituisce **null.**</span><span class="sxs-lookup"><span data-stu-id="1379c-120">If the value name does not exist then the method returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="1379c-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="1379c-121">Examples</span></span>

<span data-ttu-id="1379c-122">Gli esempi seguenti illustrano l'uso corretto di **ExplorerPolicy** per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1379c-122">The following examples show the proper use of **ExplorerPolicy** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="1379c-123">Jscript:</span><span class="sxs-lookup"><span data-stu-id="1379c-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ExplorerPolicyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;
        
        vReturn = objshell.ExplorerPolicy("ValueName");
        alert(vReturn);
    }
</script>
```



<span data-ttu-id="1379c-124">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="1379c-124">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4ExplorerPolicyVB()
        dim objShell
        dim vReturn
        
        set objShell = CreateObject("shell.application")
            vReturn = objshell.ExplorerPolicy("ValueName")
            alert(vReturn)
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="1379c-125">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="1379c-125">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ExplorerPolicyVB()
    Dim objShell As Shell
    Dim vReturn  As Variant
    
    Set objShell = New Shell
        vReturn = objshell.ExplorerPolicy("ValueName")
        Debug.Print vReturn
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="1379c-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1379c-126">Requirements</span></span>



| <span data-ttu-id="1379c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="1379c-127">Requirement</span></span> | <span data-ttu-id="1379c-128">Valore</span><span class="sxs-lookup"><span data-stu-id="1379c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1379c-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1379c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1379c-130">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="1379c-130">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="1379c-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1379c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1379c-132">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1379c-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1379c-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1379c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="1379c-134"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="1379c-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="1379c-135">Idl</span><span class="sxs-lookup"><span data-stu-id="1379c-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1379c-136"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="1379c-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="1379c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="1379c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1379c-138"><dt>Shell32.dll (versione 6.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="1379c-138"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
