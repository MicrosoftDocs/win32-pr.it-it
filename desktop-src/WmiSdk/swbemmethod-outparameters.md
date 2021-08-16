---
description: La proprietà OutParameters dell'oggetto SWbemMethod è un oggetto SWbemObject le cui proprietà definiscono i parametri out e il tipo restituito di questo metodo. Questa proprietà è di sola lettura.
ms.assetid: ae7774f7-8a53-44e4-a110-2aef9ae4037f
ms.tgt_platform: multiple
title: Proprietà SWbemMethod.OutParameters (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod.OutParameters
- ISWbemMethod.OutParameters
- ISWbemMethod.get_OutParameters
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5dec1b2fe18dae65443b45ee6c1d2efcd1d924a72eb2817869c35406ebbc7808
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314414"
---
# <a name="swbemmethodoutparameters-property"></a>Proprietà SWbemMethod.OutParameters

La **proprietà OutParameters** dell'oggetto [**SWbemMethod**](swbemmethod.md) è un [**oggetto SWbemObject**](swbemobject.md) le cui proprietà definiscono i parametri out e il tipo restituito di questo metodo. Questa proprietà è di sola lettura.

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
SWbemMethod.OutParameters As Object
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Per altre informazioni su come usare questa proprietà per ottenere parametri di output dai metodi del provider, vedere Costruzione di oggetti [InParameters e Analisi di oggetti OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md). Si noti che le modifiche apportate a questo oggetto non vengono riflesse nella definizione del metodo sottostante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemMethod<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemMethod<br/>                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemMethod**](swbemmethod.md)
</dt> <dt>

[**SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md)
</dt> <dt>

[**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md)
</dt> <dt>

[**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
</dt> <dt>

[**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)
</dt> </dl>

 

 




