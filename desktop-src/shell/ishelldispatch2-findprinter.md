---
description: 'Metodo IShellDispatch2.FindPrinter: visualizza la finestra di dialogo Trova stampante.'
ms.assetid: a3d1e810-f0cf-48ec-93da-5cc01117c5d4
title: Metodo IShellDispatch2.FindPrinter (Shldisp.h)
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
ms.openlocfilehash: 64a3975039255de76b3e59432b0848cc2cb1795b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117119"
---
# <a name="ishelldispatch2findprinter-method"></a><span data-ttu-id="b5dc5-103">Metodo IShellDispatch2.FindPrinter</span><span class="sxs-lookup"><span data-stu-id="b5dc5-103">IShellDispatch2.FindPrinter method</span></span>

<span data-ttu-id="b5dc5-104">Visualizza la **finestra di dialogo Trova** stampante.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-104">Displays the **Find Printer** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5dc5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5dc5-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="b5dc5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5dc5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5dc5-107">*sName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="b5dc5-107">*sName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b5dc5-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="b5dc5-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="b5dc5-109">Valore **String** contenente il nome della stampante.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-109">A **String** that contains the printer name.</span></span>

</dd> <dt>

<span data-ttu-id="b5dc5-110">*sLocation* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="b5dc5-110">*sLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b5dc5-111">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="b5dc5-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="b5dc5-112">Valore **String** che contiene il percorso della stampante.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-112">A **String** that contains the printer location.</span></span>

</dd> <dt>

<span data-ttu-id="b5dc5-113">*sModel* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="b5dc5-113">*sModel* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b5dc5-114">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="b5dc5-114">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="b5dc5-115">Valore **String** che contiene il modello di stampante.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-115">A **String** that contains the printer model.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5dc5-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5dc5-116">Remarks</span></span>

<span data-ttu-id="b5dc5-117">Questo metodo viene implementato e accessibile tramite il [**metodo Shell.FindPrinter.**](./shell-findprinter.md)</span><span class="sxs-lookup"><span data-stu-id="b5dc5-117">This method is implemented and accessed through the [**Shell.FindPrinter**](./shell-findprinter.md) method.</span></span>

<span data-ttu-id="b5dc5-118">Se si assegnano stringhe a uno o più parametri facoltativi, vengono visualizzate  come valori predefiniti nel controllo di modifica associato quando viene visualizzata la finestra di dialogo Trova stampante .</span><span class="sxs-lookup"><span data-stu-id="b5dc5-118">If you assign strings to one or more of the optional parameters, they are displayed as default values in the associated edit control when the **Find Printer** dialog box is displayed.</span></span> <span data-ttu-id="b5dc5-119">L'utente può accettare o eseguire l'override di questi valori.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-119">The user can either accept or override these values.</span></span> <span data-ttu-id="b5dc5-120">Se a un parametro non viene assegnato alcun valore, la casella di modifica associata è vuota e l'utente deve immettere un valore.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-120">If no value is assigned to a parameter, the associated edit box is empty and the user must enter a value.</span></span>

<span data-ttu-id="b5dc5-121">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-121">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="b5dc5-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="b5dc5-122">Examples</span></span>

<span data-ttu-id="b5dc5-123">Negli esempi seguenti viene illustrato l'uso di **FindPrinter** per visualizzare la **finestra di** dialogo Trova stampante per una determinata applicazione.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-123">The following examples show the use of **FindPrinter** to display the **Find Printer** dialog box for a particular application.</span></span> <span data-ttu-id="b5dc5-124">L'utilizzo è illustrato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b5dc5-124">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b5dc5-125">Jscript:</span><span class="sxs-lookup"><span data-stu-id="b5dc5-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



<span data-ttu-id="b5dc5-126">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="b5dc5-126">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="b5dc5-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5dc5-127">Requirements</span></span>



| <span data-ttu-id="b5dc5-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5dc5-128">Requirement</span></span> | <span data-ttu-id="b5dc5-129">Valore</span><span class="sxs-lookup"><span data-stu-id="b5dc5-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5dc5-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5dc5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b5dc5-131">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b5dc5-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b5dc5-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5dc5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b5dc5-133">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b5dc5-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b5dc5-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5dc5-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5dc5-135"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="b5dc5-135"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="b5dc5-136">Idl</span><span class="sxs-lookup"><span data-stu-id="b5dc5-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b5dc5-137"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="b5dc5-137"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="b5dc5-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b5dc5-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5dc5-139"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="b5dc5-139"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
