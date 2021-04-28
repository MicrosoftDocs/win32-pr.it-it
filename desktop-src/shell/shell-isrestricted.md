---
description: "Metodo Shell.IsRestricted: recupera l'impostazione di restrizione di un gruppo dal Registro di sistema."
ms.assetid: C4B3B5C0-7445-483a-885F-5283BD4D4B39
title: Metodo Shell.IsRestricted (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.IsRestricted
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3e428c914cf95d282fd721071009efc70fcb3a4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104259"
---
# <a name="shellisrestricted-method"></a><span data-ttu-id="f617d-103">Metodo Shell.IsRestricted</span><span class="sxs-lookup"><span data-stu-id="f617d-103">Shell.IsRestricted method</span></span>

<span data-ttu-id="f617d-104">Recupera l'impostazione di restrizione di un gruppo dal Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="f617d-104">Retrieves a group's restriction setting from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="f617d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f617d-105">Syntax</span></span>


```JScript
iRetVal = Shell.IsRestricted(
  sGroup,
  sRestriction
)
```


```VB

Shell.IsRestricted( _
  ByVal sGroup As BSTR, _
  ByVal sRestriction As BSTR _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="f617d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f617d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f617d-107">*sGroup* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f617d-107">*sGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f617d-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="f617d-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="f617d-109">Valore **String** contenente il nome del gruppo.</span><span class="sxs-lookup"><span data-stu-id="f617d-109">A **String** that contains the group name.</span></span> <span data-ttu-id="f617d-110">Questo valore è il nome di una sottochiave del Registro di sistema in cui verificare la restrizione.</span><span class="sxs-lookup"><span data-stu-id="f617d-110">This value is the name of a registry subkey under which to check for the restriction.</span></span>

</dd> <dt>

<span data-ttu-id="f617d-111">*sRestriction* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f617d-111">*sRestriction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f617d-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="f617d-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="f617d-113">Valore **String** contenente la restrizione di cui recuperare il valore.</span><span class="sxs-lookup"><span data-stu-id="f617d-113">A **String** that contains the restriction whose value is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f617d-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f617d-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="f617d-115">JScript</span><span class="sxs-lookup"><span data-stu-id="f617d-115">JScript</span></span>

<span data-ttu-id="f617d-116">Tipo: **\* Integer**</span><span class="sxs-lookup"><span data-stu-id="f617d-116">Type: **Integer\***</span></span>

<span data-ttu-id="f617d-117">Valore della restrizione.</span><span class="sxs-lookup"><span data-stu-id="f617d-117">The value of the restriction.</span></span> <span data-ttu-id="f617d-118">Se la restrizione specificata non viene trovata, il valore restituito è 0.</span><span class="sxs-lookup"><span data-stu-id="f617d-118">If the specified restriction is not found, the return value is 0.</span></span>

### <a name="vb"></a><span data-ttu-id="f617d-119">VB</span><span class="sxs-lookup"><span data-stu-id="f617d-119">VB</span></span>

<span data-ttu-id="f617d-120">Tipo: **\* Integer**</span><span class="sxs-lookup"><span data-stu-id="f617d-120">Type: **Integer\***</span></span>

<span data-ttu-id="f617d-121">Valore della restrizione.</span><span class="sxs-lookup"><span data-stu-id="f617d-121">The value of the restriction.</span></span> <span data-ttu-id="f617d-122">Se la restrizione specificata non viene trovata, il valore restituito è 0.</span><span class="sxs-lookup"><span data-stu-id="f617d-122">If the specified restriction is not found, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="f617d-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="f617d-123">Remarks</span></span>

<span data-ttu-id="f617d-124">**IsRestricted** cerca prima di tutto un nome di sottochiave che corrisponda *a sGroup* nella chiave seguente.</span><span class="sxs-lookup"><span data-stu-id="f617d-124">**IsRestricted** first looks for a subkey name that matches *sGroup* under the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

<span data-ttu-id="f617d-125">Le restrizioni vengono dichiarate come valori delle singole sottochiavi dei criteri.</span><span class="sxs-lookup"><span data-stu-id="f617d-125">Restrictions are declared as values of the individual policy subkeys.</span></span> <span data-ttu-id="f617d-126">Se la restrizione denominata in *sRestriction* viene trovata nella sottochiave denominata in *sGroup*, **IsRestricted** restituisce il valore corrente della restrizione.</span><span class="sxs-lookup"><span data-stu-id="f617d-126">If the restriction named in *sRestriction* is found in the subkey named in *sGroup*, **IsRestricted** returns the restriction's current value.</span></span> <span data-ttu-id="f617d-127">Se la restrizione non viene trovata in **HKEY \_ LOCAL \_ MACHINE**, la stessa sottochiave viene controllata in **HKEY \_ CURRENT \_ USER**.</span><span class="sxs-lookup"><span data-stu-id="f617d-127">If the restriction is not found under **HKEY\_LOCAL\_MACHINE**, the same subkey is checked under **HKEY\_CURRENT\_USER**.</span></span>

<span data-ttu-id="f617d-128">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f617d-128">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="f617d-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="f617d-129">Examples</span></span>

<span data-ttu-id="f617d-130">Negli esempi seguenti viene illustrato l'uso di **IsRestricted** per recuperare il valore dei dati della restrizione **undockwithoutlogon** dalla **sottochiave System.**</span><span class="sxs-lookup"><span data-stu-id="f617d-130">The following examples show the use of **IsRestricted** to retrieve the data value of the **undockwithoutlogon** restriction from the **System** subkey.</span></span> <span data-ttu-id="f617d-131">L'utilizzo è illustrato per JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="f617d-131">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="f617d-132">Jscript:</span><span class="sxs-lookup"><span data-stu-id="f617d-132">JScript:</span></span>


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



<span data-ttu-id="f617d-133">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="f617d-133">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="f617d-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f617d-134">Requirements</span></span>



| <span data-ttu-id="f617d-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="f617d-135">Requirement</span></span> | <span data-ttu-id="f617d-136">Valore</span><span class="sxs-lookup"><span data-stu-id="f617d-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f617d-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f617d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f617d-138">Solo app desktop windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f617d-138">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f617d-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f617d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f617d-140">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f617d-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f617d-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f617d-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="f617d-142"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="f617d-142"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="f617d-143">Idl</span><span class="sxs-lookup"><span data-stu-id="f617d-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f617d-144"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="f617d-144"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="f617d-145">DLL</span><span class="sxs-lookup"><span data-stu-id="f617d-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f617d-146"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="f617d-146"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
