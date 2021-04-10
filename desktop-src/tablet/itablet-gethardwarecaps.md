---
description: Restituisce un valore che rappresenta le funzionalità dell'hardware del tablet.
ms.assetid: 68936dab-3df4-42c4-9945-bcd525c996f3
title: 'Metodo ITablet:: GetHardwareCaps'
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
ms.openlocfilehash: 5ada3ad58699952bac5458ddd079abaf84f63bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884366"
---
# <a name="itabletgethardwarecaps-method"></a>Metodo ITablet:: GetHardwareCaps

Restituisce un valore che rappresenta le funzionalità dell'hardware del tablet.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetHardwareCaps(
  [out] DWORD *pdwCaps
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pdwCaps* \[ out\]
</dt> <dd>

Flag di bit che rappresentano le funzionalità dell'hardware del tablet.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Esito positivo.<br/>                       |
| <dl> <dt>**E \_ non riescono**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="remarks"></a>Commenti

Il parametro *pdwCaps* è un set di flag di bit che descrivono le funzionalità hardware del tablet. Nella tabella seguente vengono descritti questi flag.



| Nome del flag                         | Valore                 | Descrizione                                                                                                                    |
|-----------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------|
| THWC \_ integrato<br/>       | 0x00000001<br/> | Indica che la visualizzazione e il digitalizzatore condividono la stessa superficie.<br/>                                                    |
| THWC \_ CSR \_ deve \_ toccare<br/> | 0x00000002<br/> | Indica che il cursore deve essere in contatto fisico con il dispositivo per segnalare la posizione.<br/>                           |
| \_prossimità THWC \_<br/>  | 0x00000004<br/> | Indica che il dispositivo può generare eventi quando il cursore entra e lascia l'intervallo di rilevamento fisico.<br/> |
| THWC \_ PHYSID \_ i CSR<br/>     | 0x00000008<br/> | Indica che il dispositivo può identificare in modo univoco il cursore attivo nell'hardware.<br/>                                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITablet**](itablet.md)
</dt> </dl>

 

 




