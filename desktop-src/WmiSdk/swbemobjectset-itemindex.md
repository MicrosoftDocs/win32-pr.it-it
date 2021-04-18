---
description: Restituisce l'oggetto SWbemObject associato all'indice specificato nella raccolta.
ms.assetid: 75830f78-0489-4fae-bf9c-2eee8526232e
ms.tgt_platform: multiple
title: Metodo SWbemObjectSet. ItemIndex (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.ItemIndex
- ISWbemObjectSet.ItemIndex
- ISWbemObjectSet.ItemIndex
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 606a09ebf54f0a31dbe14e10abd52a7e92d815d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316986"
---
# <a name="swbemobjectsetitemindex-method"></a>SWbemObjectSet. ItemIndex, metodo

Il metodo **ItemIndex** restituisce l' [**SWbemObject**](swbemobject.md) associato all'indice specificato nella raccolta. L'indice indica la posizione dell'elemento all'interno dell'insieme. La numerazione della raccolta inizia da zero.

## <a name="syntax"></a>Sintassi


```VB
objWbemObject = .ItemIndex( _
  ByVal lIndex _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lIndex* 
</dt> <dd>

Indice dell'elemento nella raccolta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, l'oggetto [**SWbemObject**](swbemobject.md) richiesto restituisce.

## <a name="error-codes"></a>Codici di errore

Al termine del metodo [**Item**](swbemobjectset-item.md) , l'oggetto **Err** può contenere uno dei codici di errore riportati di seguito.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

È stato specificato un parametro non valido. Questo errore viene restituito se viene specificato un numero di indice negativo.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

L'elemento richiesto non è stato trovato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il metodo **ItemIndex** consente agli script e alle applicazioni dei client WMI scritti in qualsiasi linguaggio un modo uniforme per modificare una raccolta come una matrice. Questo metodo può essere utilizzato con le raccolte [**SWbemObjectSet**](swbemobjectset.md) . Le query, ad esempio [**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md), [**SWbemServices. ReferencesTo**](swbemservices-referencesto.md), [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)o [**SWbemServices.ExecQuery**](swbemservices-execquery.md) restituiscono le raccolte **SWbemObjectSet** . Il metodo **ItemIndex** non funziona con le raccolte che non contengono [**SWbemObjects**](swbemobject.md), ad esempio [**SWbemMethodSet**](swbemmethodset.md), [**SWbemNamedValueSet**](swbemnamedvalueset.md), [**SWbemPrivilegeSet**](swbemprivilegeset.md), [**SWbemPropertySet**](swbempropertyset.md)e [**dell'SWbemQualifierSet**](swbemqualifierset.md).

**ItemIndex** può essere utilizzato anche per ottenere la singola istanza di una classe singleton.

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente viene eseguita una query per una raccolta di tutte le istanze del [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) , quindi vengono visualizzati i nomi dei primi tre processi.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colProcesses = _
    objWMIService.Execquery("Select * from Win32_Process")
Wscript.Echo  colProcesses.ItemIndex(0).Name
Wscript.Echo  colProcesses.ItemIndex(1).Name
Wscript.Echo  colProcesses.ItemIndex(2).Name
```



Per ogni installazione del sistema operativo esiste una sola istanza di [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) . La creazione del percorso [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) per ottenere la singola istanza è imbarazzante, quindi gli script enumerano normalmente **Win32 \_ OperatingSystem** anche se è disponibile una sola istanza. Nell'esempio di codice VBScript riportato di seguito viene illustrato come utilizzare il metodo **ItemIndex** per ottenere **un \_ OperatingSystem Win32** senza utilizzare un ciclo **for each** .


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery _
    ("Select * from Win32_OperatingSystem")

Wscript.Echo "Caption: " & colOperatingSystems.ItemIndex(0).Caption
```



Nell'esempio di codice VBScript seguente vengono ottenute le istanze associate a [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem), ad esempio [**\_ SystemOperatingSystem Win32**](/windows/desktop/CIMWin32Prov/win32-systemoperatingsystem).


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colOS = _
    objWMIService.Execquery("Select * from Win32_OperatingSystem")
    Wscript.Echo  colOS.ItemIndex(0).Name

set colAssociators = colOS.ItemIndex(0).Associators_
    For Each Associator in colAssociators 
        Wscript.Echo Associator.Path_.RelPath  
    Next
```



Nell'output di esempio di codice riportato di seguito vengono mostrate le istanze associate a [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).

``` syntax
Windows Server 2008 
    |C:\Windows|\Device\Harddisk0\Partition1
Win32_ComputerSystem.Name="Test1"
Win32_AutochkSetting.SettingID="Windows Server 2008 
    |C:\\Windows|\\Device\\Harddisk0\\Partition1"
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECTSET CLSID<br/>                                                        |
| IID<br/>                      | \_ISWBEMOBJECTSET IID<br/>                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemObjectSet**](swbemobjectset.md)
</dt> </dl>

 

