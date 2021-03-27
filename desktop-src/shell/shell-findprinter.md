---
description: Consente di visualizzare la finestra di dialogo Trova stampante.
ms.assetid: 61C700CF-623B-4c99-A211-AC26A1E4AE85
title: Metodo Shell. FindPrinter (shldisp. h)
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
ms.openlocfilehash: 1286bb7247359ea91d29a53f8f0eaa13b55be5e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980634"
---
# <a name="shellfindprinter-method"></a><span data-ttu-id="159d8-103">Shell. FindPrinter, metodo</span><span class="sxs-lookup"><span data-stu-id="159d8-103">Shell.FindPrinter method</span></span>

<span data-ttu-id="159d8-104">Consente di visualizzare la finestra di dialogo **Trova stampante** .</span><span class="sxs-lookup"><span data-stu-id="159d8-104">Displays the **Find Printer** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="159d8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="159d8-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="159d8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="159d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="159d8-107">*sName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="159d8-107">*sName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="159d8-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="159d8-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="159d8-109">**Stringa** che contiene il nome della stampante.</span><span class="sxs-lookup"><span data-stu-id="159d8-109">A **String** that contains the printer name.</span></span>

</dd> <dt>

<span data-ttu-id="159d8-110">*sLocation* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="159d8-110">*sLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="159d8-111">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="159d8-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="159d8-112">**Stringa** che contiene la posizione della stampante.</span><span class="sxs-lookup"><span data-stu-id="159d8-112">A **String** that contains the printer location.</span></span>

</dd> <dt>

<span data-ttu-id="159d8-113">*sModel* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="159d8-113">*sModel* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="159d8-114">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="159d8-114">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="159d8-115">**Stringa** che contiene il modello di stampante.</span><span class="sxs-lookup"><span data-stu-id="159d8-115">A **String** that contains the printer model.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="159d8-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="159d8-116">Remarks</span></span>

<span data-ttu-id="159d8-117">Se si assegnano stringhe a uno o più parametri facoltativi, questi vengono visualizzati come valori predefiniti nel controllo di modifica associato quando viene visualizzata la finestra di dialogo **Trova stampante** .</span><span class="sxs-lookup"><span data-stu-id="159d8-117">If you assign strings to one or more of the optional parameters, they are displayed as default values in the associated edit control when the **Find Printer** dialog box is displayed.</span></span> <span data-ttu-id="159d8-118">L'utente può accettare o eseguire l'override di questi valori.</span><span class="sxs-lookup"><span data-stu-id="159d8-118">The user can either accept or override these values.</span></span> <span data-ttu-id="159d8-119">Se non viene assegnato alcun valore a un parametro, la casella di modifica associata è vuota e l'utente deve immettere un valore.</span><span class="sxs-lookup"><span data-stu-id="159d8-119">If no value is assigned to a parameter, the associated edit box is empty and the user must enter a value.</span></span>

<span data-ttu-id="159d8-120">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="159d8-120">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="159d8-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="159d8-121">Examples</span></span>

<span data-ttu-id="159d8-122">Negli esempi seguenti viene illustrato l'utilizzo di **FindPrinter** per visualizzare la finestra di dialogo **Trova stampante** per una particolare applicazione.</span><span class="sxs-lookup"><span data-stu-id="159d8-122">The following examples show the use of **FindPrinter** to display the **Find Printer** dialog box for a particular application.</span></span> <span data-ttu-id="159d8-123">L'utilizzo viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="159d8-123">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="159d8-124">JScript</span><span class="sxs-lookup"><span data-stu-id="159d8-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



<span data-ttu-id="159d8-125">VBScript</span><span class="sxs-lookup"><span data-stu-id="159d8-125">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="159d8-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="159d8-126">Requirements</span></span>



| <span data-ttu-id="159d8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="159d8-127">Requirement</span></span> | <span data-ttu-id="159d8-128">Valore</span><span class="sxs-lookup"><span data-stu-id="159d8-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="159d8-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="159d8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="159d8-130">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="159d8-130">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="159d8-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="159d8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="159d8-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="159d8-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="159d8-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="159d8-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="159d8-134"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="159d8-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="159d8-135">IDL</span><span class="sxs-lookup"><span data-stu-id="159d8-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="159d8-136"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="159d8-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="159d8-137">DLL</span><span class="sxs-lookup"><span data-stu-id="159d8-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="159d8-138"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="159d8-138"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
