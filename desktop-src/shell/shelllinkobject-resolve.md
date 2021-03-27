---
description: Cerca la destinazione di un collegamento della shell, anche se la destinazione è stata spostata o rinominata.
ms.assetid: 60e119be-8e45-4f63-a381-cad048de0765
title: Metodo ShellLinkObject. Resolve (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Resolve
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b1cb0760f1ee19acfa10208711e73919fd084ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980799"
---
# <a name="shelllinkobjectresolve-method"></a><span data-ttu-id="1cd2d-103">Metodo ShellLinkObject. Resolve</span><span class="sxs-lookup"><span data-stu-id="1cd2d-103">ShellLinkObject.Resolve method</span></span>

<span data-ttu-id="1cd2d-104">Cerca la destinazione di un collegamento della shell, anche se la destinazione è stata spostata o rinominata.</span><span class="sxs-lookup"><span data-stu-id="1cd2d-104">Looks for the target of a Shell link, even if the target has been moved or renamed.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cd2d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1cd2d-105">Syntax</span></span>


```JScript
iRetVal = ShellLinkObject.Resolve(
  fFlags
)
```



## <a name="parameters"></a><span data-ttu-id="1cd2d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1cd2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cd2d-107">*fFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1cd2d-107">*fFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cd2d-108">Tipo: **Integer**</span><span class="sxs-lookup"><span data-stu-id="1cd2d-108">Type: **Integer**</span></span>

<span data-ttu-id="1cd2d-109">Flag che specificano l'azione da intraprendere.</span><span class="sxs-lookup"><span data-stu-id="1cd2d-109">Flags that specify the action to be taken.</span></span> <span data-ttu-id="1cd2d-110">Può trattarsi di una combinazione dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="1cd2d-110">This can be a combination of the following values:</span></span>

<dt>



 <span data-ttu-id="1cd2d-111">(1)</span><span class="sxs-lookup"><span data-stu-id="1cd2d-111">(1)</span></span>


</dt> <dd>

<span data-ttu-id="1cd2d-112">Non visualizzare una finestra di dialogo se non è possibile risolvere il collegamento.</span><span class="sxs-lookup"><span data-stu-id="1cd2d-112">Do not display a dialog box if the link cannot be resolved.</span></span> <span data-ttu-id="1cd2d-113">Quando questo flag è impostato, la parola più ordinata di *fFlags* specifica una durata di timeout, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="1cd2d-113">When this flag is set, the high-order word of *fFlags* specifies a time-out duration, in milliseconds.</span></span> <span data-ttu-id="1cd2d-114">Il metodo restituisce se non è possibile risolvere il collegamento entro la durata del timeout.</span><span class="sxs-lookup"><span data-stu-id="1cd2d-114">The method returns if the link cannot be resolved within the time-out duration.</span></span> <span data-ttu-id="1cd2d-115">Se la parola più ordinata è impostata su zero, il valore predefinito per la durata del timeout è 3000 millisecondi (3 secondi).</span><span class="sxs-lookup"><span data-stu-id="1cd2d-115">If the high-order word is set to zero, the time-out duration defaults to 3000 milliseconds (3 seconds).</span></span>

</dd> <dt>



 <span data-ttu-id="1cd2d-116">(4)</span><span class="sxs-lookup"><span data-stu-id="1cd2d-116">(4)</span></span>


</dt> <dd>

<span data-ttu-id="1cd2d-117">Se il collegamento è stato modificato, aggiornarne il percorso e l'elenco degli identificatori.</span><span class="sxs-lookup"><span data-stu-id="1cd2d-117">If the link has changed, update its path and list of identifiers.</span></span>

</dd> <dt>



 <span data-ttu-id="1cd2d-118">(8)</span><span class="sxs-lookup"><span data-stu-id="1cd2d-118">(8)</span></span>


</dt> <dd>

<span data-ttu-id="1cd2d-119">Non aggiornare le informazioni sul collegamento.</span><span class="sxs-lookup"><span data-stu-id="1cd2d-119">Do not update the link information.</span></span>

</dd> <dt>



 <span data-ttu-id="1cd2d-120">(16)</span><span class="sxs-lookup"><span data-stu-id="1cd2d-120">(16)</span></span>


</dt> <dd>

<span data-ttu-id="1cd2d-121">Non eseguire l'euristica di ricerca.</span><span class="sxs-lookup"><span data-stu-id="1cd2d-121">Do not execute the search heuristics.</span></span>

</dd> <dt>



 <span data-ttu-id="1cd2d-122">(32)</span><span class="sxs-lookup"><span data-stu-id="1cd2d-122">(32)</span></span>


</dt> <dd>

<span data-ttu-id="1cd2d-123">Non usare il rilevamento dei collegamenti distribuiti.</span><span class="sxs-lookup"><span data-stu-id="1cd2d-123">Do not use distributed link tracking.</span></span>

</dd> <dt>



 <span data-ttu-id="1cd2d-124">(64)</span><span class="sxs-lookup"><span data-stu-id="1cd2d-124">(64)</span></span>


</dt> <dd>

<span data-ttu-id="1cd2d-125">Disabilitare il rilevamento dei collegamenti distribuiti.</span><span class="sxs-lookup"><span data-stu-id="1cd2d-125">Disable distributed link tracking.</span></span> <span data-ttu-id="1cd2d-126">Per impostazione predefinita, il rilevamento dei collegamenti distribuiti tiene traccia dei supporti rimovibili tra più dispositivi in base al nome del volume.</span><span class="sxs-lookup"><span data-stu-id="1cd2d-126">By default, distributed link tracking tracks removable media across multiple devices based on the volume name.</span></span> <span data-ttu-id="1cd2d-127">USA anche il percorso UNC per tenere traccia dei file system remoti con la lettera di unità modificata.</span><span class="sxs-lookup"><span data-stu-id="1cd2d-127">It also uses the UNC path to track remote file systems whose drive letter has changed.</span></span> <span data-ttu-id="1cd2d-128">L'impostazione di questo flag consente di disabilitare entrambi i tipi di rilevamento.</span><span class="sxs-lookup"><span data-stu-id="1cd2d-128">Setting this flag disables both types of tracking.</span></span>

</dd> <dt>



 <span data-ttu-id="1cd2d-129">(128)</span><span class="sxs-lookup"><span data-stu-id="1cd2d-129">(128)</span></span>


</dt> <dd>

<span data-ttu-id="1cd2d-130">Chiamare il Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="1cd2d-130">Call the Windows Installer.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1cd2d-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="1cd2d-131">Remarks</span></span>

<span data-ttu-id="1cd2d-132">Questo metodo è essenzialmente identico nelle funzionalità da [**risolvere**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve).</span><span class="sxs-lookup"><span data-stu-id="1cd2d-132">This method is essentially identical in functionality to [**Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve).</span></span> <span data-ttu-id="1cd2d-133">Per ulteriori informazioni sulla risoluzione dei collegamenti, vedere la sezione Osservazioni di tale pagina.</span><span class="sxs-lookup"><span data-stu-id="1cd2d-133">For further discussion of link resolution, see the Remarks section of that page.</span></span>

## <a name="examples"></a><span data-ttu-id="1cd2d-134">Esempio</span><span class="sxs-lookup"><span data-stu-id="1cd2d-134">Examples</span></span>

<span data-ttu-id="1cd2d-135">Nell'esempio seguente viene illustrato l'utilizzo corretto di questo metodo per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1cd2d-135">The following example shows the proper usage of this method for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="1cd2d-136">JScript</span><span class="sxs-lookup"><span data-stu-id="1cd2d-136">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellLinkObjectResolveJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var objShellLink;
                
                objShellLink = objFolderItem.GetLink;
                if (objShellLink != null)
                {
                    objShellLink.Resolve(1);
                }
            }
        }
    }
