---
description: 'Evento InkOverlay.NewInAirPackets: si verifica quando viene visualizzato un pacchetto in aria.'
ms.assetid: 10dc1909-bfbc-4ea0-b77a-e33149205107
title: Evento InkOverlay.NewInAirPackets (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7198fe2d105421654bfba037049e46a592d603bd94409350e97b794882ab4de2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219169"
---
# <a name="inkoverlaynewinairpackets-event"></a>Evento InkOverlay.NewInAirPackets

Si verifica quando viene visualizzato un pacchetto in aria.

## <a name="syntax"></a>Sintassi


```C++
void NewInAirPackets(
  [in]      IInkCursor *Cursor,
  [in]      long       PacketCount,
  [in, out] VARIANT    *PacketData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Cursore* \[ Pollici\]
</dt> <dd>

Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato [**l'evento NewInAirPackets.**](inkcollector-newinairpackets.md)

</dd> <dt>

*PacketCount* \[ Pollici\]
</dt> <dd>

Numero di pacchetti in aria ricevuti.

</dd> <dt>

*PacketData* \[ in, out\]
</dt> <dd>

Matrice che contiene i dati selezionati per il pacchetto.

Per altre informazioni sulla struttura VARIANT, vedere [Uso della libreria COM.](using-the-com-library.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Un pacchetto in aria viene creato quando un utente sposta una penna accanto al tablet e il cursore si trova all'interno della finestra dell'oggetto dell'agente di raccolta input penna o quando l'utente sposta un mouse all'interno della finestra associata dell'oggetto dell'agente di raccolta input penna. [**Gli eventi NewInAirPackets**](inkcollector-newinairpackets.md) vengono generati rapidamente e il gestore eventi deve essere veloce o le prestazioni ne risentiranno.

Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID ICENewInAirPackets.

[**L'evento NewInAirPackets**](inkcollector-newinairpackets.md) viene generato anche in modalità di selezione o cancellazione, non solo quando si inserisce l'input penna. A questo scopo, è necessario monitorare la modalità di modifica (che si è responsabili dell'impostazione) e conoscere la modalità prima di interpretare l'evento. Il vantaggio di questo requisito è una maggiore libertà di innovazione sulla piattaforma attraverso una maggiore consapevolezza degli eventi della piattaforma.

Per impostare le proprietà contenute in questa matrice, usare la [**proprietà DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) dell'oggetto agente di raccolta input penna. La matrice restituita *dal parametro PacketData* contiene i dati per tali proprietà.

> [!Note]  
> Sebbene sia possibile modificare i dati del pacchetto, queste modifiche non vengono rese persistenti o utilizzate.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[**Proprietà DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)
</dt> <dt>

[**Evento NewPackets**](inkcollector-newpackets.md)
</dt> <dt>

[**Interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




