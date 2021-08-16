---
description: Il metodo GetCurrentFormat recupera il formato multimediale del flusso corrente.
ms.assetid: 02d1b3b5-3639-4864-9b72-623bf94acf69
title: Metodo ITFormatControl::GetCurrentFormat (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50d261cd88a9aac4998f15d871a20408aecb367b793b78b7f9fcaeff452273a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140334"
---
# <a name="itformatcontrolgetcurrentformat-method"></a>Metodo ITFormatControl::GetCurrentFormat

\[Questo metodo non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Il **metodo GetCurrentFormat** recupera il formato multimediale del flusso corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCurrentFormat(
  [out] AM_MEDIA_TYPE **ppMediaType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppMediaType* \[ Cambio\]
</dt> <dd>

Puntatore a un **descrittore AM \_ MEDIA \_ TYPE** del formato del terminale. Per altre informazioni su **AM \_ MEDIA \_ TYPE,** vedere la documentazione di DirectX.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.1<br/>                                                         |
| Intestazione<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITFormatControl**](itformatcontrol.md)
</dt> </dl>

 

 




