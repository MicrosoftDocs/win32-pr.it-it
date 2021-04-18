---
description: Il metodo ReleaseFormat rilascia la struttura associata al formato.
ms.assetid: 67181773-5a04-4e20-9814-b004d3b549f5
title: 'Metodo ITFormatControl:: ReleaseFormat (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c91b3eb2a84149054d7ff364cf05290946bca975
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329452"
---
# <a name="itformatcontrolreleaseformat-method"></a>Metodo ITFormatControl:: ReleaseFormat

\[ Questo metodo non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **ReleaseFormat** rilascia la struttura associata al formato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReleaseFormat(
  [in] AM_MEDIA_TYPE *pMediaType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaType* \[ in\]
</dt> <dd>

Puntatore a un descrittore del **\_ \_ tipo di supporto am** del formato terminale. Per ulteriori informazioni sul **\_ \_ tipo di supporto am**, vedere la documentazione di DirectX.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,1<br/>                                                         |
| Intestazione<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITFormatControl**](itformatcontrol.md)
</dt> </dl>

 

 




