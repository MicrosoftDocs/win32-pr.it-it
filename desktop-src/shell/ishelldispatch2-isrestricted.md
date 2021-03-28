---
description: Recupera l'impostazione di restrizione di un gruppo dal registro di sistema.
ms.assetid: 04275c5f-c3ed-4962-882f-2cce0258a9f4
title: Metodo IShellDispatch2. Unrestricted (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.IsRestricted
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f666a9ed3407d12eb9cf2c28ae062a9886d7a2cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978066"
---
# <a name="ishelldispatch2isrestricted-method"></a><span data-ttu-id="fd55a-103">Metodo IShellDispatch2. Unrestricted</span><span class="sxs-lookup"><span data-stu-id="fd55a-103">IShellDispatch2.IsRestricted method</span></span>

<span data-ttu-id="fd55a-104">Recupera l'impostazione di restrizione di un gruppo dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="fd55a-104">Retrieves a group's restriction setting from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd55a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd55a-105">Syntax</span></span>


```JScript
iRetVal = IShellDispatch2.IsRestricted(
  sGroup,
  sRestriction
)
```


```VB

IShellDispatch2.IsRestricted( _
  ByVal sGroup As BSTR, _
  ByVal sRestriction As BSTR _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="fd55a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fd55a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd55a-107">*sGroup* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd55a-107">*sGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd55a-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="fd55a-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="fd55a-109">**Stringa** che contiene il nome del gruppo.</span><span class="sxs-lookup"><span data-stu-id="fd55a-109">A **String** that contains the group name.</span></span> <span data-ttu-id="fd55a-110">Questo valore è il nome di una sottochiave del registro di sistema in cui verificare la restrizione.</span><span class="sxs-lookup"><span data-stu-id="fd55a-110">This value is the name of a registry subkey under which to check for the restriction.</span></span>

</dd> <dt>

<span data-ttu-id="fd55a-111">*sRestriction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd55a-111">*sRestriction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd55a-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="fd55a-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="fd55a-113">**Stringa** che contiene la restrizione di cui è necessario recuperare il valore.</span><span class="sxs-lookup"><span data-stu-id="fd55a-113">A **String** that contains the restriction whose value is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd55a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fd55a-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="fd55a-115">JScript</span><span class="sxs-lookup"><span data-stu-id="fd55a-115">JScript</span></span>

<span data-ttu-id="fd55a-116">Tipo: \**integer \** _</span><span class="sxs-lookup"><span data-stu-id="fd55a-116">Type: \**Integer\** _</span></span>

<span data-ttu-id="fd55a-117">Valore della restrizione.</span><span class="sxs-lookup"><span data-stu-id="fd55a-117">The value of the restriction.</span></span> <span data-ttu-id="fd55a-118">Se la restrizione specificata non viene trovata, il valore restituito è 0.</span><span class="sxs-lookup"><span data-stu-id="fd55a-118">If the specified restriction is not found, the return value is 0.</span></span>

### <a name="vb"></a><span data-ttu-id="fd55a-119">VB</span><span class="sxs-lookup"><span data-stu-id="fd55a-119">VB</span></span>

<span data-ttu-id="fd55a-120">Tipo: _*integer \**_</span><span class="sxs-lookup"><span data-stu-id="fd55a-120">Type: _*Integer\**_</span></span>

<span data-ttu-id="fd55a-121">Valore della restrizione.</span><span class="sxs-lookup"><span data-stu-id="fd55a-121">The value of the restriction.</span></span> <span data-ttu-id="fd55a-122">Se la restrizione specificata non viene trovata, il valore restituito è 0.</span><span class="sxs-lookup"><span data-stu-id="fd55a-122">If the specified restriction is not found, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd55a-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd55a-123">Remarks</span></span>

<span data-ttu-id="fd55a-124">Questo metodo viene implementato e accessibile tramite il metodo [_ *Shell. Unrestricted* \*](./shell-isrestricted.md) .</span><span class="sxs-lookup"><span data-stu-id="fd55a-124">This method is implemented and accessed through the [_ *Shell.IsRestricted*\*](./shell-isrestricted.md) method.</span></span>

<span data-ttu-id="fd55a-125">Con la prima **limitazione** viene eseguita la ricerca di un nome di sottochiave che corrisponde a *sGroup* nella chiave seguente.</span><span class="sxs-lookup"><span data-stu-id="fd55a-125">**IsRestricted** first looks for a subkey name that matches *sGroup* under the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

<span data-ttu-id="fd55a-126">Le restrizioni vengono dichiarate come valori delle sottochiavi dei singoli criteri.</span><span class="sxs-lookup"><span data-stu-id="fd55a-126">Restrictions are declared as values of the individual policy subkeys.</span></span> <span data-ttu-id="fd55a-127">Se la restrizione denominata in *sRestriction* si trova nella sottochiave denominata in *sGroup*, con **restrizioni** viene restituito il valore corrente della restrizione.</span><span class="sxs-lookup"><span data-stu-id="fd55a-127">If the restriction named in *sRestriction* is found in the subkey named in *sGroup*, **IsRestricted** returns the restriction's current value.</span></span> <span data-ttu-id="fd55a-128">Se la restrizione non viene trovata **nel \_ \_ computer locale HKEY**, viene controllata la stessa sottochiave in **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="fd55a-128">If the restriction is not found under **HKEY\_LOCAL\_MACHINE**, the same subkey is checked under **HKEY\_CURRENT\_USER**.</span></span>

<span data-ttu-id="fd55a-129">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="fd55a-129">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="fd55a-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="fd55a-130">Examples</span></span>

<span data-ttu-id="fd55a-131">Negli esempi seguenti viene illustrato l'utilizzo di con **restrizioni** per recuperare il valore dei dati della restrizione **undockwithoutlogon** dalla sottochiave di **sistema** .</span><span class="sxs-lookup"><span data-stu-id="fd55a-131">The following examples show the use of **IsRestricted** to retrieve the data value of the **undockwithoutlogon** restriction from the **System** subkey.</span></span> <span data-ttu-id="fd55a-132">L'utilizzo viene visualizzato per JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="fd55a-132">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="fd55a-133">JScript</span><span class="sxs-lookup"><span data-stu-id="fd55a-133">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsRestricedJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var lReturn;
        
        lReturn = objShell.IsRestricted("system", "undockwithoutlogon");
        document.write(lReturn);
    }
</script>
```



<span data-ttu-id="fd55a-134">VBScript</span><span class="sxs-lookup"><span data-stu-id="fd55a-134">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsRestricedVB()
        dim objShell
        dim lReturn

        set objShell = CreateObject("shell.application")

        lReturn = objShell.IsRestricted("system", "undockwithoutlogon")
        document.write(lReturn)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="fd55a-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd55a-135">Requirements</span></span>



| <span data-ttu-id="fd55a-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd55a-136">Requirement</span></span> | <span data-ttu-id="fd55a-137">Valore</span><span class="sxs-lookup"><span data-stu-id="fd55a-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd55a-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd55a-138">Minimum supported client</span></span><br/> | <span data-ttu-id="fd55a-139">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fd55a-139">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fd55a-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd55a-140">Minimum supported server</span></span><br/> | <span data-ttu-id="fd55a-141">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fd55a-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fd55a-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fd55a-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd55a-143"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd55a-143"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="fd55a-144">IDL</span><span class="sxs-lookup"><span data-stu-id="fd55a-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fd55a-145"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fd55a-145"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="fd55a-146">DLL</span><span class="sxs-lookup"><span data-stu-id="fd55a-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd55a-147"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="fd55a-147"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
