---
description: Il \_ Metodo CompareTo dell'oggetto SWbemLastError Confronta due oggetti SWbemObject. Questo confronto è soggetto a determinati vincoli in base ai valori specificati nel parametro iFlags.
ms.assetid: 541510e4-ef8d-4436-966f-19c5df422281
ms.tgt_platform: multiple
title: Metodo SWbemLastError.CompareTo_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.CompareTo_
- ISWbemLastError.CompareTo_
- ISWbemLastError.CompareTo_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4c24eb6e57e81c6c44922b2d6643be65198951ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309848"
---
# <a name="swbemlasterrorcompareto_-method"></a>Metodo SWbemLastError. CompareTo \_

Il **metodo \_ CompareTo** dell'oggetto [**SWbemLastError**](swbemlasterror.md) Confronta due oggetti [**SWbemObject**](swbemobject.md) . Questo confronto è soggetto a determinati vincoli in base ai valori specificati nel parametro *iFlags* .

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

Obbligatorio. Oggetto della classe [**SWbemObject**](swbemobject.md) . Questo parametro è l'oggetto con cui viene confrontato il primo oggetto. L'oggetto deve essere un'istanza di **SWbemObject** valida.

</dd> <dt>

*iFlags* \[ in, facoltativo\]
</dt> <dd>

Intero che specifica flag aggiuntivi per l'operazione. Questo parametro specifica le caratteristiche dell'oggetto da considerare quando vengono eseguiti i confronti degli oggetti. È possibile utilizzare **wbemComparisonFlagIncludeAll** per considerare tutte le funzionalità (impostazione predefinita) o qualsiasi combinazione dei valori seguenti.

<dt>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>wbemComparisonFlagIncludeAll * * * * (0 (0x0))


</dt> <dd>

Causa il confronto di tutte le proprietà, i qualificatori e le versioni.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>wbemComparisonFlagIgnoreQualifiers * * * * (1 (0x1))


</dt> <dd>

Fa in modo che tutti i qualificatori, incluse la **chiave** e la **dinamica**, vengano ignorati in confronto.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>wbemComparisonFlagIgnoreObjectSource * * * * (2 (0x2))


</dt> <dd>

Causa l'origine degli oggetti, ovvero il server e lo spazio dei nomi da cui provengono, da ignorare rispetto ad altri oggetti.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>wbemComparisonFlagIgnoreDefaultValues * * * * (4 (0x4))


</dt> <dd>

Fa in modo che i valori predefiniti delle proprietà vengano ignorati. Questo flag è significativo solo quando si confrontano le classi.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>wbemComparisonFlagIgnoreClass * * * * (8 (0x8))


</dt> <dd>

Indica al sistema di presumere che gli oggetti da confrontare siano istanze della stessa classe. Di conseguenza, questo flag confronta solo le informazioni correlate all'istanza. Utilizzare questo flag per ottimizzare le prestazioni. Se gli oggetti non appartengono alla stessa classe, i risultati sono indefiniti.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>wbemComparisonFlagIgnoreCase * * * * (16 (0x10))


</dt> <dd>

Fa in modo che i valori stringa vengano confrontati senza distinzione tra maiuscole e minuscole. Questo vale sia per le stringhe sia per i valori del qualificatore. I nomi di proprietà e di qualificatori vengono sempre confrontati senza distinzione tra maiuscole e minuscole, indipendentemente dal fatto che questo flag sia specificato.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>wbemComparisonFlagIgnoreFlavor * * * * (32 (0x20))


</dt> <dd>

Consente di ignorare le versioni del qualificatore. Impostando questo flag, anche se vengono presi in considerazione i valori del qualificatore, vengono tuttavia ignorate le distinzioni tra le caratteristiche, quali le regole di propagazione e le limitazioni di override.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Il **metodo \_ CompareTo** restituisce il valore booleano **true** se gli oggetti corrispondono; in caso contrario, restituisce **false**.

## <a name="error-codes"></a>Codici di errore

Al termine del metodo **CompareTo \_** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.

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
| CLSID<br/>                    | \_SWBEMLASTERROR CLSID<br/>                                                        |
| IID<br/>                      | \_ISWBEMLASTERROR IID<br/>                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemLastError**](swbemlasterror.md)
</dt> <dt>

[**SWbemObject**](swbemobject.md)
</dt> </dl>

 

 




