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
# <a name="shellfolderitemextendedproperty-method"></a>Metodo ShellFolderItem. ExtendedProperty

Ottiene il valore di una proprietà dal set di proprietà di un elemento. La proprietà può essere specificata in base al nome o in base all'identificatore di formato (FMTID) e all'identificatore di proprietà (PID) del set di proprietà.

## <a name="syntax"></a>Sintassi


```JScript
retVal = ShellFolderItem.ExtendedProperty(
  sPropName
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sPropName* \[ in\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valore **stringa** che specifica la proprietà. Vedere la sezione Osservazioni per informazioni dettagliate.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **Variant \** _

Quando termina, questo metodo contiene il valore della proprietà, se esiste per l'elemento specificato. Il valore avrà una tipizzazione completa, ad esempio le date vengono restituite come date e non come stringhe.

Questo metodo restituisce una stringa di lunghezza zero se la proprietà è valida ma non esiste per l'elemento specificato o in caso contrario un codice di errore.

## <a name="remarks"></a>Commenti

Esistono due modi per specificare una proprietà. Il primo consiste nell'assegnare il nome noto della proprietà, ad esempio "Author" o "date", a _sPropName *. Tuttavia, ogni proprietà è un membro di un set di proprietà Component Object Model (COM) e può anche essere identificata specificando l'ID di formato (FMTID) e l'ID della proprietà (PID). Un [**fmtid**](../stg/structured-storage-serialized-property-set-format.md) è un GUID che identifica il set di proprietà e un [**PID**](../stg/structured-storage-serialized-property-set-format.md) è un intero che identifica una particolare proprietà all'interno del set di proprietà.

La specifica di una proprietà in base ai relativi valori FMTID/PID è in genere più efficiente rispetto all'uso del nome. Per usare i valori FMTID/PID di una proprietà con **ExtendedProperty**, è necessario combinarli in un SCID. Una SCID è una stringa che contiene i valori FMTID/PID nel formato "*fmtid * * PID*", dove fmtid è il formato stringa del GUID del set di proprietà. Ad esempio, la SCID della proprietà autore del set di proprietà informazioni di riepilogo è "{F29F85E0-4FF9-1068-AB91-08002B27B3D9} 4".

Per un elenco di FMTIDs e PID attualmente supportati dalla shell, vedere [**SHCOLUMNID**](./objects.md).

## <a name="examples"></a>Esempio

In questo esempio di codice viene illustrato come utilizzare **ExtendedProperty** per recuperare le proprietà "title" e "Author" da un documento di Word. Una volta che l'oggetto [**ShellFolderItem**](shellfolderitem-object.md) è associato al file, *fiWordDoc* in questo esempio recuperare il valore della proprietà passandone il nome a **ExtendedProperty**.


```none
...
Doc_Title=fiWordDoc.ExtendedProperty("DocTitle")
Doc_Author=fiWordDoc.ExtendedProperty("Author")
...
```



Un approccio più rapido ed efficiente consiste nel passare una SCID a **ExtendedProperty**.


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



Negli esempi seguenti viene illustrato l'utilizzo corretto di questo metodo per JScript, VBScript e Visual Basic.

JScript


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



VBScript


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



Visual Basic:


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



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



 

 
