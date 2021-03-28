---
description: Ottiene il valore per i criteri di Windows Internet Explorer specificati.
ms.assetid: 47E17F6A-ED43-44cd-AF77-A6E49865E1B5
title: Metodo Shell. ExplorerPolicy (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ExplorerPolicy
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: fea5192990b8c19c8ddfe8ffad6efe21b98625c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980863"
---
# <a name="shellexplorerpolicy-method"></a><span data-ttu-id="963b9-103">Shell. ExplorerPolicy, metodo</span><span class="sxs-lookup"><span data-stu-id="963b9-103">Shell.ExplorerPolicy method</span></span>

<span data-ttu-id="963b9-104">Ottiene il valore per i criteri di Windows Internet Explorer specificati.</span><span class="sxs-lookup"><span data-stu-id="963b9-104">Gets the value for a specified Windows Internet Explorer policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="963b9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="963b9-105">Syntax</span></span>


```JScript
retVal = Shell.ExplorerPolicy(
  bstrPolicyName
)
```


```VB

Shell.ExplorerPolicy( _
  ByVal bstrPolicyName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="963b9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="963b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="963b9-107">*bstrPolicyName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="963b9-107">*bstrPolicyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="963b9-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="963b9-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="963b9-109">**Stringa** che specifica il nome dei criteri.</span><span class="sxs-lookup"><span data-stu-id="963b9-109">A **String** that specifies the name of the policy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="963b9-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="963b9-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="963b9-111">JScript</span><span class="sxs-lookup"><span data-stu-id="963b9-111">JScript</span></span>

<span data-ttu-id="963b9-112">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="963b9-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="963b9-113">Valore associato al nome dei criteri specificato.</span><span class="sxs-lookup"><span data-stu-id="963b9-113">The value associated with the specified policy name.</span></span>

### <a name="vb"></a><span data-ttu-id="963b9-114">VB</span><span class="sxs-lookup"><span data-stu-id="963b9-114">VB</span></span>

<span data-ttu-id="963b9-115">Tipo: _*Variant \**_</span><span class="sxs-lookup"><span data-stu-id="963b9-115">Type: _*Variant\**_</span></span>

<span data-ttu-id="963b9-116">Valore associato al nome dei criteri specificato.</span><span class="sxs-lookup"><span data-stu-id="963b9-116">The value associated with the specified policy name.</span></span>

## <a name="remarks"></a><span data-ttu-id="963b9-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="963b9-117">Remarks</span></span>

<span data-ttu-id="963b9-118">Gli amministratori di rete possono controllare e gestire l'ambiente di elaborazione dei propri utenti impostando i criteri.</span><span class="sxs-lookup"><span data-stu-id="963b9-118">Network Administrators can control and manage the computing environment of their users by setting policies.</span></span>

<span data-ttu-id="963b9-119">Il nome del valore specificato deve essere incluso nella sottochiave _ \*HKEY \_ Current \_ **\\** software utente **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Policies **\\** Explorer\*\*.</span><span class="sxs-lookup"><span data-stu-id="963b9-119">The specified value name must be within the _ *HKEY\_CURRENT\_USER **\\** Software **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Policies **\\** Explorer*\* subkey.</span></span> <span data-ttu-id="963b9-120">Se il nome del valore non esiste, il metodo restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="963b9-120">If the value name does not exist then the method returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="963b9-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="963b9-121">Examples</span></span>

<span data-ttu-id="963b9-122">Gli esempi seguenti illustrano l'uso corretto di **ExplorerPolicy** per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="963b9-122">The following examples show the proper use of **ExplorerPolicy** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="963b9-123">JScript</span><span class="sxs-lookup"><span data-stu-id="963b9-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ExplorerPolicyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;
        
        vReturn = objShell.ExplorerPolicy("ValueName");
        alert(vReturn);
    }
</script>
```



<span data-ttu-id="963b9-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="963b9-124">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4ExplorerPolicyVB()
        dim objShell
        dim vReturn
        
        set objShell = CreateObject("shell.application")
            vReturn = objShell.ExplorerPolicy("ValueName")
            alert(vReturn)
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="963b9-125">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="963b9-125">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ExplorerPolicyVB()
    Dim objShell As Shell
    Dim vReturn  As Variant
    
    Set objShell = New Shell
        vReturn = objShell.ExplorerPolicy("ValueName")
        Debug.Print vReturn
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="963b9-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="963b9-126">Requirements</span></span>



| <span data-ttu-id="963b9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="963b9-127">Requirement</span></span> | <span data-ttu-id="963b9-128">Valore</span><span class="sxs-lookup"><span data-stu-id="963b9-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="963b9-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="963b9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="963b9-130">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="963b9-130">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="963b9-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="963b9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="963b9-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="963b9-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="963b9-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="963b9-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="963b9-134"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="963b9-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="963b9-135">IDL</span><span class="sxs-lookup"><span data-stu-id="963b9-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="963b9-136"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="963b9-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="963b9-137">DLL</span><span class="sxs-lookup"><span data-stu-id="963b9-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="963b9-138"><dt>Shell32.dll (versione 6,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="963b9-138"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
