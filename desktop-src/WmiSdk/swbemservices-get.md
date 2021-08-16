---
description: Recupera un oggetto, che è una definizione di classe o un'istanza, in base al percorso dell'oggetto.
ms.assetid: 3071aeb2-adab-47aa-a10c-9796766bb630
ms.tgt_platform: multiple
title: Metodo SWbemServices.Get (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.Get
- ISWbemServices.Get
- ISWbemServices.Get
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d448d92cddf24e98f05cf023116e7087ad8cc3dcd310b7ccd3657571ee7650ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312660"
---
# <a name="swbemservicesget-method"></a>Metodo SWbemServices.Get

Il **metodo Get** dell'oggetto [**SWbemServices**](swbemservices.md) recupera un oggetto, che è una definizione di classe o un'istanza, in base al percorso dell'oggetto. Questo metodo recupera solo gli oggetti dallo spazio dei nomi associato **all'oggetto SWbemServices** corrente.

Il metodo viene chiamato in modalità sincrona. Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objWbemObject = .Get( _
  [ ByVal strObjectPath ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strObjectPath* \[ Opzionale\]
</dt> <dd>

Stringa contenente il percorso dell'oggetto da recuperare. Se questo valore è vuoto, l'oggetto vuoto restituito può diventare una nuova classe. Per altre informazioni, vedere [Descrizione del percorso di un oggetto WMI.](describing-the-location-of-a-wmi-object.md)

</dd> <dt>

*iFlags* \[ Opzionale\]
</dt> <dd>

Numero intero che determina il comportamento della query. Questo parametro può accettare i valori seguenti.

<dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers**** (131072 (0x20000))


</dt> <dd>

Fa in modo che WMI restituirà i dati di modifica della classe con la definizione della classe di base. Per altre informazioni sui qualificatori modificati, vedere [Localizing WMI Class Information](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ Opzionale\]
</dt> <dd>

In genere, questa operazione non è definita. In caso contrario, si tratta di un [**oggetto SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere usate dal provider che sta servo della richiesta. Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, questo metodo restituisce un [**oggetto SWbemObject**](swbemobject.md) che rappresenta l'oggetto richiesto.

## <a name="error-codes"></a>Codici di errore

Al termine del metodo **Get,** **l'oggetto Err** può contenere uno dei codici di errore nell'elenco seguente.

<dl> <dt>

**wbemErrAccessDenied** - 2147749891 (0x80041003)
</dt> <dd>

L'utente corrente non dispone dell'autorizzazione per accedere all'oggetto.

</dd> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidParameter** - 2147749896 (0x80041008)
</dt> <dd>

Un parametro specificato non è valido.

</dd> <dt>

**wbemErrInvalidObjectPath** - 2147749946 (0x8004103A)
</dt> <dd>

Percorso specificato non valido.

</dd> <dt>

**wbemErrNotFound** - 2147749890 (0x80041002)
</dt> <dd>

Impossibile trovare l'oggetto richiesto.

</dd> <dt>

**wbemErrOutOfMemory** - 2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

A differenza [**dei metodi ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) e [**InstancesOf,**](swbemservices-instancesof.md) il metodo Get restituisce sempre un [**oggetto SWbemObject**](swbemobject.md) che rappresenta un'istanza specifica di una risorsa gestita da WMI. Per ottenere un'istanza specifica di una risorsa gestita da WMI usando il metodo Get, è necessario indicare a Get l'istanza di recuperare passando al metodo il percorso dell'oggetto, come illustrato nello script seguente.


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set objSWbemObject = objSWbemServices.Get("Win32_Service.Name='Messenger'")
Wscript.Echo "Name:         " & objSWbemObject.Name        & vbCrLf & _
             "Display Name: " & objSWbemObject.DisplayName & vbCrLf & _
             "Start Mode:   " & objSWbemObject.StartMode   & vbCrLf & _
             "State:        " & objSWbemObject.State
```



È possibile usare questo metodo per ottenere [*oggetti singleton,*](gloss-s.md) ad esempio [**\_ \_ CIMOMIdentification**](--cimomidentification.md), che contiene informazioni sulla versione dell'installazione WMI in esecuzione.

È possibile esaminare il repository con uno strumento di visualizzazione, ad esempio [CIM Studio,](further-information.md) per verificare che vengano visualizzate la nuova classe e la nuova istanza. Per un esempio di rimozione di una classe e di un'istanza dal repository, vedere [**SWbemServices.Delete**](swbemservices-delete.md) o [**SWbemObject.Delete \_**](swbemobject-delete-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemServices<br/>                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemObject**](swbemobject.md)
</dt> </dl>

 

 




