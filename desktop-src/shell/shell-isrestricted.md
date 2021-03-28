---
description: Recupera l'impostazione di restrizione di un gruppo dal registro di sistema.
ms.assetid: C4B3B5C0-7445-483a-885F-5283BD4D4B39
title: Metodo Shell. Unrestricted (shldisp. h)
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
ms.openlocfilehash: 2224a3ea4ea26cf39f2e15486de4f96afe5448d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232107"
---
# <a name="shellisrestricted-method"></a><span data-ttu-id="ef7db-103">Shell. Unrestricted (metodo)</span><span class="sxs-lookup"><span data-stu-id="ef7db-103">Shell.IsRestricted method</span></span>

<span data-ttu-id="ef7db-104">Recupera l'impostazione di restrizione di un gruppo dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="ef7db-104">Retrieves a group's restriction setting from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef7db-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ef7db-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="ef7db-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ef7db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef7db-107">*sGroup* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef7db-107">*sGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef7db-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="ef7db-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="ef7db-109">**Stringa** che contiene il nome del gruppo.</span><span class="sxs-lookup"><span data-stu-id="ef7db-109">A **String** that contains the group name.</span></span> <span data-ttu-id="ef7db-110">Questo valore è il nome di una sottochiave del registro di sistema in cui verificare la restrizione.</span><span class="sxs-lookup"><span data-stu-id="ef7db-110">This value is the name of a registry subkey under which to check for the restriction.</span></span>

</dd> <dt>

<span data-ttu-id="ef7db-111">*sRestriction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef7db-111">*sRestriction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef7db-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="ef7db-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="ef7db-113">**Stringa** che contiene la restrizione di cui è necessario recuperare il valore.</span><span class="sxs-lookup"><span data-stu-id="ef7db-113">A **String** that contains the restriction whose value is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef7db-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ef7db-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="ef7db-115">JScript</span><span class="sxs-lookup"><span data-stu-id="ef7db-115">JScript</span></span>

<span data-ttu-id="ef7db-116">Tipo: \**integer \** _</span><span class="sxs-lookup"><span data-stu-id="ef7db-116">Type: \**Integer\** _</span></span>

<span data-ttu-id="ef7db-117">Valore della restrizione.</span><span class="sxs-lookup"><span data-stu-id="ef7db-117">The value of the restriction.</span></span> <span data-ttu-id="ef7db-118">Se la restrizione specificata non viene trovata, il valore restituito è 0.</span><span class="sxs-lookup"><span data-stu-id="ef7db-118">If the specified restriction is not found, the return value is 0.</span></span>

### <a name="vb"></a><span data-ttu-id="ef7db-119">VB</span><span class="sxs-lookup"><span data-stu-id="ef7db-119">VB</span></span>

<span data-ttu-id="ef7db-120">Tipo: _*integer \**_</span><span class="sxs-lookup"><span data-stu-id="ef7db-120">Type: _*Integer\**_</span></span>

<span data-ttu-id="ef7db-121">Valore della restrizione.</span><span class="sxs-lookup"><span data-stu-id="ef7db-121">The value of the restriction.</span></span> <span data-ttu-id="ef7db-122">Se la restrizione specificata non viene trovata, il valore restituito è 0.</span><span class="sxs-lookup"><span data-stu-id="ef7db-122">If the specified restriction is not found, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef7db-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="ef7db-123">Remarks</span></span>

<span data-ttu-id="ef7db-124">_ *Unrestricted*\* cerca prima di tutto un nome di sottochiave che corrisponde a *sGroup* nella chiave seguente.</span><span class="sxs-lookup"><span data-stu-id="ef7db-124">_ *IsRestricted*\* first looks for a subkey name that matches *sGroup* under the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

<span data-ttu-id="ef7db-125">Le restrizioni vengono dichiarate come valori delle sottochiavi dei singoli criteri.</span><span class="sxs-lookup"><span data-stu-id="ef7db-125">Restrictions are declared as values of the individual policy subkeys.</span></span> <span data-ttu-id="ef7db-126">Se la restrizione denominata in *sRestriction* si trova nella sottochiave denominata in *sGroup*, con **restrizioni** viene restituito il valore corrente della restrizione.</span><span class="sxs-lookup"><span data-stu-id="ef7db-126">If the restriction named in *sRestriction* is found in the subkey named in *sGroup*, **IsRestricted** returns the restriction's current value.</span></span> <span data-ttu-id="ef7db-127">Se la restrizione non viene trovata **nel \_ \_ computer locale HKEY**, viene controllata la stessa sottochiave in **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="ef7db-127">If the restriction is not found under **HKEY\_LOCAL\_MACHINE**, the same subkey is checked under **HKEY\_CURRENT\_USER**.</span></span>

<span data-ttu-id="ef7db-128">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ef7db-128">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="ef7db-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="ef7db-129">Examples</span></span>

<span data-ttu-id="ef7db-130">Negli esempi seguenti viene illustrato l'utilizzo di con **restrizioni** per recuperare il valore dei dati della restrizione **undockwithoutlogon** dalla sottochiave di **sistema** .</span><span class="sxs-lookup"><span data-stu-id="ef7db-130">The following examples show the use of **IsRestricted** to retrieve the data value of the **undockwithoutlogon** restriction from the **System** subkey.</span></span> <span data-ttu-id="ef7db-131">L'utilizzo viene visualizzato per JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="ef7db-131">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="ef7db-132">JScript</span><span class="sxs-lookup"><span data-stu-id="ef7db-132">JScript:</span></span>


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



<span data-ttu-id="ef7db-133">VBScript</span><span class="sxs-lookup"><span data-stu-id="ef7db-133">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="ef7db-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef7db-134">Requirements</span></span>



| <span data-ttu-id="ef7db-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef7db-135">Requirement</span></span> | <span data-ttu-id="ef7db-136">Valore</span><span class="sxs-lookup"><span data-stu-id="ef7db-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef7db-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef7db-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ef7db-138">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ef7db-138">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ef7db-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef7db-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ef7db-140">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ef7db-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ef7db-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ef7db-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef7db-142"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef7db-142"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="ef7db-143">IDL</span><span class="sxs-lookup"><span data-stu-id="ef7db-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ef7db-144"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ef7db-144"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="ef7db-145">DLL</span><span class="sxs-lookup"><span data-stu-id="ef7db-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef7db-146"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="ef7db-146"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
