---
description: Imposta l'elenco di ID di gruppo permanente per tutti i profili resi permanente dall'app.
ms.assetid: EF83F295-CD53-45A4-B209-560B4069CA7C
title: Funzione WFDDisplaySinkSetPersistedGroupIDList (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDSetDisplaySinkPersistedGroupIDList
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 423360d7127f331fd1aa2de7f7370daebcc2b417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309444"
---
# <a name="wfddisplaysinksetpersistedgroupidlist-function"></a>WFDDisplaySinkSetPersistedGroupIDList (funzione)

Imposta l'elenco di ID di gruppo permanente per tutti i profili resi permanente dall'app. L'app deve chiamare questo metodo ogni volta che aggiunge o Elimina un profilo dalla relativa archiviazione.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI WFDSetDisplaySinkPersistedGroupIDList(
  _In_ UINT32             cGroupIDList,
  _In_ DOT11_WFD_GROUP_ID *pGroupIDList
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cGroupIDList* \[ in\]
</dt> <dd>

Numero di ID di gruppo a cui punta *pGroupIDList*.

</dd> <dt>

*pGroupIDList* \[ in\]
</dt> <dd>

Puntatore a una matrice di ID di gruppo *cGroupIDList* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

## <a name="remarks"></a>Commenti

Questo metodo deve essere sempre chiamato con l'intero elenco e non con un subset. Quando l'archivio del profilo è vuoto, è possibile chiamare questo metodo con 0 profili.

Un nuovo richiamo per un ID gruppo che non fa parte dell'elenco fornito avrà esito negativo con "errore; Gruppo P2P sconosciuto "(stato 8).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows 10<br/>                                                                      |
| Fine del supporto server<br/>    | Windows Server 2016<br/>                                                             |
| Intestazione<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl>       |
| Libreria<br/>                  | <dl> <dt>Wifidisplay. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



 

 




