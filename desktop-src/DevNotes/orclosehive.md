---
description: Chiude l'hive del registro di sistema offline specificato e libera la memoria allocata per l'hive.
ms.assetid: e30a92dd-8533-406f-ad63-96306f125d78
title: Funzione ORCloseHive (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCloseHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: a7f018e2ccdb98de14f908224ade52d0cdf7819f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331960"
---
# <a name="orclosehive-function"></a>ORCloseHive (funzione)

Chiude l'hive del registro di sistema offline specificato e libera la memoria allocata per l'hive.

## <a name="syntax"></a>Sintassi


```C++
DWORD ORCloseHive(
  _In_ ORHKEY Handle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Gestisci* \[ in\]
</dt> <dd>

Handle per la chiave radice dell'hive del registro di sistema offline da chiudere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h. [](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.

## <a name="remarks"></a>Commenti

La funzione **ORCloseHive** libera tutta la memoria allocata dalle funzioni del registro di sistema offline per conto dell'hive specificato.

Per mantenere le modifiche apportate all'hive, chiamare la funzione [**ORSaveHive**](orsavehive.md) prima di chiamare **ORCloseHive**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|---------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Windows offline Registry Library versione 1,0 o successiva<br/>                      |
| Intestazione<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**OROpenHive**](oropenhive.md)
</dt> <dt>

[**ORSaveHive**](orsavehive.md)
</dt> </dl>

 

 
