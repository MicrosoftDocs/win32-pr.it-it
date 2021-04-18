---
description: Esegue una query per il recupero di oggetti.
ms.assetid: 06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f
ms.tgt_platform: multiple
title: Metodo SWbemServices.ExecQuery (wbemdisp. h)
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
ms.openlocfilehash: 2f3a894681bafc71de34ae7722b985494ef80b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313163"
---
# <a name="swbemservicesexecquery-method"></a>Metodo cQuery SWbemServices.Exe

Il metodo **ExecQuery** dell'oggetto [**SWbemServices**](swbemservices.md) esegue una query per recuperare gli oggetti. Questi oggetti sono disponibili tramite la raccolta [**SWbemObjectSet**](swbemobjectset.md) restituita.

Questo metodo viene chiamato in modalità semisincrono. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

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

Obbligatorio. Stringa che contiene il testo della query. Questo parametro non può essere vuoto. Per ulteriori informazioni sulla creazione di stringhe di query WMI, vedere [esecuzione di query con WQL](querying-with-wql.md) e informazioni di riferimento su [WQL](wql-sql-for-wmi.md) .

</dd> <dt>

*strQueryLanguage* \[ opzionale\]
</dt> <dd>

Stringa che contiene il linguaggio di query da utilizzare. Se specificato, questo valore deve essere "WQL".

</dd> <dt>

*iFlags* \[ opzionale\]
</dt> <dd>

Integer che determina il comportamento della query e determina se la chiamata restituisce immediatamente un risultato. Il valore predefinito per questo parametro è **wbemFlagReturnImmediately**. Questo parametro può accettare i valori seguenti.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly * * * * (32 (0x20))


</dt> <dd>

Causa la restituzione di un enumeratore di sola trasmissione. Gli enumeratori di solo avanzamento sono in genere molto più veloci e utilizzano meno memoria rispetto agli enumeratori convenzionali, ma non consentono chiamate a [**SWbemObject \_ . Clone**](swbemobject-clone-.md).

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional * * * * (0 (0x0))


</dt> <dd>

Causa la conservazione dei puntatori agli oggetti dell'enumerazione da parte di WMI finché il client non rilascia l'enumeratore.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately * * * * (16 (0x10))


</dt> <dd>

Causa la restituzione immediata della chiamata.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete * * * * (0 (0x0))


</dt> <dd>

Causa il blocco della chiamata fino al completamento della query. Questo flag chiama il metodo in modalità sincrona.

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>wbemQueryFlagPrototype * * * * (2 (0x2))


</dt> <dd>

Usato per la realizzazione di prototipi. Questo flag interrompe l'esecuzione della query e restituisce un oggetto simile a un oggetto risultato tipico.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers * * * * (131072 (0x20000))


</dt> <dd>

Causa la restituzione dei dati di modifica della classe da parte di WMI con la definizione della classe base. Per ulteriori informazioni, vedere la pagina relativa alla [localizzazione delle informazioni sulle classi WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ opzionale\]
</dt> <dd>

In genere, non è definito. In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta. Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se non si verificano errori, questo metodo restituisce un oggetto [**SWbemObjectSet**](swbemobjectset.md) . Si tratta di una raccolta di oggetti che contiene il set di risultati della query. Il chiamante può esaminare la raccolta usando l'implementazione delle raccolte per il linguaggio di programmazione in uso. Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md).

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del metodo **ExecQuery** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore elencati di seguito.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

L'utente corrente non dispone dell'autorizzazione per visualizzare il set di risultati.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

È stato specificato un parametro non valido.

</dd> <dt>

**wbemErrInvalidQuery** -2147749911 (0x80041017)
</dt> <dd>

Sintassi di query non valida.

</dd> <dt>

**wbemErrInvalidQueryType** -2147749912 (0x80041018)
</dt> <dd>

Il linguaggio di query richiesto non è supportato.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

**ExecQuery** è una delle chiamate più diffuse per recuperare le informazioni WMI. Una chiamata standard a **ExecQuery** ha un aspetto simile al seguente:


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



Si noti che si crea l'oggetto [**SWbemServices**](swbemservices.md) con un moniker che rappresenta lo spazio dei nomi e la sicurezza appropriati, quindi si effettua la chiamata **ExecQuery** tramite il servizio. Per una descrizione più completa, vedere [creazione di uno script WMI](creating-a-wmi-script.md) ed [enumerazione di WMI](enumerating-wmi.md).

Come il metodo [**InstancesOf**](swbemservices-instancesof.md) , il metodo **ExecQuery** restituisce sempre una raccolta [**SWbemObjectSet**](swbemobjectset.md) . Pertanto, lo script WMI deve enumerare la raccolta restituita da ExecQuery per accedere a ogni istanza di risorsa gestita nella raccolta, come illustrato di seguito:


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
   ("SELECT * FROM Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



Altri metodi [**SWbemServices**](swbemservices.md) che restituiscono [**un SWbemObjectSet**](swbemobjectset.md) includono [**AssociatorsOf**](swbemservices-associatorsof.md), [**ReferencesTo**](swbemservices-referencesto.md)e [**SubclassesOf**](swbemservices-subclassesof.md).

Non si tratta di un errore perché la query restituisca un set di risultati vuoto. Il metodo **ExecQuery** restituisce le proprietà chiave se la proprietà Key è richiesta nell'argomento *strQuery* . Se si verifica un errore durante l'esecuzione di questo metodo e non si utilizza il flag **wbemFlagReturnImmediately** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) non viene impostato fino a quando non si tenta di accedere al set di oggetti restituito. Tuttavia, se si usa il flag **wbemFlagReturnWhenComplete** , l'oggetto Err viene impostato quando viene chiamato il metodo **ExecQuery** .

Esistono limiti al numero di parole chiave **and** e **or** che possono essere utilizzate nelle query WQL. Un numero elevato di parole chiave WQL utilizzate in una query complessa può causare la restituzione del codice di errore di **\_ \_ \_ violazione della quota E di WBEM** come valore **HRESULT** . Il limite di parole chiave WQL dipende dalla complessità della query.

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente vengono individuate tutte le unità disco nel computer locale e vengono visualizzati l'ID del dispositivo e il tipo dell'unità disco.


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
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMSERVICES CLSID<br/>                                                         |
| IID<br/>                      | \_ISWBEMSERVICES IID<br/>                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemServices. Get**](swbemservices-get.md)
</dt> <dt>

[Esecuzione di query con WQL](querying-with-wql.md)
</dt> <dt>

[Creazione di uno script WMI](creating-a-wmi-script.md)
</dt> <dt>

[Enumerazione di WMI](enumerating-wmi.md)
</dt> </dl>

 

