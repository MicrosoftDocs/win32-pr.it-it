---
description: Consente di visualizzare la finestra di dialogo Trova stampante.
ms.assetid: a3d1e810-f0cf-48ec-93da-5cc01117c5d4
title: Metodo IShellDispatch2. FindPrinter (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.FindPrinter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 81124e3f0d04244b9b81e812e090bde25971c17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226366"
---
# <a name="ishelldispatch2findprinter-method"></a><span data-ttu-id="ca85e-103">IShellDispatch2. FindPrinter, metodo</span><span class="sxs-lookup"><span data-stu-id="ca85e-103">IShellDispatch2.FindPrinter method</span></span>

<span data-ttu-id="ca85e-104">Consente di visualizzare la finestra di dialogo **Trova stampante** .</span><span class="sxs-lookup"><span data-stu-id="ca85e-104">Displays the **Find Printer** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca85e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca85e-105">Syntax</span></span>


```JScript
iRetVal = IShellDispatch2.FindPrinter(
  [ sName ],
  [ sLocation ],
  [ sModel ]
)
```


```VB

IShellDispatch2.FindPrinter( _
  [ ByVal sName As BSTR ], _
  [ ByVal sLocation As BSTR ], _
  [ ByVal sModel As BSTR ] _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="ca85e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca85e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca85e-107">*sName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ca85e-107">*sName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ca85e-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="ca85e-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="ca85e-109">**Stringa** che contiene il nome della stampante.</span><span class="sxs-lookup"><span data-stu-id="ca85e-109">A **String** that contains the printer name.</span></span>

</dd> <dt>

<span data-ttu-id="ca85e-110">*sLocation* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ca85e-110">*sLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ca85e-111">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="ca85e-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="ca85e-112">**Stringa** che contiene la posizione della stampante.</span><span class="sxs-lookup"><span data-stu-id="ca85e-112">A **String** that contains the printer location.</span></span>

</dd> <dt>

<span data-ttu-id="ca85e-113">*sModel* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ca85e-113">*sModel* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ca85e-114">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="ca85e-114">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="ca85e-115">**Stringa** che contiene il modello di stampante.</span><span class="sxs-lookup"><span data-stu-id="ca85e-115">A **String** that contains the printer model.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca85e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca85e-116">Remarks</span></span>

<span data-ttu-id="ca85e-117">Questo metodo viene implementato e accessibile tramite il metodo [**Shell. FindPrinter**](./shell-findprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="ca85e-117">This method is implemented and accessed through the [**Shell.FindPrinter**](./shell-findprinter.md) method.</span></span>

<span data-ttu-id="ca85e-118">Se si assegnano stringhe a uno o più parametri facoltativi, questi vengono visualizzati come valori predefiniti nel controllo di modifica associato quando viene visualizzata la finestra di dialogo **Trova stampante** .</span><span class="sxs-lookup"><span data-stu-id="ca85e-118">If you assign strings to one or more of the optional parameters, they are displayed as default values in the associated edit control when the **Find Printer** dialog box is displayed.</span></span> <span data-ttu-id="ca85e-119">L'utente può accettare o eseguire l'override di questi valori.</span><span class="sxs-lookup"><span data-stu-id="ca85e-119">The user can either accept or override these values.</span></span> <span data-ttu-id="ca85e-120">Se non viene assegnato alcun valore a un parametro, la casella di modifica associata è vuota e l'utente deve immettere un valore.</span><span class="sxs-lookup"><span data-stu-id="ca85e-120">If no value is assigned to a parameter, the associated edit box is empty and the user must enter a value.</span></span>

<span data-ttu-id="ca85e-121">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ca85e-121">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="ca85e-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="ca85e-122">Examples</span></span>

<span data-ttu-id="ca85e-123">Negli esempi seguenti viene illustrato l'utilizzo di **FindPrinter** per visualizzare la finestra di dialogo **Trova stampante** per una particolare applicazione.</span><span class="sxs-lookup"><span data-stu-id="ca85e-123">The following examples show the use of **FindPrinter** to display the **Find Printer** dialog box for a particular application.</span></span> <span data-ttu-id="ca85e-124">L'utilizzo viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ca85e-124">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="ca85e-125">JScript</span><span class="sxs-lookup"><span data-stu-id="ca85e-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



<span data-ttu-id="ca85e-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="ca85e-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFindPrinterVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")
        objShell.FindPrinter()

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="ca85e-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca85e-127">Requirements</span></span>



| <span data-ttu-id="ca85e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca85e-128">Requirement</span></span> | <span data-ttu-id="ca85e-129">Valore</span><span class="sxs-lookup"><span data-stu-id="ca85e-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca85e-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca85e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ca85e-131">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ca85e-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ca85e-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca85e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ca85e-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ca85e-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ca85e-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca85e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca85e-135"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca85e-135"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="ca85e-136">IDL</span><span class="sxs-lookup"><span data-stu-id="ca85e-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ca85e-137"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ca85e-137"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="ca85e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ca85e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca85e-139"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="ca85e-139"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
