---
description: Il \_ Metodo CompareTo dell'oggetto SWbemObject Confronta due oggetti SWbemObject. Questo confronto è soggetto a determinati vincoli in base ai valori specificati nel parametro iFlags.
ms.assetid: 38813551-2403-4def-ae57-2b17f72cd180
ms.tgt_platform: multiple
title: Metodo SWbemObject.CompareTo_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.CompareTo_
- ISWbemObject.CompareTo_
- ISWbemObject.CompareTo_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f77bf9db9ee864e136ba695051445e543b466e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755015"
---
# <a name="swbemobjectcompareto_-method"></a>Metodo SWbemObject. CompareTo \_

Il **metodo \_ CompareTo** dell'oggetto [**SWbemObject**](swbemobject.md) Confronta due oggetti **SWbemObject** . Questo confronto è soggetto a determinati vincoli in base ai valori specificati nel parametro *iFlags* .

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
bAreEqual = .CompareTo_( _
  ByVal objwbemObject, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*objwbemObject* \[ in\]
</dt> <dd>

Obbligatorio. Questo parametro è un oggetto [**SWbemObject**](swbemobject.md) . Si tratta dell'oggetto con il quale viene confrontato il primo oggetto. L'oggetto deve essere un'istanza di **SWbemObject** valida.

</dd> <dt>

*iFlags* \[ in, facoltativo\]
</dt> <dd>

Specifica le caratteristiche dell'oggetto da considerare quando si confronta un oggetto con altri oggetti. È possibile usare **wbemComparisonFlagIncludeAll** per considerare tutte le funzionalità (impostazione predefinita) o qualsiasi combinazione dei valori seguenti.

<dt>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>wbemComparisonFlagIncludeAll * * * * (0 (0x0))


</dt> <dd>

Confronta tutte le proprietà, i qualificatori e le versioni.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>wbemComparisonFlagIgnoreObjectSource * * * * (2 (0x2))


</dt> <dd>

Causa l'origine degli oggetti, ovvero il server e lo spazio dei nomi da cui provengono, da ignorare rispetto ad altri oggetti.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>wbemComparisonFlagIgnoreQualifiers * * * * (1 (0x1))


</dt> <dd>

Fa in modo che tutti i qualificatori, incluse la **chiave** e la **dinamica**, vengano ignorati in confronto.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>wbemComparisonFlagIgnoreDefaultValues * * * * (4 (0x4))


</dt> <dd>

Fa in modo che i valori predefiniti delle proprietà vengano ignorati. Questo flag è significativo solo quando si confrontano le classi.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>wbemComparisonFlagIgnoreFlavor * * * * (32 (0x20))


</dt> <dd>

Consente di ignorare le versioni del qualificatore. Questo flag prende in considerazione i valori dei qualificatori, ma ignora le differenze di sapore, ad esempio le regole di propagazione e le restrizioni di sostituzione.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>wbemComparisonFlagIgnoreCase * * * * (16 (0x10))


</dt> <dd>

Confronta i valori stringa senza distinzione tra maiuscole e minuscole. Questo vale sia per le stringhe sia per i valori del qualificatore. I nomi di proprietà e di qualificatori vengono sempre confrontati senza distinzione tra maiuscole e minuscole, indipendentemente dal fatto che questo flag sia specificato.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>wbemComparisonFlagIgnoreClass * * * * (8 (0x8))


</dt> <dd>

Indica al sistema di presumere che gli oggetti da confrontare siano istanze della stessa classe. Di conseguenza, questo flag confronta solo le informazioni correlate all'istanza. Utilizzare questo flag per ottimizzare le prestazioni. Se gli oggetti non appartengono alla stessa classe, i risultati sono indefiniti.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce il valore booleano **true** se gli oggetti corrispondono. Restituisce **false** se gli oggetti non corrispondono.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del metodo **CompareTo \_** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Parametro specificato non valido.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECT CLSID<br/>                                                           |
| IID<br/>                      | \_ISWBEMOBJECT IID<br/>                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> </dl>

 

 