</script>
```



<span data-ttu-id="1cd2d-137">VBScript</span><span class="sxs-lookup"><span data-stu-id="1cd2d-137">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectResolveVB()
        dim objShell
        dim objFolder
        dim ssfPROGRAMS
        
        ssfPROGRAMS = 2
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objFolderItem
                
                set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                    if (not objFolderItem is nothing) then
                        dim objShellLink
                        
                        set objShellLink = objFolderItem.GetLink
                            if (not objShellLink is nothing) then
                                objShellLink.Resolve(1)
                            end if
                        set objShellLink = nothing
                    end if
                set objFolderItem = nothing
            end if
        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="1cd2d-138">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="1cd2d-138">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectResolveVB()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim objShellLink As ShellLinkObject
                    
                    Set objShellLink = objFolderItem.GetLink
                        If (Not objShellLink Is Nothing) Then
                            objShellLink.Resolve (1)
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="1cd2d-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1cd2d-139">Requirements</span></span>



| <span data-ttu-id="1cd2d-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cd2d-140">Requirement</span></span> | <span data-ttu-id="1cd2d-141">Valore</span><span class="sxs-lookup"><span data-stu-id="1cd2d-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cd2d-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1cd2d-142">Minimum supported client</span></span><br/> | <span data-ttu-id="1cd2d-143">Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="1cd2d-143">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1cd2d-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1cd2d-144">Minimum supported server</span></span><br/> | <span data-ttu-id="1cd2d-145">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1cd2d-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1cd2d-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1cd2d-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cd2d-147"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cd2d-147"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="1cd2d-148">IDL</span><span class="sxs-lookup"><span data-stu-id="1cd2d-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1cd2d-149"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1cd2d-149"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="1cd2d-150">DLL</span><span class="sxs-lookup"><span data-stu-id="1cd2d-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cd2d-151"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="1cd2d-151"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
