---
description: Crea un enumeratore che restituisce le istanze di una classe specificata in base ai criteri di selezione specificati dall'utente.
ms.assetid: 6465a981-f98e-4ece-a9b6-9da8ae618bc6
ms.tgt_platform: multiple
title: Metodo SWbemServices.InstancesOf (Wbemdisp.h)
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
ms.openlocfilehash: 9c53b3f27b570f2fab76cb2164c4a029ad21cfccfe7bff52f2c5b9d8d55bf9da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118107964"
---
# <a name="swbemservicesinstancesof-method"></a>Metodo SWbemServices.InstancesOf

Il **metodo InstancesOf** dell'oggetto [**SWbemServices**](swbemservices.md) crea un enumeratore che restituisce le istanze di una classe specificata in base ai criteri di selezione specificati dall'utente. Questo metodo implementa una query semplice. Le query più complesse possono richiedere l'uso [**diSWbemServices.ExecQuery**](swbemservices-execquery.md).

Il metodo viene chiamato in modalità semisincrona. Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

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

*iFlags* \[ Opzionale\]
</dt> <dd>

Questo parametro determina la descrizione dettagliata dell'enumerazione della chiamata e se la chiamata restituisce immediatamente . Il valore predefinito per questo parametro è **wbemFlagReturnImmediately**. Questo parametro può accettare i valori seguenti.

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

Valore predefinito per questo parametro. Questo flag fa sì che la chiamata restituirà immediatamente .

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete**** (0 (0x0))


</dt> <dd>

Fa sì che questa chiamata si blocchi fino al completamento della query. Questo flag chiama il metodo in modalità sincrona.

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow**** (1 (0x1))


</dt> <dd>

Impone all'enumerazione di includere solo sottoclassi immediate della classe padre specificata.

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep**** (0 (0x0))


</dt> <dd>

Valore predefinito per questo parametro. Questo valore forza l'enumerazione a includere tutte le classi nella gerarchia.

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

Se ha esito positivo, il metodo restituisce [**un oggetto SWbemObjectSet**](swbemobjectset.md).

## <a name="error-codes"></a>Codici di errore

Al termine del metodo **InstancesOf,** **l'oggetto Err** può contenere uno dei codici di errore nell'elenco seguente.

> [!Note]  
> Un enumeratore restituito con zero elementi non è un errore.

 

<dl> <dt>

**wbemErrAccessDenied** - 2147749891 (0x80041003)
</dt> <dd>

L'utente corrente non dispone dell'autorizzazione per visualizzare le istanze della classe specificata.

</dd> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

Si è verificato un errore non specificato.

</dd> <dt>

**wbemErrInvalidClass** - 2147749904 (0x80041010)
</dt> <dd>

La classe specificata non è valida.

</dd> <dt>

**wbemErrInvalidParameter** - 2147749896 (0x80041008)
</dt> <dd>

Un parametro specificato non è valido.

</dd> <dt>

**wbemErrOutOfMemory** - 2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il **metodo InstancesOf** funziona solo per gli oggetti classe.

Per impostazione predefinita, InstancesOf esegue un recupero approfondito. In altre informazioni, InstancesOf recupera tutte le istanze della risorsa gestita identificata e tutte le istanze di tutte le sottoclassi definite sotto la classe di destinazione. Ad esempio, lo script seguente recupera tutte le risorse modellate da tutte le classi dinamiche definite sotto la classe astratta CIM \_ Service.


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("CIM_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Object Path: " & objSWbemObject.Path_.Path
Next
```



Se si esegue questo script, si otterrà nuovamente informazioni. Tuttavia, queste informazioni non saranno limitate ai servizi installati in un computer. Includerà invece le informazioni di tutte le classi figlio del [**servizio CIM, \_**](/windows/desktop/CIMWin32Prov/cim-service)tra cui [**\_ SystemDriver Win32**](/windows/desktop/CIMWin32Prov/win32-systemdriver) e [**Win32 \_ ApplicationService**](/previous-versions/windows/desktop/legacy/aa394068(v=vs.85)).

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

[**SWbemObjectSet**](swbemobjectset.md)
</dt> </dl>

 

