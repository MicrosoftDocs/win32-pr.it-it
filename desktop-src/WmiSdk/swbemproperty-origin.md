---
description: La proprietà Origin dell'oggetto SWbemProperty Recupera il nome della classe WMI in cui è stata introdotta la proprietà. Per le classi con gerarchie di ereditarietà completa, è spesso opportuno individuare le proprietà dichiarate nelle classi.
ms.assetid: 25bc0303-43b8-42da-a194-82213c1009d9
ms.tgt_platform: multiple
title: Proprietà SWbemProperty. Origin (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.Origin
- ISWbemProperty.Origin
- ISWbemProperty.get_Origin
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f0aef6c1041e14d65ee3cbacaa40255421a1b064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231821"
---
# <a name="swbempropertyorigin-property"></a>Proprietà SWbemProperty. Origin

La proprietà **Origin** dell'oggetto [**SWbemProperty**](swbemproperty.md) Recupera il nome della classe WMI in cui è stata introdotta la proprietà. Per le classi con gerarchie di ereditarietà completa, è spesso opportuno individuare le proprietà dichiarate nelle classi.

Se la proprietà è locale (vedere [**oggetto SWbemQualifier. setlocale**](swbemqualifier-islocal.md)), questo valore corrisponde alla classe proprietaria. Questa proprietà è di sola lettura.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
SWbemProperty.Origin As String
```



## <a name="property-value"></a>Valore proprietà

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMPROPERTY CLSID<br/>                                                         |
| IID<br/>                      | \_ISWBEMPROPERTY IID<br/>                                                          |



 

 




