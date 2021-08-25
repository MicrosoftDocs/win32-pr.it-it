---
description: Il metodo Delete \_ dell'oggetto SWbemObject elimina la classe corrente o l'istanza corrente.
ms.assetid: bf1db667-4bd5-4717-bc0b-5bffe9d0f4fb
ms.tgt_platform: multiple
title: SWbemObject.Delete_ metodo (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Delete_
- ISWbemObject.Delete_
- ISWbemObject.Delete_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: db8df81e56db9967db46b88c0587af9b82a6281e7e732b8647059e8bf4f5457a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857381"
---
# <a name="swbemobjectdelete_-method"></a>Metodo SWbemObject.Delete \_

Il **\_ metodo Delete** dell'oggetto [**SWbemObject**](swbemobject.md) elimina la classe corrente o l'istanza corrente. Se un provider dinamico fornisce la classe o l'istanza, talvolta non è possibile eliminare questo oggetto a meno che il provider non supporti l'eliminazione di classi o istanze. Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
SWbemObject.Delete_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iFlags* \[ in, facoltativo\]
</dt> <dd>

Riservato e deve essere 0 (zero) se specificato.

</dd> <dt>

*objwbemNamedValueSet* \[ in, facoltativo\]
</dt> <dd>

Questo parametro non è in genere definito. In caso contrario, si tratta di un [**oggetto SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere usate dal provider che sta servo della richiesta. Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento **del metodo Delete, \_** l'oggetto **Err** può contenere uno dei codici di errore nell'elenco seguente.

<dl> <dt>

**wbemErrAccessDenied** - 2147749891 (0x80041003)
</dt> <dd>

Il contesto corrente non dispone di diritti di sicurezza adeguati per eliminare l'oggetto.

</dd> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidClass** - 2147749904 (0x80041010)
</dt> <dd>

La classe specificata non esiste.

</dd> <dt>

**wbemErrInvalidOperation** - 2147749910 (0x80041016)
</dt> <dd>

Impossibile eliminare l'oggetto.

</dd> <dt>

**wbemErrNotFound** - 2147749890 (0x80041002)
</dt> <dd>

L'oggetto non esiste.

</dd> <dt>

**wbemErrOutOfMemory** - 2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il **\_ metodo Delete** ha esito negativo se viene creata una nuova istanza di [**SWbemObject,**](swbemobject.md) ma non viene fornito alcun valore per la proprietà key. Windows Strumentazione gestione (WMI) genera automaticamente un valore GUID (Globally Unique Identifier), ma non viene accettato da **SWbemObject.Delete. \_** In questo caso, [**SWbemServices.Delete**](swbemservices-delete.md), che usa il percorso dell'oggetto funziona. Si noti che [**un oggetto SWbemObjectPath**](swbemobjectpath.md) viene restituito dal metodo [**SWbemObject.Put \_**](swbemobject-put-.md) dopo il commit di un oggetto in WMI.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creata una nuova classe . aggiunge una proprietà chiave. scrive la nuova classe nel repository; e visualizza il percorso del nuovo oggetto classe. Lo script genera quindi un'istanza della nuova classe. lo scrive; e visualizza il percorso. Si noti che lo script elimina sia la classe che le relative istanze dal repository eliminando semplicemente la classe .


```VB
On Error Resume Next
wbemCimtypeString = 8             ' String datatype
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString 
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.Add "key", TRUE

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objClass.Delete_()
If Err <> 0 Then
    WScript.Echo Err.Number & "    " & Err.Description 
Else
    WScript.Echo "Delete succeeded"
End If

' Release SwbemServices object
Set objSWbemService = Nothing
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



 

 




