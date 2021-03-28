---
description: Esegue un verbo in FolderItem associato al verbo.
ms.assetid: 92400fe9-e4d1-4bc9-b4ee-d2adaf38154f
title: Metodo FolderItemVerb. DoIt (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerb.DoIt
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0703b9403dfe9ff6600de68aaa710cd5a55c225a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977002"
---
# <a name="folderitemverbdoit-method"></a><span data-ttu-id="c512c-103">FolderItemVerb. DoIt, metodo</span><span class="sxs-lookup"><span data-stu-id="c512c-103">FolderItemVerb.DoIt method</span></span>

<span data-ttu-id="c512c-104">Esegue un verbo in [**FolderItem**](folderitem.md) associato al verbo.</span><span class="sxs-lookup"><span data-stu-id="c512c-104">Executes a verb on the [**FolderItem**](folderitem.md) associated with the verb.</span></span>

## <a name="syntax"></a><span data-ttu-id="c512c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c512c-105">Syntax</span></span>


```JScript
FolderItemVerb.DoIt()
```



## <a name="parameters"></a><span data-ttu-id="c512c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c512c-106">Parameters</span></span>

<span data-ttu-id="c512c-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c512c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c512c-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c512c-108">Return value</span></span>

<span data-ttu-id="c512c-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="c512c-109">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="c512c-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="c512c-110">Examples</span></span>

<span data-ttu-id="c512c-111">Nell'esempio seguente viene usato **doit** per eseguire il primo verbo nella raccolta di verbi a cui risponde la cartella del programma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c512c-111">The following example uses **DoIt** to execute the first verb in the collection of verbs to which the user's Program folder responds.</span></span> <span data-ttu-id="c512c-112">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c512c-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c512c-113">JScript</span><span class="sxs-lookup"><span data-stu-id="c512c-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemVerbDoItJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objVerbs;
            
            objVerbs = objFolder.Self.Verbs();
            if (objVerbs != null)
            {
                objVerbs.Item(0).DoIt();
            }
        }
    }
</script>
```



<span data-ttu-id="c512c-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="c512c-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemVerbDoItVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objVerbs
                
                set objVerbs = objFolder.Self.Verbs
                    if (not objVerbs is nothing) then
                        objVerbs.Item(0).DoIt
                    end if
                set objVerbs = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="c512c-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="c512c-115">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemVerbDoItVB()
    Dim objShell    As Shell
    Dim objFolder2  As Folder2
    Dim ssfPROGRAMS As Long
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder2 Is Nothing) Then
        Dim objVerbs As FolderItemVerbs
        
        Set objVerbs = objFolder2.Self.Verbs
            If (Not objVerbs Is Nothing) Then
                objVerbs.Item(0).DoIt
            End If
        Set objVerbs = Nothing
    End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c512c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c512c-116">Requirements</span></span>



| <span data-ttu-id="c512c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c512c-117">Requirement</span></span> | <span data-ttu-id="c512c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="c512c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c512c-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c512c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c512c-120">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c512c-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c512c-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c512c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c512c-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c512c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c512c-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c512c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c512c-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c512c-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c512c-125">IDL</span><span class="sxs-lookup"><span data-stu-id="c512c-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c512c-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c512c-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c512c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c512c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c512c-128"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="c512c-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




