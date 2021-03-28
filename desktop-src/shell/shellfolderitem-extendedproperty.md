---
description: Ottiene il valore di una proprietà dal set di proprietà di un elemento. La proprietà può essere specificata in base al nome o in base all'identificatore di formato (FMTID) e all'identificatore di proprietà (PID) del set di proprietà.
ms.assetid: ca787d7b-d95a-45b9-9627-fd505f99f868
title: Metodo ShellFolderItem. ExtendedProperty (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem.ExtendedProperty
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 614e42512b17a0d8a6950ac96914128b8746c685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980439"
---
# <a name="shellfolderitemextendedproperty-method"></a><span data-ttu-id="48e79-104">Metodo ShellFolderItem. ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="48e79-104">ShellFolderItem.ExtendedProperty method</span></span>

<span data-ttu-id="48e79-105">Ottiene il valore di una proprietà dal set di proprietà di un elemento.</span><span class="sxs-lookup"><span data-stu-id="48e79-105">Gets the value of a property from an item's property set.</span></span> <span data-ttu-id="48e79-106">La proprietà può essere specificata in base al nome o in base all'identificatore di formato (FMTID) e all'identificatore di proprietà (PID) del set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="48e79-106">The property can be specified either by name or by the property set's format identifier (FMTID) and property identifier (PID).</span></span>

## <a name="syntax"></a><span data-ttu-id="48e79-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="48e79-107">Syntax</span></span>


```JScript
retVal = ShellFolderItem.ExtendedProperty(
  sPropName
)
```



## <a name="parameters"></a><span data-ttu-id="48e79-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="48e79-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48e79-109">*sPropName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48e79-109">*sPropName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48e79-110">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="48e79-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="48e79-111">Valore **stringa** che specifica la proprietà.</span><span class="sxs-lookup"><span data-stu-id="48e79-111">A **String** value that specifies the property.</span></span> <span data-ttu-id="48e79-112">Vedere la sezione Osservazioni per informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="48e79-112">See the Remarks section for details.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48e79-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="48e79-113">Return value</span></span>

<span data-ttu-id="48e79-114">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="48e79-114">Type: \**Variant\** _</span></span>

<span data-ttu-id="48e79-115">Quando termina, questo metodo contiene il valore della proprietà, se esiste per l'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="48e79-115">When this method returns, contains the value of the property, if it exists for the specified item.</span></span> <span data-ttu-id="48e79-116">Il valore avrà una tipizzazione completa, ad esempio le date vengono restituite come date e non come stringhe.</span><span class="sxs-lookup"><span data-stu-id="48e79-116">The value will have full typing—for example, dates are returned as dates, not strings.</span></span>

<span data-ttu-id="48e79-117">Questo metodo restituisce una stringa di lunghezza zero se la proprietà è valida ma non esiste per l'elemento specificato o in caso contrario un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="48e79-117">This method returns a zero-length string if the property is valid but does not exist for the specified item, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="48e79-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="48e79-118">Remarks</span></span>

<span data-ttu-id="48e79-119">Esistono due modi per specificare una proprietà.</span><span class="sxs-lookup"><span data-stu-id="48e79-119">There are two ways to specify a property.</span></span> <span data-ttu-id="48e79-120">Il primo consiste nell'assegnare il nome noto della proprietà, ad esempio "Author" o "date", a _sPropName \*.</span><span class="sxs-lookup"><span data-stu-id="48e79-120">The first is to assign the property's well-known name, such as "Author" or "Date", to _sPropName\*.</span></span> <span data-ttu-id="48e79-121">Tuttavia, ogni proprietà è un membro di un set di proprietà Component Object Model (COM) e può anche essere identificata specificando l'ID di formato (FMTID) e l'ID della proprietà (PID).</span><span class="sxs-lookup"><span data-stu-id="48e79-121">However, each property is a member of a Component Object Model (COM) property set and can also be identified by specifying its format ID (FMTID) and property ID (PID).</span></span> <span data-ttu-id="48e79-122">Un [**fmtid**](../stg/structured-storage-serialized-property-set-format.md) è un GUID che identifica il set di proprietà e un [**PID**](../stg/structured-storage-serialized-property-set-format.md) è un intero che identifica una particolare proprietà all'interno del set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="48e79-122">An [**FMTID**](../stg/structured-storage-serialized-property-set-format.md) is a GUID that identifies the property set, and a [**PID**](../stg/structured-storage-serialized-property-set-format.md) is an integer that identifies a particular property within the property set.</span></span>

<span data-ttu-id="48e79-123">La specifica di una proprietà in base ai relativi valori FMTID/PID è in genere più efficiente rispetto all'uso del nome.</span><span class="sxs-lookup"><span data-stu-id="48e79-123">Specifying a property by its FMTID/PID values is usually more efficient than using its name.</span></span> <span data-ttu-id="48e79-124">Per usare i valori FMTID/PID di una proprietà con **ExtendedProperty**, è necessario combinarli in un SCID.</span><span class="sxs-lookup"><span data-stu-id="48e79-124">To use a property's FMTID/PID values with **ExtendedProperty**, they must be combined into an SCID.</span></span> <span data-ttu-id="48e79-125">Una SCID è una stringa che contiene i valori FMTID/PID nel formato "*fmtid \* \* PID*", dove fmtid è il formato stringa del GUID del set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="48e79-125">An SCID is a string that contains the FMTID/PID values in the form "*FMTID\*\*PID*", where the FMTID is the string form of the property set's GUID.</span></span> <span data-ttu-id="48e79-126">Ad esempio, la SCID della proprietà autore del set di proprietà informazioni di riepilogo è "{F29F85E0-4FF9-1068-AB91-08002B27B3D9} 4".</span><span class="sxs-lookup"><span data-stu-id="48e79-126">For example, the SCID of the summary information property set's author property is "{F29F85E0-4FF9-1068-AB91-08002B27B3D9} 4".</span></span>

<span data-ttu-id="48e79-127">Per un elenco di FMTIDs e PID attualmente supportati dalla shell, vedere [**SHCOLUMNID**](./objects.md).</span><span class="sxs-lookup"><span data-stu-id="48e79-127">For a list of FMTIDs and PIDs that are currently supported by the Shell, see [**SHCOLUMNID**](./objects.md).</span></span>

## <a name="examples"></a><span data-ttu-id="48e79-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="48e79-128">Examples</span></span>

<span data-ttu-id="48e79-129">In questo esempio di codice viene illustrato come utilizzare **ExtendedProperty** per recuperare le proprietà "title" e "Author" da un documento di Word.</span><span class="sxs-lookup"><span data-stu-id="48e79-129">This sample code illustrates how to use **ExtendedProperty** to retrieve the "Title" and "Author" properties from a Word document.</span></span> <span data-ttu-id="48e79-130">Una volta che l'oggetto [**ShellFolderItem**](shellfolderitem-object.md) è associato al file, *fiWordDoc* in questo esempio recuperare il valore della proprietà passandone il nome a **ExtendedProperty**.</span><span class="sxs-lookup"><span data-stu-id="48e79-130">Once you have the [**ShellFolderItem**](shellfolderitem-object.md) object associated with the file, *fiWordDoc* in this example, retrieve the property's value by passing its name to **ExtendedProperty**.</span></span>


```none
...
Doc_Title=fiWordDoc.ExtendedProperty("DocTitle")
Doc_Author=fiWordDoc.ExtendedProperty("Author")
...
```



<span data-ttu-id="48e79-131">Un approccio più rapido ed efficiente consiste nel passare una SCID a **ExtendedProperty**.</span><span class="sxs-lookup"><span data-stu-id="48e79-131">A faster and more efficient approach is to pass an SCID to **ExtendedProperty**.</span></span>


```none
...
FMTID_SummaryInfo="{F29F85E0-4FF9-1068-AB91-08002B27B3D9}"
PID_TITLE="2"
PID_AUTHOR="4"
SCID_TITLE=FMTID_SummaryInfo+" "+PID_TITLE
SCID_AUTHOR=FMTID_SummaryInfo+" "+PID_AUTHOR
Doc_Title=fiWordDoc.ExtendedProperty(SCID_TITLE)
Doc_Author=fiWordDoc.ExtendedProperty(SCID_AUTHOR)
...
```



<span data-ttu-id="48e79-132">Negli esempi seguenti viene illustrato l'utilizzo corretto di questo metodo per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="48e79-132">The following examples show the proper usage of this method for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="48e79-133">JScript</span><span class="sxs-lookup"><span data-stu-id="48e79-133">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItem2ExtendedPropertyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("NOTEPAD.EXE");
            if (objFolderItem != null)
            {
                var szReturn = "";
                
                szReturn = objFolderItem.ExtendedProperty("infotip");
                alert(szReturn);
            }
        }
    }
