---
description: Usare il \_ metodo SpawnInstance dell'oggetto SWbemObject per creare una nuova istanza di una classe.
ms.assetid: 4761bdb2-455a-48c4-9e22-bfba6a1036ec
ms.tgt_platform: multiple
title: Metodo SWbemObject.SpawnInstance_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 804c7d2828723ee8da5dae28321faab62a32a0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233804"
---
# <a name="swbemobjectspawninstance_-method"></a>SWbemObject. SpawnInstance, \_ Metodo

Usare il **metodo \_ SpawnInstance** dell'oggetto [**SWbemObject**](swbemobject.md) per creare una nuova istanza di una classe. L'oggetto corrente deve essere una definizione di classe ottenuta da WMI tramite un metodo, ad esempio [**SWbemServices. Get**](swbemservices-get.md) o [**SWbemServices.ExecQuery**](swbemservices-execquery.md). Usare quindi questa definizione di classe per creare nuove istanze. Creare ogni nuova istanza in locale all'interno del processo e quindi chiamare [**SWbemObject. \_ put**](swbemobject-put-.md) per creare effettivamente l'istanza in WMI.

> [!Note]  
> La generazione di un'istanza da un'istanza è supportata, ma l'istanza restituita è vuota.

 

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objNewInstance = .SpawnInstance_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iFlags* \[ in, facoltativo\]
</dt> <dd>

Riservato e deve essere zero se specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, questa chiamata restituisce un oggetto [**SWbemObject**](swbemobject.md) che contiene una nuova istanza della classe.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del metodo **SpawnInstance \_** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.

<dl> <dt>

**wbemErrIncompleteClass** -2147749920 (0x80041020)
</dt> <dd>

L'oggetto corrente non è una definizione di classe valida e non può generare nuove istanze. Il valore è incompleto o non è stato registrato con WMI mediante [**SWbemObject. put \_**](swbemobject-put-.md).

</dd> <dt>

**wbemErrIllegalOperation** -2147749918 (0x8004101E)
</dt> <dd>

Restituito se questo metodo viene utilizzato in un'istanza di anziché in una classe.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

È stato specificato un parametro non valido.

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
</dt> <dt>

[**SWbemObject. Put\_**](swbemobject-put-.md)
</dt> <dt>

[**SWbemServices. Get**](swbemservices-get.md)
</dt> </dl>

 

 




