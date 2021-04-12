---
description: La proprietà AutoReconnect dell'oggetto SWbemRefresher è un valore booleano che indica se l'aggiornamento viene riconnesso automaticamente a un provider remoto se la connessione è interruppe.
ms.assetid: 3be24128-8a35-44b0-befd-8b8937eff1b7
ms.tgt_platform: multiple
title: Proprietà SWbemRefresher. AutoReconnect (wbemdisp. h)
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
ms.openlocfilehash: 4faa02a4a77409bb8b1813ee433c326d1c45d1bd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351321"
---
# <a name="swbemrefresherautoreconnect-property"></a>Proprietà SWbemRefresher. AutoReconnect

La proprietà **AutoReconnect** dell'oggetto [**SWbemRefresher**](swbemrefresher.md) è un valore booleano che indica se l'aggiornamento viene riconnesso automaticamente a un provider remoto se la connessione è interruppe.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
SWbemRefresher.AutoReconnect As Boolean
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

La modifica di questa proprietà ha effetto solo sugli oggetti nell'aggiornamento supportato da un provider ad alte prestazioni. Se il provider non è un provider a prestazioni elevate, l'impostazione della proprietà **AutoReconnect** su **true** non ha alcun effetto perché l'oggetto [**SWbemRefresher**](swbemrefresher.md) non si riconnette mai.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMREFRESHER CLSID<br/>                                                        |
| IID<br/>                      | \_ISWBEMREFRESHER IID<br/>                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemRefresher**](swbemrefresher.md)
</dt> </dl>

 

 