</script>
```



<span data-ttu-id="48e79-134">VBScript</span><span class="sxs-lookup"><span data-stu-id="48e79-134">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemExtendedPropertyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    dim szReturn
                    
                    szReturn = objFolderItem.ExtendedProperty("type")
                    alert(szReturn)
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="48e79-135">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="48e79-135">Visual Basic:</span></span>


```VB
Private Sub fnFolderItem2ExtendedPropertyVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem2 As Object
            
            Set objFolderItem2 = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem2 Is Nothing) Then
                    Dim szReturn As String
                    
                    szReturn = objFolderItem2.ExtendedProperty("size")
                    Debug.Print szReturn
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem2 = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="48e79-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48e79-136">Requirements</span></span>



| <span data-ttu-id="48e79-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="48e79-137">Requirement</span></span> | <span data-ttu-id="48e79-138">Valore</span><span class="sxs-lookup"><span data-stu-id="48e79-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48e79-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48e79-139">Minimum supported client</span></span><br/> | <span data-ttu-id="48e79-140">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="48e79-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="48e79-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48e79-141">Minimum supported server</span></span><br/> | <span data-ttu-id="48e79-142">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="48e79-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="48e79-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="48e79-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="48e79-144"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="48e79-144"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="48e79-145">IDL</span><span class="sxs-lookup"><span data-stu-id="48e79-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="48e79-146"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="48e79-146"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="48e79-147">DLL</span><span class="sxs-lookup"><span data-stu-id="48e79-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48e79-148"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="48e79-148"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
