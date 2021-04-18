---
description: La proprietà OutParameters dell'oggetto SWbemMethod è un oggetto SWbemObject le cui proprietà definiscono i parametri out e il tipo restituito di questo metodo. Questa proprietà è di sola lettura.
ms.assetid: ae7774f7-8a53-44e4-a110-2aef9ae4037f
ms.tgt_platform: multiple
title: Proprietà SWbemMethod. OutParameters (wbemdisp. h)
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
ms.openlocfilehash: 2087dd545a37cdc4b82899cb261cfef5fdb1fda6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313680"
---
# <a name="swbemmethodoutparameters-property"></a>SWbemMethod. OutParameters (proprietà)

La proprietà **OutParameters** dell'oggetto [**SWbemMethod**](swbemmethod.md) è un oggetto [**SWbemObject**](swbemobject.md) le cui proprietà definiscono i parametri out e il tipo restituito di questo metodo. Questa proprietà è di sola lettura.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
SWbemMethod.OutParameters As Object
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Per ulteriori informazioni su come utilizzare questa proprietà per ottenere i parametri di output dai metodi del provider, vedere [creazione di oggetti InParameters e analisi di oggetti OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md). Si noti che tutte le modifiche apportate a questo oggetto non vengono riflesse nella definizione del metodo sottostante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMMETHOD CLSID<br/>                                                           |
| IID<br/>                      | \_ISWBEMMETHOD IID<br/>                                                            |



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

 

 




