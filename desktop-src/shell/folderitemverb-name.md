---
description: Contiene il nome del verbo.
ms.assetid: d18fddac-eb51-4031-a572-1bfef2f757a9
title: Proprietà FolderItemVerb.Name (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerb.Name
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5d352f02486f1d7304d4c474aa836401bfef635e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104976999"
---
# <a name="folderitemverbname-property"></a><span data-ttu-id="08159-103">Proprietà FolderItemVerb.Name</span><span class="sxs-lookup"><span data-stu-id="08159-103">FolderItemVerb.Name property</span></span>

<span data-ttu-id="08159-104">Contiene il nome del verbo.</span><span class="sxs-lookup"><span data-stu-id="08159-104">Contains the verb's name.</span></span>

<span data-ttu-id="08159-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="08159-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="08159-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08159-106">Syntax</span></span>


```JScript
strName = FolderItemVerb.Name
```



## <a name="property-value"></a><span data-ttu-id="08159-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="08159-107">Property value</span></span>

<span data-ttu-id="08159-108">Variabile di tipo [**BSTR**](/previous-versions/windows/desktop/automat/bstr) che riceve la proprietà Name.</span><span class="sxs-lookup"><span data-stu-id="08159-108">A variable of type [**BSTR**](/previous-versions/windows/desktop/automat/bstr) that receives the Name property.</span></span>

## <a name="examples"></a><span data-ttu-id="08159-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="08159-109">Examples</span></span>

<span data-ttu-id="08159-110">Nell'esempio seguente viene usato **Name** per recuperare il nome del primo elemento nella raccolta di verbi a cui risponde la cartella del programma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="08159-110">The following example uses **Name** to retrieve the name of the first item in the collection of verbs to which the user's Program folder responds.</span></span> <span data-ttu-id="08159-111">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="08159-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="08159-112">JScript</span><span class="sxs-lookup"><span data-stu-id="08159-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemVerbNameJ()
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
                var szReturn = "";
                
                szReturn = objVerbs.Item(0).Name;
                alert(szReturn);
            }
        }
    }
</script>
```



<span data-ttu-id="08159-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="08159-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemVerbNameVB()
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
                        dim szReturn
                        
                        szReturn = objVerbs.Item(0).Name
                        alert(szReturn)
                    end if
                set objVerbs = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="08159-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="08159-114">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemVerbNameVB()
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
                Dim szReturn As String
                
                szReturn = objVerbs.Item(0).Name
                Debug.Print szReturn
            End If
        Set objVerbs = Nothing
    End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="08159-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08159-115">Requirements</span></span>



| <span data-ttu-id="08159-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="08159-116">Requirement</span></span> | <span data-ttu-id="08159-117">Valore</span><span class="sxs-lookup"><span data-stu-id="08159-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08159-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08159-118">Minimum supported client</span></span><br/> | <span data-ttu-id="08159-119">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="08159-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="08159-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08159-120">Minimum supported server</span></span><br/> | <span data-ttu-id="08159-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="08159-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="08159-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="08159-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="08159-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="08159-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="08159-124">IDL</span><span class="sxs-lookup"><span data-stu-id="08159-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="08159-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="08159-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="08159-126">DLL</span><span class="sxs-lookup"><span data-stu-id="08159-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08159-127"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="08159-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
