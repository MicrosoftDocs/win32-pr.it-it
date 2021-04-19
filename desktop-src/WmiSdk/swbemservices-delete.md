---
description: Elimina la classe o l'istanza specificata nel percorso dell'oggetto. È possibile eliminare solo gli oggetti nello spazio dei nomi corrente.
ms.assetid: 7dabab12-e8ee-4d44-932f-f3239b6f066e
ms.tgt_platform: multiple
title: Metodo SWbemServices. Delete (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.Delete
- ISWbemServices.Delete
- ISWbemServices.Delete
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 690dc595471baa5514d7f1ab84a8f6def16ee5b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485444"
---
# <a name="swbemservicesdelete-method"></a>Metodo SWbemServices. Delete

Il metodo **Delete** dell'oggetto [**SWbemServices**](swbemservices.md) Elimina la classe o l'istanza specificata nel percorso dell'oggetto. È possibile eliminare solo gli oggetti nello spazio dei nomi corrente.

Se un provider dinamico fornisce la classe o l'istanza, non è possibile eliminare questo oggetto a meno che il provider non supporti l'eliminazione di classi o istanze.

Questo metodo viene chiamato in modalità sincrona. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
SWbemServices.Delete( _
  ByVal strObjectPath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strObjectPath* 
</dt> <dd>

Obbligatorio. Stringa che contiene il percorso dell'oggetto che si desidera eliminare. Per ulteriori informazioni, vedere [Descrizione della posizione di un oggetto WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*iFlags* \[ opzionale\]
</dt> <dd>

Riservato. Il valore deve essere zero.

</dd> <dt>

*objWbemNamedValueSet* \[ opzionale\]
</dt> <dd>

In genere, non è definito. In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che servizi la richiesta. Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del metodo **Delete** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

Il contesto corrente non dispone dei privilegi di protezione appropriati per eliminare l'oggetto.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidClass** -2147749904 (0x80041010)
</dt> <dd>

La classe specificata non esiste.

</dd> <dt>

**wbemErrInvalidOperation** -2147749910 (0x80041016)
</dt> <dd>

Impossibile eliminare l'oggetto.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

Oggetto inesistente.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il metodo **SWbemServices. Delete** può essere utilizzato quando alla proprietà della chiave per l'oggetto non viene assegnato un valore, perché questo metodo richiede solo un percorso di oggetto come input. Questo metodo può essere utilizzato in situazioni in cui [**SWbemObject. \_ Delete**](swbemobject-delete-.md) non riesce per mancanza di un valore di chiave. Se viene eseguito il commit dell'oggetto in WMI tramite [**SWbemObject \_ . Put**](swbemobject-put-.md), un oggetto [**SWbemObjectPath**](swbemobjectpath.md) è stato ottenuto tramite la chiamata.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creata una nuova classe, viene aggiunta una proprietà che non è una chiave, viene scritta la nuova classe nel repository e viene visualizzato il percorso del nuovo oggetto classe. Lo script genera quindi un'istanza della nuova classe, scrive l'istanza e visualizza il percorso. Si noti che lo script Elimina la classe e le relative istanze dal repository eliminando la classe. Per ulteriori informazioni sulle classi e le istanze WMI, vedere la pagina relativa alla [modifica delle informazioni relative](manipulating-class-and-instance-information.md) a classi e istanze e [Common Information Model](common-information-model.md).


```VB
wbemCimtypeSint32 = 3
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' Integer property
objClass.Properties_.Add "iProperty", wbemCimtypeSint32  
objClass.Properties_("iProperty").Qualifiers_.Add "key", TRUE 

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.iProperty = 1000

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objSWbemService.Delete("NewClass")
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
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMSERVICES CLSID<br/>                                                         |
| IID<br/>                      | \_ISWBEMSERVICES IID<br/>                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemObjectPath**](swbemobjectpath.md)
</dt> </dl>

 

 




