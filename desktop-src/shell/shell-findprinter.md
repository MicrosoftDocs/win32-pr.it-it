---
description: 'Metodo Shell.FindPrinter : visualizza la finestra di dialogo Trova stampante.'
ms.assetid: 61C700CF-623B-4c99-A211-AC26A1E4AE85
title: Metodo Shell.FindPrinter (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindPrinter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 17d04b60de2b52ca3d2f17fbdccf7de93ac095b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104309"
---
# <a name="shellfindprinter-method"></a><span data-ttu-id="da362-103">Metodo Shell.FindPrinter</span><span class="sxs-lookup"><span data-stu-id="da362-103">Shell.FindPrinter method</span></span>

<span data-ttu-id="da362-104">Consente di visualizzare **la finestra di dialogo** Trova stampante .</span><span class="sxs-lookup"><span data-stu-id="da362-104">Displays the **Find Printer** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="da362-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da362-105">Syntax</span></span>


```JScript
iRetVal = Shell.FindPrinter(
  [ sName ],
  [ sLocation ],
  [ sModel ]
)
```


```VB

Shell.FindPrinter( _
  [ ByVal sName As BSTR ], _
  [ ByVal sLocation As BSTR ], _
  [ ByVal sModel As BSTR ] _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="da362-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="da362-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da362-107">*sName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="da362-107">*sName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="da362-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="da362-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="da362-109">Valore **String** contenente il nome della stampante.</span><span class="sxs-lookup"><span data-stu-id="da362-109">A **String** that contains the printer name.</span></span>

</dd> <dt>

<span data-ttu-id="da362-110">*sLocation* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="da362-110">*sLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="da362-111">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="da362-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="da362-112">Valore **String** contenente il percorso della stampante.</span><span class="sxs-lookup"><span data-stu-id="da362-112">A **String** that contains the printer location.</span></span>

</dd> <dt>

<span data-ttu-id="da362-113">*sModel* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="da362-113">*sModel* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="da362-114">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="da362-114">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="da362-115">Valore **String** contenente il modello della stampante.</span><span class="sxs-lookup"><span data-stu-id="da362-115">A **String** that contains the printer model.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da362-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="da362-116">Remarks</span></span>

<span data-ttu-id="da362-117">Se si assegnano stringhe a uno o più parametri facoltativi, queste vengono  visualizzate come valori predefiniti nel controllo di modifica associato quando viene visualizzata la finestra di dialogo Trova stampante .</span><span class="sxs-lookup"><span data-stu-id="da362-117">If you assign strings to one or more of the optional parameters, they are displayed as default values in the associated edit control when the **Find Printer** dialog box is displayed.</span></span> <span data-ttu-id="da362-118">L'utente può accettare o eseguire l'override di questi valori.</span><span class="sxs-lookup"><span data-stu-id="da362-118">The user can either accept or override these values.</span></span> <span data-ttu-id="da362-119">Se a un parametro non viene assegnato alcun valore, la casella di modifica associata è vuota e l'utente deve immettere un valore.</span><span class="sxs-lookup"><span data-stu-id="da362-119">If no value is assigned to a parameter, the associated edit box is empty and the user must enter a value.</span></span>

<span data-ttu-id="da362-120">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="da362-120">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="da362-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="da362-121">Examples</span></span>

<span data-ttu-id="da362-122">Negli esempi seguenti viene illustrato l'utilizzo di **FindPrinter** per visualizzare la **finestra di** dialogo Trova stampante per una determinata applicazione.</span><span class="sxs-lookup"><span data-stu-id="da362-122">The following examples show the use of **FindPrinter** to display the **Find Printer** dialog box for a particular application.</span></span> <span data-ttu-id="da362-123">L'utilizzo viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="da362-123">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="da362-124">Jscript:</span><span class="sxs-lookup"><span data-stu-id="da362-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



<span data-ttu-id="da362-125">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="da362-125">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="da362-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da362-126">Requirements</span></span>



| <span data-ttu-id="da362-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="da362-127">Requirement</span></span> | <span data-ttu-id="da362-128">Valore</span><span class="sxs-lookup"><span data-stu-id="da362-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da362-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da362-129">Minimum supported client</span></span><br/> | <span data-ttu-id="da362-130">Solo app desktop windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="da362-130">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="da362-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da362-131">Minimum supported server</span></span><br/> | <span data-ttu-id="da362-132">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="da362-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="da362-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da362-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="da362-134"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="da362-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="da362-135">Idl</span><span class="sxs-lookup"><span data-stu-id="da362-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="da362-136"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="da362-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="da362-137">DLL</span><span class="sxs-lookup"><span data-stu-id="da362-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da362-138"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="da362-138"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
