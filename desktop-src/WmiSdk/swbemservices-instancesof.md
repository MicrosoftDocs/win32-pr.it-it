---
description: Crea un enumeratore che restituisce le istanze di una classe specificata in base ai criteri di selezione specificati dall'utente.
ms.assetid: 6465a981-f98e-4ece-a9b6-9da8ae618bc6
ms.tgt_platform: multiple
title: Metodo SWbemServices. InstancesOf (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.InstancesOf
- ISWbemServices.InstancesOf
- ISWbemServices.InstancesOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e2386b52160b1e2a08c5a345b67922ed24afc44c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885214"
---
# <a name="swbemservicesinstancesof-method"></a>SWbemServices. InstancesOf, metodo

Il metodo **InstancesOf** dell'oggetto [**SWbemServices**](swbemservices.md) crea un enumeratore che restituisce le istanze di una classe specificata in base ai criteri di selezione specificati dall'utente. Questo metodo implementa una semplice query. Query più complesse possono richiedere l'uso di [**SWbemServices.ExecQuery**](swbemservices-execquery.md).

Il metodo viene chiamato in modalità semisincrono. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objWbemObjectSet = .InstancesOf( _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strClass* 
</dt> <dd>

Obbligatorio. Stringa che contiene il nome della classe per cui si desiderano le istanze. Questo parametro non può essere vuoto.

</dd> <dt>

*iFlags* \[ opzionale\]
</dt> <dd>

Questo parametro determina il modo in cui la chiamata esegue l'enumerazione e se la chiamata restituisce immediatamente un risultato. Il valore predefinito per questo parametro è **wbemFlagReturnImmediately**. Questo parametro può accettare i valori seguenti.

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

Valore predefinito per questo parametro. Questo flag causa la restituzione immediata della chiamata.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete * * * * (0 (0x0))


</dt> <dd>

Causa il blocco della chiamata fino al completamento della query. Questo flag chiama il metodo in modalità sincrona.

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow * * * * (1 (0x1))


</dt> <dd>

Impone all'enumerazione di includere solo le sottoclassi immediate della classe padre specificata.

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep * * * * (0 (0x0))


</dt> <dd>

Valore predefinito per questo parametro. Questo valore impone all'enumerazione di includere tutte le classi nella gerarchia.

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

Se ha esito positivo, il metodo restituisce un [**SWbemObjectSet**](swbemobjectset.md).

## <a name="error-codes"></a>Codici di errore

Al termine del metodo **InstancesOf** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.

> [!Note]  
> Un enumeratore restituito con zero elementi non è un errore.

 

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

L'utente corrente non dispone dell'autorizzazione per visualizzare le istanze della classe specificata.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Si è verificato un errore non specificato.

</dd> <dt>

**wbemErrInvalidClass** -2147749904 (0x80041010)
</dt> <dd>

La classe specificata non è valida.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Parametro specificato non valido.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il metodo **InstancesOf** funziona solo per gli oggetti classe.

Per impostazione predefinita, InstancesOf esegue un recupero approfondito. Ovvero, InstancesOf recupera tutte le istanze della risorsa gestita identificata e tutte le istanze di tutte le sottoclassi definite sotto la classe di destinazione. Lo script seguente, ad esempio, recupera tutte le risorse modellate da tutte le classi dinamiche definite sotto la \_ classe astratta del servizio CIM.


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("CIM_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Object Path: " & objSWbemObject.Path_.Path
Next
```



Se si esegue questo script, le informazioni vengono restituite. Tuttavia, queste informazioni non saranno limitate ai servizi installati in un computer. Ma includerà le informazioni di tutte le classi figlio del [**\_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service), tra cui [**Win32 \_ SystemDriver**](/windows/desktop/CIMWin32Prov/win32-systemdriver) e [**Win32 \_ ApplicationService**](/previous-versions/windows/desktop/legacy/aa394068(v=vs.85)).

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

[**SWbemObjectSet**](swbemobjectset.md)
</dt> </dl>

 

