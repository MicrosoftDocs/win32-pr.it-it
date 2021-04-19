---
description: Il metodo GetCurrentFormat Recupera il formato multimediale del flusso corrente.
ms.assetid: 02d1b3b5-3639-4864-9b72-623bf94acf69
title: 'Metodo ITFormatControl:: GetCurrentFormat (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1b711b539ea9a92af6bd345c5a1f48b212b640b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329460"
---
# <a name="itformatcontrolgetcurrentformat-method"></a>Metodo ITFormatControl:: GetCurrentFormat

\[ Questo metodo non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **GetCurrentFormat** Recupera il formato multimediale del flusso corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCurrentFormat(
  [out] AM_MEDIA_TYPE **ppMediaType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppMediaType* \[ out\]
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

 

 




