---
description: Il metodo ReOrderCapabilities imposta un nuovo ordine per le funzionalità di formattazione.
ms.assetid: 05785d64-a22f-411f-9fae-318828d30c52
title: 'Metodo ITFormatControl:: ReOrderCapabilities (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d6f7800e4a04dbd70c5b270778cd7eb0ff540b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329448"
---
# <a name="itformatcontrolreordercapabilities-method"></a>Metodo ITFormatControl:: ReOrderCapabilities

\[ Questo metodo non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **ReOrderCapabilities** imposta un nuovo ordine per le funzionalità di formattazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReOrderCapabilities(
  [in] DWORD *pdwIndices,
  [in] BOOL  *pfEnabled,
  [in] BOOL  *pfPublicize,
  [in] DWORD dwNumIndices
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pdwIndices* \[ in\]
</dt> <dd>

Indice del formato riordinato.

</dd> <dt>

*pfEnabled* \[ in\]
</dt> <dd>

Indica se il formato deve essere abilitato o disabilitato.

</dd> <dt>

*pfPublicize* \[ in\]
</dt> <dd>

Indica se il formato deve essere reso disponibile.

</dd> <dt>

*dwNumIndices* \[ in\]
</dt> <dd>

Nuovo numero di indice per il formato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Il metodo [**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md) deve essere chiamato prima di usare questo metodo.

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
</dt> <dt>

[**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md)
</dt> </dl>

 

 




