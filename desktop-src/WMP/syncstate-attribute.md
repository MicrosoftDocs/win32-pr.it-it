---
title: Attributo SyncState
description: L'attributo SyncState è una rappresentazione di stringa di un valore a 32 bit Windows Media Player quando sincronizza le playlist con dispositivi portatili.
ms.assetid: affc3d1c-7fe6-4811-acfc-57285cb181ca
keywords:
- Attributo SyncState Windows Media Player
topic_type:
- apiref
api_name:
- SyncState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7712a6e3bb0a01f4a713af114f91ebdcb302ef172c77e1cb64b8746f9ae0dcf7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414861"
---
# <a name="syncstate-attribute"></a>Attributo SyncState

**L'attributo SyncState** è una rappresentazione di stringa di un valore a 32 bit che Windows Media Player quando sincronizza le playlist con dispositivi portatili.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Altri elementi](other-item-attributes.md)
-   [Elementi foto](photo-item-attributes.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo è costituito da sedici valori a 2 bit, ognuno dei quali specifica lo stato di sincronizzazione di un dispositivo portatile. Il bit più significativo (MSB) di questo valore a 32 bit corrisponde al dispositivo 16. Il bit meno significativo corrisponde al dispositivo 1.

Il valore MSB di ogni valore a 2 bit indica se Windows Media Player sincronizzato il contenuto con il dispositivo corrispondente. Il valore 1 indica che è stato fatto. Il valore 0 indica che non è stato fatto.

Se msb è 0, l'LSB specifica il motivo per cui la sincronizzazione non è riuscita. Il valore 1 nell'LSB indica che lo spazio disponibile per il contenuto non è sufficiente. Il valore 0 nell'LSB indica un altro motivo per cui la sincronizzazione non è consentita.

Per recuperare lo stato di sincronizzazione di un determinato dispositivo, è necessario eseguire le operazioni seguenti:

1.  Richiamare **lo stato IWMPSyncDevice::get \_** per determinare se un determinato dispositivo è sincronizzato.
2.  Se è sincronizzato, richiamare **IWMPSyncDevice::get \_ partnershipIndex** per recuperare l'indice della coppia di bit del dispositivo **nell'attributo SyncState.**
3.  Usando questo indice, mascherare la coppia di bit corrispondente dell'attributo **SyncState** ed esaminare il risultato per determinare lo stato di sincronizzazione della playlist con il dispositivo.

Per determinare se è possibile modificare il valore di questo attributo, usare il [metodo Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------|
| Versione<br/> | Windows Media Player 10 o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento all'attributo**](attribute-reference.md)
</dt> <dt>

[**Determinazione dello stato di sincronizzazione delle playlist**](determining-playlist-synchronization-state.md)
</dt> <dt>

[**IWMPSyncDevice::get \_ partnershipIndex**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex)
</dt> <dt>

[**Stato IWMPSyncDevice::get \_**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status)
</dt> </dl>

 

 





