---
description: Chiamato in risposta alla barricata della visualizzazione Web che viene rilasciata dall'utente.
ms.assetid: 170893b6-c947-45b1-b717-a93a0b083bda
title: Metodo Cartella2. DismissedWebViewBarricade (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.DismissedWebViewBarricade
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: cdedc7292b0dd52ca903b944993e32df1ec2c3b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131634"
---
# <a name="folder2dismissedwebviewbarricade-method"></a><span data-ttu-id="609bd-103">Cartella2. DismissedWebViewBarricade, metodo</span><span class="sxs-lookup"><span data-stu-id="609bd-103">Folder2.DismissedWebViewBarricade method</span></span>

<span data-ttu-id="609bd-104">Chiamato in risposta alla barricata della visualizzazione Web che viene rilasciata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="609bd-104">Called in response to the web view barricade being dismissed by the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="609bd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="609bd-105">Syntax</span></span>


```JScript
Folder2.DismissedWebViewBarricade()
```



## <a name="parameters"></a><span data-ttu-id="609bd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="609bd-106">Parameters</span></span>

<span data-ttu-id="609bd-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="609bd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="609bd-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="609bd-108">Return value</span></span>

<span data-ttu-id="609bd-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="609bd-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="609bd-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="609bd-110">Remarks</span></span>

<span data-ttu-id="609bd-111">Un'applicazione chiama questo metodo dopo che l'utente chiude la barricata di visualizzazione Web.</span><span class="sxs-lookup"><span data-stu-id="609bd-111">An application calls this method after the user dismisses the web view barricade.</span></span>

## <a name="examples"></a><span data-ttu-id="609bd-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="609bd-112">Examples</span></span>

<span data-ttu-id="609bd-113">Nell'esempio seguente viene usato **DismissedWebViewBarricade** per specificare che la barricata della vista web per la \\ cartella C: Windows è stata rilasciata.</span><span class="sxs-lookup"><span data-stu-id="609bd-113">The following example uses **DismissedWebViewBarricade** to specify that the web view barricade for the C:\\Windows folder has been dismissed.</span></span> <span data-ttu-id="609bd-114">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="609bd-114">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="609bd-115">JScript</span><span class="sxs-lookup"><span data-stu-id="609bd-115">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolder2ObjectDismissedWebViewBarricadeJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder2 != null)
        {
            objFolder2.DismissedWebViewBarricade();
        }
    }
</script>
```



<span data-ttu-id="609bd-116">VBScript</span><span class="sxs-lookup"><span data-stu-id="609bd-116">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolder2ObjectDismissedWebViewBarricadeVB()
        dim objShell
        dim objFolder2

        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder2 is nothing) then
            objFolder2.DismissedWebViewBarricade()
        end if

        set objFolder2 = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="609bd-117">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="609bd-117">Visual Basic:</span></span>


```VB
Private Sub btnDismissedWebViewBarricade_Click()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2

    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder2 Is Nothing) Then
        objFolder2.DismissedWebViewBarricade
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="609bd-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="609bd-118">Requirements</span></span>



| <span data-ttu-id="609bd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="609bd-119">Requirement</span></span> | <span data-ttu-id="609bd-120">Valore</span><span class="sxs-lookup"><span data-stu-id="609bd-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="609bd-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="609bd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="609bd-122">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="609bd-122">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="609bd-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="609bd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="609bd-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="609bd-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="609bd-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="609bd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="609bd-126"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="609bd-126"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="609bd-127">IDL</span><span class="sxs-lookup"><span data-stu-id="609bd-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="609bd-128"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="609bd-128"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="609bd-129">DLL</span><span class="sxs-lookup"><span data-stu-id="609bd-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="609bd-130"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="609bd-130"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="609bd-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="609bd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="609bd-132">**Cartella2**</span><span class="sxs-lookup"><span data-stu-id="609bd-132">**Folder2**</span></span>](folder2-object.md)
</dt> <dt>

[<span data-ttu-id="609bd-133">**Cartella**</span><span class="sxs-lookup"><span data-stu-id="609bd-133">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




