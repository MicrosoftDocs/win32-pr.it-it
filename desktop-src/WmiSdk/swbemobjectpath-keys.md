---
description: La proprietà Keys dell'oggetto SWbemObjectPath è un oggetto SWbemNamedValueSet che contiene le associazioni del valore della chiave. Questa proprietà è di sola lettura.
ms.assetid: 1919403d-6dea-4d41-9bc7-a622a9c9c2c8
ms.tgt_platform: multiple
title: Proprietà SWbemObjectPath. Keys (Adoctint. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Keys
- ISWbemObjectPath.Keys
- ISWbemObjectPath.get_Keys
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 898ae7dac4a9c63273a8ff45a85b5bbb65aaa9d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049757"
---
# <a name="swbemobjectpathkeys-property"></a>Proprietà SWbemObjectPath. Keys

La proprietà **Keys** dell'oggetto [**SWbemObjectPath**](swbemobjectpath.md) è un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che contiene le associazioni del valore della chiave. Questa proprietà è di sola lettura.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
SWbemObjectPath.Keys As Object
```



## <a name="property-value"></a>Valore proprietà

## <a name="error-codes"></a>Codici di errore

Una volta recuperata la proprietà **Keys** , l'oggetto **Err** può contenere il codice di errore riportato di seguito.

<dl> <dt>

**wbemErrNotSupported** -2147749900 (0x8004100C)
</dt> <dd>

La funzionalità o l'operazione non è supportata. Questo errore viene restituito se uno script tenta di scrivere in questa proprietà.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                   |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                             |
| Intestazione<br/>                   | <dl> <dt>Adoctint. h (include wbemdisp. h)</dt> </dl> |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl>                    |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl>                    |
| CLSID<br/>                    | \_SWBEMOBJECTPATH CLSID<br/>                                                                          |
| IID<br/>                      | \_ISWBEMOBJECTPATH IID<br/>                                                                           |



 

 




