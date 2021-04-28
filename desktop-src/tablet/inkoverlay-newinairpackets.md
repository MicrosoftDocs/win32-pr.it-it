---
description: 'Evento InkOverlay.NewInAirPackets: si verifica quando viene visualizzato un pacchetto in air.'
ms.assetid: 10dc1909-bfbc-4ea0-b77a-e33149205107
title: Evento InkOverlay.NewInAirPackets (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f39e568941b1af0727ad9c8464913325409b4604
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086709"
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

Per altre informazioni sulla struttura VARIANT, vedere [Uso della libreria COM](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Un pacchetto in air viene creato quando un utente sposta una penna vicino al tablet e il cursore si trova all'interno della finestra dell'oggetto dell'agente di raccolta input penna oppure l'utente sposta un mouse all'interno della finestra associata dell'oggetto dell'agente di raccolta input penna. [**Gli eventi NewInAirPackets**](inkcollector-newinairpackets.md) vengono generati rapidamente e il gestore eventi deve essere veloce o le prestazioni ne risentiranno.

Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID ICENewInAirPackets.

[**L'evento NewInAirPackets**](inkcollector-newinairpackets.md) viene generato anche in modalità di selezione o cancellazione, non solo quando si inserisce l'input penna. A questo scopo, è necessario monitorare la modalità di modifica (che si è responsabili dell'impostazione) e conoscere la modalità prima di interpretare l'evento. Il vantaggio di questo requisito è una maggiore libertà di innovare sulla piattaforma attraverso una maggiore consapevolezza degli eventi della piattaforma.

Per impostare le proprietà contenute in questa matrice, usare la [**proprietà DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) dell'oggetto agente di raccolta input penna. La matrice *restituita dal parametro PacketData* contiene i dati per tali proprietà.

> [!Note]  
> Sebbene sia possibile modificare i dati del pacchetto, queste modifiche non vengono rese persistenti o utilizzate.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC \[ Edition\]<br/>                                                       |
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

 

 




