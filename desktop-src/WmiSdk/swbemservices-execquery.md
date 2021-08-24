---
description: 'SWbemServices.Exemetodo cQuery: esegue una query per recuperare gli oggetti.'
ms.assetid: 06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f
ms.tgt_platform: multiple
title: SWbemServices.Exemetodo cQuery (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecQuery
- ISWbemServices.ExecQuery
- ISWbemServices.ExecQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9e827b1297a2bdd3bac39a22efa7f80e0d4723ded689e691423c6945a88bb729
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897487"
---
# <a name="swbemservicesexecquery-method"></a>SWbemServices.Exemetodo cQuery

Il **metodo ExecQuery** dell'oggetto [**SWbemServices**](swbemservices.md) esegue una query per recuperare gli oggetti. Questi oggetti sono disponibili tramite la raccolta [**SWbemObjectSet**](swbemobjectset.md) restituita.

Questo metodo viene chiamato in modalità semisincrona. Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objWbemObjectSet = .ExecQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strQuery* 
</dt> <dd>

Obbligatorio. Stringa contenente il testo della query. Questo parametro non può essere vuoto. Per altre informazioni sulla creazione di stringhe di query WMI, vedere [Query con WQL](querying-with-wql.md) e informazioni [di riferimento su WQL.](wql-sql-for-wmi.md)

</dd> <dt>

*strQueryLanguage* \[ Opzionale\]
</dt> <dd>

Stringa contenente il linguaggio di query da utilizzare. Se specificato, questo valore deve essere "WQL".

</dd> <dt>

*iFlags* \[ Opzionale\]
</dt> <dd>

Numero intero che determina il comportamento della query e determina se la chiamata restituisce immediatamente . Il valore predefinito per questo parametro è **wbemFlagReturnImmediately**. Questo parametro può accettare i valori seguenti.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly**** (32 (0x20))


</dt> <dd>

Determina la restituita di un enumeratore forward-only. Gli enumeratori forward-only sono in genere molto più veloci e usano meno memoria rispetto agli enumeratori convenzionali, ma non consentono chiamate a [**SWbemObject.Clone \_**](swbemobject-clone-.md).

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional**** (0 (0x0))


</dt> <dd>

Fa in modo che WMI manteni i puntatori agli oggetti dell'enumerazione fino a quando il client non rilascia l'enumeratore.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately**** (16 (0x10))


</dt> <dd>

Determina la restituzione immediata della chiamata.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete**** (0 (0x0))


</dt> <dd>

Fa sì che questa chiamata si blocchi fino al completamento della query. Questo flag chiama il metodo in modalità sincrona.

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>wbemQueryFlagPrototype**** (2 (0x2))


</dt> <dd>

Usato per la prototipazione. Questo flag impedisce l'esecuzione della query e restituisce un oggetto simile a un tipico oggetto risultato.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers**** (131072 (0x20000))


</dt> <dd>

Fa in modo che WMI restituirà i dati di modifica della classe con la definizione della classe di base. Per altre informazioni, vedere [Localizzazione di informazioni sulle classi WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ Opzionale\]
</dt> <dd>

In genere, questa operazione non è definita. In caso contrario, si tratta di un [**oggetto SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere usate dal provider che sta servo della richiesta. Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se non si verifica alcun errore, questo metodo restituisce un [**oggetto SWbemObjectSet.**](swbemobjectset.md) Si tratta di una raccolta di oggetti che contiene il set di risultati della query. Il chiamante può esaminare la raccolta usando l'implementazione delle raccolte per il linguaggio di programmazione in uso. Per altre informazioni, vedere [Accesso a una raccolta](accessing-a-collection.md).

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del **metodo ExecQuery,** l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore nell'elenco seguente.

<dl> <dt>

**wbemErrAccessDenied** - 2147749891 (0x80041003)
</dt> <dd>

L'utente corrente non dispone dell'autorizzazione per visualizzare il set di risultati.

</dd> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidParameter** - 2147749896 (0x80041008)
</dt> <dd>

È stato specificato un parametro non valido.

</dd> <dt>

**wbemErrInvalidQuery** - 2147749911 (0x80041017)
</dt> <dd>

La sintassi della query non è valida.

</dd> <dt>

**wbemErrInvalidQueryType** - 2147749912 (0x80041018)
</dt> <dd>

Il linguaggio di query richiesto non è supportato.

</dd> <dt>

**wbemErrOutOfMemory** - 2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

**ExecQuery** è una delle chiamate più comunemente usate per recuperare informazioni WMI. Una chiamata standard a **ExecQuery** è simile alla seguente:


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```



Si noti che si crea [**l'oggetto SWbemServices**](swbemservices.md) con un moniker che rappresenta lo spazio dei nomi e la sicurezza appropriati, quindi si effettua la chiamata **ExecQuery** tramite il servizio. Per una discussione più completa, vedere [Creazione di uno script WMI](creating-a-wmi-script.md) ed Enumerazione di [WMI.](enumerating-wmi.md)

Analogamente al [**metodo InstancesOf,**](swbemservices-instancesof.md) il **metodo ExecQuery** restituisce sempre una [**raccolta SWbemObjectSet.**](swbemobjectset.md) Lo script WMI deve quindi enumerare la raccolta restituita da ExecQuery per accedere a ogni istanza di risorsa gestita nella raccolta, come illustrato di seguito:


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
   ("SELECT * FROM Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



Altri [**metodi SWbemServices**](swbemservices.md) che restituiscono [**un oggetto SWbemObjectSet**](swbemobjectset.md) includono [**AssociatorsOf**](swbemservices-associatorsof.md), [**ReferencesTo**](swbemservices-referencesto.md)e [**SubclassesOf**](swbemservices-subclassesof.md).

Non è un errore che la query restituirà un set di risultati vuoto. Il **metodo ExecQuery** restituisce le proprietà chiave indipendentemente dal fatto che la proprietà key sia richiesta o meno nell'argomento *strQuery.* Se si verifica un errore durante l'esecuzione di questo metodo e non si usa il flag **wbemFlagReturnImmediately,** l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) non viene impostato fino a quando non si tenta di accedere al set di oggetti restituito. Tuttavia, se si usa il flag **wbemFlagReturnWhenComplete,** l'oggetto Err viene impostato quando viene chiamato il metodo **ExecQuery.**

Esistono limiti al numero di parole **chiave AND** **e OR** che possono essere usate nelle query WQL. Un numero elevato di parole chiave WQL usate in una query complessa può causare la restituzione del codice di errore **WBEM \_ E \_ QUOTA \_ VIOLATION** da parte di WMI come **valore HRESULT.** Il limite delle parole chiave WQL dipende dalla complessità della query.

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente vengono individuate tutte le unità disco nel computer locale e vengono visualizzati l'ID dispositivo e il tipo di unità disco.


```VB
Set colDisks = GetObject( _
    "Winmgmts:").ExecQuery("Select * from Win32_LogicalDisk")
For Each objDisk in colDisks
 
    Select Case objDisk.DriveType
        Case 1
            Wscript.Echo "No root directory. Drive type could not be determined."
        Case 2
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Removable drive" 
        Case 3
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Local hard disk" 
        Case 4
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Network disk" 
        Case 5
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Compact disk" 
        Case 6
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = RAM disk" 
        Case Else
            Wscript.Echo "Drive type could not be determined."
    End Select
Next
```



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

[**SWbemServices.Get**](swbemservices-get.md)
</dt> <dt>

[Esecuzione di query con WQL](querying-with-wql.md)
</dt> <dt>

[Creazione di uno script WMI](creating-a-wmi-script.md)
</dt> <dt>

[Enumerazione di WMI](enumerating-wmi.md)
</dt> </dl>

 

