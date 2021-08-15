---
description: La proprietà AutoReconnect dell'oggetto SWbemRefresher è un valore booleano che indica se l'aggiornamento si riconnette automaticamente a un provider remoto se la connessione viene interrotta.
ms.assetid: 3be24128-8a35-44b0-befd-8b8937eff1b7
ms.tgt_platform: multiple
title: Proprietà SWbemRefresher.AutoReconnect (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AutoReconnect
- ISWbemRefresher.AutoReconnect
- ISWbemRefresher.get_AutoReconnect
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b1ad11c4362276d5714e54ef3196b246a40de1e26bf8f311f41fb5b5834bab0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312813"
---
# <a name="swbemrefresherautoreconnect-property"></a>Proprietà SWbemRefresher.AutoReconnect

La **proprietà AutoReconnect** dell'oggetto [**SWbemRefresher**](swbemrefresher.md) è un valore booleano che indica se l'aggiornamento si riconnette automaticamente a un provider remoto se la connessione viene interrotta.

Per una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
SWbemRefresher.AutoReconnect As Boolean
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

La modifica di questa proprietà influisce solo sugli oggetti nell'aggiornamento supportati da un provider a prestazioni elevate. Se il provider non è un provider a prestazioni elevate, l'impostazione della proprietà **AutoReconnect** su **TRUE** non ha alcun effetto perché l'oggetto [**SWbemRefresher**](swbemrefresher.md) non si riconnette mai.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefresher<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemRefresher<br/>                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemRefresher**](swbemrefresher.md)
</dt> </dl>

 

 




