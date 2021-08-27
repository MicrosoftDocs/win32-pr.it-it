---
description: Restituisce un valore che rappresenta le funzionalità dell'hardware del tablet.
ms.assetid: 68936dab-3df4-42c4-9945-bcd525c996f3
title: Metodo ITablet::GetHardwareCaps
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetHardwareCaps
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 6faa286a95c27556427ed62dfebd6b16496b22b2e55263661f529709d546656b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031909"
---
# <a name="itabletgethardwarecaps-method"></a>Metodo ITablet::GetHardwareCaps

Restituisce un valore che rappresenta le funzionalità dell'hardware del tablet.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetHardwareCaps(
  [out] DWORD *pdwCaps
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pdwCaps* \[ Cambio\]
</dt> <dd>

Flag di bit che rappresentano le funzionalità dell'hardware del tablet.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Operazione completata.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="remarks"></a>Commenti

Il *parametro pdwCaps* è un set di flag di bit che descrivono le funzionalità hardware del tablet. Nella tabella seguente vengono descritti questi flag.



| Nome flag                         | Valore                 | Descrizione                                                                                                                    |
|-----------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------|
| INTEGRAZIONE DI \_ THWC<br/>       | 0x00000001<br/> | Indica che lo schermo e il digitalizzatore condividono la stessa superficie.<br/>                                                    |
| THWC \_ CSR \_ DEVE \_ TOCCARE<br/> | 0x00000002<br/> | Indica che il cursore deve essere in contatto fisico con il dispositivo per segnalare la posizione.<br/>                           |
| PROSSIMITÀ RIGIDA DI THWC \_ \_<br/>  | 0x00000004<br/> | Indica che il dispositivo può generare eventi quando il cursore entra e esce dall'intervallo di rilevamento fisico.<br/> |
| THWC \_ PHYSID \_ CSRS<br/>     | 0x00000008<br/> | Indica che il dispositivo può identificare in modo univoco il cursore attivo nell'hardware.<br/>                                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITablet**](itablet.md)
</dt> </dl>

 

 




