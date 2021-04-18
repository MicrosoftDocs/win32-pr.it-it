---
title: Attributo SyncState
description: L'attributo SyncState è una rappresentazione di stringa di un valore a 32 bit utilizzato da Windows Media Player durante la sincronizzazione delle playlist con i dispositivi portatili.
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
ms.openlocfilehash: 2a948f6c649d548b375ccb676134177b0273c85c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325576"
---
# <a name="syncstate-attribute"></a>Attributo SyncState

L'attributo **SyncState** è una rappresentazione di stringa di un valore a 32 bit utilizzato da Windows Media Player durante la sincronizzazione delle playlist con i dispositivi portatili.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Altri elementi](other-item-attributes.md)
-   [Elementi foto](photo-item-attributes.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo è costituito da valori a 16 2 bit, ciascuno dei quali specifica lo stato di sincronizzazione di un dispositivo portatile. Il bit più significativo (MSB) di questo valore a 32 bit corrisponde al dispositivo 16. Il bit meno significativo (LSB) corrisponde al dispositivo 1.

Il MSB di ogni valore a 2 bit indica se Windows Media Player sincronizzato il contenuto con il dispositivo corrispondente. Il valore 1 indica che è stato fatto. Il valore 0 indica che non è stato fatto.

Se MSB è 0, LSB specifica il motivo per cui la sincronizzazione non è riuscita. Il valore 1 nell'LSB indica che lo spazio disponibile per il contenuto non è sufficiente. Il valore 0 in LSB indica un altro motivo per cui è stata impedita la sincronizzazione.

Per recuperare lo stato di sincronizzazione di un dispositivo specifico, è necessario eseguire le operazioni seguenti:

1.  Richiamare **\_ lo stato IWMPSyncDevice:: Get** per determinare se un determinato dispositivo è sincronizzato.
2.  Se è sincronizzato, richiamare **IWMPSyncDevice:: Get \_ partnershipIndex** per recuperare l'indice della coppia di bit del dispositivo nell'attributo **SyncState** .
3.  Usando questo indice, mascherare la coppia di bit corrispondente dell'attributo **SyncState** ed esaminare il risultato per determinare lo stato di sincronizzazione della playlist con il dispositivo.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------|
| Versione<br/> | Windows Media Player 10 o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> <dt>

[**Determinazione dello stato di sincronizzazione della playlist**](determining-playlist-synchronization-state.md)
</dt> <dt>

[**IWMPSyncDevice:: Get \_ partnershipIndex**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex)
</dt> <dt>

[**Stato IWMPSyncDevice:: Get \_**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status)
</dt> </dl>

 

 





