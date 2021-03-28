---
description: Aggiunge un file all'elenco degli ultimi elementi usati (MRU).
ms.assetid: 26D2AE5A-FC7E-4c7c-9F10-8D3D7AA236E7
title: Metodo Shell. AddToRecent (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.AddToRecent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c4372cc6cfac25f94e607f14734a9f544cd4fcbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980807"
---
# <a name="shelladdtorecent-method"></a><span data-ttu-id="b3ca2-103">Shell. AddToRecent, metodo</span><span class="sxs-lookup"><span data-stu-id="b3ca2-103">Shell.AddToRecent method</span></span>

<span data-ttu-id="b3ca2-104">Aggiunge un file all'elenco degli ultimi elementi usati (MRU).</span><span class="sxs-lookup"><span data-stu-id="b3ca2-104">Adds a file to the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3ca2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3ca2-105">Syntax</span></span>


```JScript
Shell.AddToRecent(
  varFile,
  [ bstrCategory ]
)
```


```VB

Shell.AddToRecent( _
  ByVal varFile As Variant, _
  [ ByVal bstrCategory As BSTR ] _
)
```





## <a name="parameters"></a><span data-ttu-id="b3ca2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b3ca2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3ca2-107">*varFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3ca2-107">*varFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3ca2-108">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="b3ca2-108">Type: **Variant**</span></span>

<span data-ttu-id="b3ca2-109">**Stringa** che contiene il percorso del file da aggiungere all'elenco dei documenti utilizzati di recente.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-109">A **String** that contains the path of the file to add to the list of recently used documents.</span></span>

<span data-ttu-id="b3ca2-110">**Windows Vista**: impostare questo parametro su **null** per cancellare la cartella documenti recenti.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-110">**Windows Vista**: Set this parameter to **null** to clear the recent documents folder.</span></span>

</dd> <dt>

<span data-ttu-id="b3ca2-111">*bstrCategory* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="b3ca2-111">*bstrCategory* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b3ca2-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="b3ca2-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="b3ca2-113">**Stringa** che contiene il nome della categoria in cui inserire il file.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-113">A **String** that contains the name of the category in which to place the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3ca2-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b3ca2-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b3ca2-115">JScript</span><span class="sxs-lookup"><span data-stu-id="b3ca2-115">JScript</span></span>

<span data-ttu-id="b3ca2-116">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-116">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="b3ca2-117">VB</span><span class="sxs-lookup"><span data-stu-id="b3ca2-117">VB</span></span>

<span data-ttu-id="b3ca2-118">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-118">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="b3ca2-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="b3ca2-119">Examples</span></span>

<span data-ttu-id="b3ca2-120">Negli esempi seguenti viene illustrato l'utilizzo di **AddToRecent** per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-120">The following examples show the use of **AddToRecent** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b3ca2-121">JScript</span><span class="sxs-lookup"><span data-stu-id="b3ca2-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch3AddToRecentJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("system.ini");
            if (objFolderItem != null)
            {
                objShell.AddToRecent(objFolderItem.Path);
            }
        }
    }
</script>
```



<span data-ttu-id="b3ca2-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="b3ca2-122">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch3AddToRecentVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfWINDOWS
            
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder.ParseName("system.ini")
                if (not objFolderItem is nothing) then
                    objShell.AddToRecent (objFolderItem.Path)
                end if
                set objFolderItem = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="b3ca2-123">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b3ca2-123">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch3AddToRecent()
    Dim objShell  As Shell
    Dim objFolder As Folder
    Dim ssfWINDOWS As Long

    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem

        Set objFolderItem = objFolder.ParseName("system.ini")
        If (Not objFolderItem Is Nothing) Then
            objShell.AddToRecent (objFolderItem.Path)
        End If
        Set objFolderItem = Nothing
    End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b3ca2-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3ca2-124">Requirements</span></span>



| <span data-ttu-id="b3ca2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3ca2-125">Requirement</span></span> | <span data-ttu-id="b3ca2-126">Valore</span><span class="sxs-lookup"><span data-stu-id="b3ca2-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3ca2-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3ca2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b3ca2-128">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b3ca2-128">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="b3ca2-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3ca2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b3ca2-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b3ca2-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b3ca2-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3ca2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3ca2-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3ca2-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="b3ca2-133">IDL</span><span class="sxs-lookup"><span data-stu-id="b3ca2-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b3ca2-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b3ca2-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="b3ca2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b3ca2-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3ca2-136"><dt>Shell32.dll (versione 6,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="b3ca2-136"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
