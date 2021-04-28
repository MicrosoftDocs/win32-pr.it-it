---
description: "Metodo IShellDispatch2.IsRestricted: recupera l'impostazione di restrizione di un gruppo dal Registro di sistema."
ms.assetid: 04275c5f-c3ed-4962-882f-2cce0258a9f4
title: Metodo IShellDispatch2.IsRestricted (Shldisp.h)
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
ms.openlocfilehash: b4f482407fadd16d7ecfe9deeafd91b032a9a24f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117099"
---
# <a name="ishelldispatch2isrestricted-method"></a><span data-ttu-id="93dd9-103">Metodo IShellDispatch2.IsRestricted</span><span class="sxs-lookup"><span data-stu-id="93dd9-103">IShellDispatch2.IsRestricted method</span></span>

<span data-ttu-id="93dd9-104">Recupera l'impostazione di restrizione di un gruppo dal Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="93dd9-104">Retrieves a group's restriction setting from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="93dd9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93dd9-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="93dd9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="93dd9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93dd9-107">*sGroup* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="93dd9-107">*sGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93dd9-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="93dd9-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="93dd9-109">Valore **String** contenente il nome del gruppo.</span><span class="sxs-lookup"><span data-stu-id="93dd9-109">A **String** that contains the group name.</span></span> <span data-ttu-id="93dd9-110">Questo valore è il nome di una sottochiave del Registro di sistema in cui verificare la restrizione.</span><span class="sxs-lookup"><span data-stu-id="93dd9-110">This value is the name of a registry subkey under which to check for the restriction.</span></span>

</dd> <dt>

<span data-ttu-id="93dd9-111">*sRestriction* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="93dd9-111">*sRestriction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93dd9-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="93dd9-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="93dd9-113">Valore **String** che contiene la restrizione il cui valore deve essere recuperato.</span><span class="sxs-lookup"><span data-stu-id="93dd9-113">A **String** that contains the restriction whose value is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93dd9-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93dd9-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="93dd9-115">JScript</span><span class="sxs-lookup"><span data-stu-id="93dd9-115">JScript</span></span>

<span data-ttu-id="93dd9-116">Tipo: **\* Integer**</span><span class="sxs-lookup"><span data-stu-id="93dd9-116">Type: **Integer\***</span></span>

<span data-ttu-id="93dd9-117">Valore della restrizione.</span><span class="sxs-lookup"><span data-stu-id="93dd9-117">The value of the restriction.</span></span> <span data-ttu-id="93dd9-118">Se la restrizione specificata non viene trovata, il valore restituito è 0.</span><span class="sxs-lookup"><span data-stu-id="93dd9-118">If the specified restriction is not found, the return value is 0.</span></span>

### <a name="vb"></a><span data-ttu-id="93dd9-119">VB</span><span class="sxs-lookup"><span data-stu-id="93dd9-119">VB</span></span>

<span data-ttu-id="93dd9-120">Tipo: **\* Integer**</span><span class="sxs-lookup"><span data-stu-id="93dd9-120">Type: **Integer\***</span></span>

<span data-ttu-id="93dd9-121">Valore della restrizione.</span><span class="sxs-lookup"><span data-stu-id="93dd9-121">The value of the restriction.</span></span> <span data-ttu-id="93dd9-122">Se la restrizione specificata non viene trovata, il valore restituito è 0.</span><span class="sxs-lookup"><span data-stu-id="93dd9-122">If the specified restriction is not found, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="93dd9-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="93dd9-123">Remarks</span></span>

<span data-ttu-id="93dd9-124">Questo metodo viene implementato e accessibile tramite il [**metodo Shell.IsRestricted.**](./shell-isrestricted.md)</span><span class="sxs-lookup"><span data-stu-id="93dd9-124">This method is implemented and accessed through the [**Shell.IsRestricted**](./shell-isrestricted.md) method.</span></span>

<span data-ttu-id="93dd9-125">**IsRestricted** cerca innanzitutto un nome di sottochiave che corrisponde *a sGroup* nella chiave seguente.</span><span class="sxs-lookup"><span data-stu-id="93dd9-125">**IsRestricted** first looks for a subkey name that matches *sGroup* under the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

<span data-ttu-id="93dd9-126">Le restrizioni vengono dichiarate come valori delle singole sottochiavi dei criteri.</span><span class="sxs-lookup"><span data-stu-id="93dd9-126">Restrictions are declared as values of the individual policy subkeys.</span></span> <span data-ttu-id="93dd9-127">Se la restrizione denominata in *sRestriction* viene trovata nella sottochiave denominata in *sGroup*, **IsRestricted** restituisce il valore corrente della restrizione.</span><span class="sxs-lookup"><span data-stu-id="93dd9-127">If the restriction named in *sRestriction* is found in the subkey named in *sGroup*, **IsRestricted** returns the restriction's current value.</span></span> <span data-ttu-id="93dd9-128">Se la restrizione non viene trovata in **HKEY \_ LOCAL \_ MACHINE**, la stessa sottochiave viene controllata in **HKEY \_ CURRENT \_ USER**.</span><span class="sxs-lookup"><span data-stu-id="93dd9-128">If the restriction is not found under **HKEY\_LOCAL\_MACHINE**, the same subkey is checked under **HKEY\_CURRENT\_USER**.</span></span>

<span data-ttu-id="93dd9-129">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="93dd9-129">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="93dd9-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="93dd9-130">Examples</span></span>

<span data-ttu-id="93dd9-131">Gli esempi seguenti illustrano l'uso di **IsRestricted** per recuperare il valore dei dati della **restrizione undockwithoutlogon** dalla **sottochiave System.**</span><span class="sxs-lookup"><span data-stu-id="93dd9-131">The following examples show the use of **IsRestricted** to retrieve the data value of the **undockwithoutlogon** restriction from the **System** subkey.</span></span> <span data-ttu-id="93dd9-132">L'utilizzo viene visualizzato per JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="93dd9-132">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="93dd9-133">Jscript:</span><span class="sxs-lookup"><span data-stu-id="93dd9-133">JScript:</span></span>


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



<span data-ttu-id="93dd9-134">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="93dd9-134">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="93dd9-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93dd9-135">Requirements</span></span>



| <span data-ttu-id="93dd9-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="93dd9-136">Requirement</span></span> | <span data-ttu-id="93dd9-137">Valore</span><span class="sxs-lookup"><span data-stu-id="93dd9-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93dd9-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93dd9-138">Minimum supported client</span></span><br/> | <span data-ttu-id="93dd9-139">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="93dd9-139">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="93dd9-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93dd9-140">Minimum supported server</span></span><br/> | <span data-ttu-id="93dd9-141">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="93dd9-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="93dd9-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="93dd9-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="93dd9-143"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="93dd9-143"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="93dd9-144">Idl</span><span class="sxs-lookup"><span data-stu-id="93dd9-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="93dd9-145"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="93dd9-145"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="93dd9-146">DLL</span><span class="sxs-lookup"><span data-stu-id="93dd9-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93dd9-147"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="93dd9-147"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
