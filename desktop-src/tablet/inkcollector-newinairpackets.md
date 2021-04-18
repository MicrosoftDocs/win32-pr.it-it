---
description: Si verifica quando viene visualizzato un pacchetto in aria.
ms.assetid: e8eacdec-0381-435f-b453-24dca1c507c9
title: Evento InkCollector. NewInAirPackets (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49d942aa474b5cb53d01f5ce83d2bd3ec28d521c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314925"
---
# <a name="inkcollectornewinairpackets-event"></a>Evento InkCollector. NewInAirPackets

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

*Cursore* \[ in\]
</dt> <dd>

Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento **NewInAirPackets** .

</dd> <dt>

*PacketCount* \[ in\]
</dt> <dd>

Numero di pacchetti in aria ricevuti.

</dd> <dt>

*PacketData* \[ in uscita\]
</dt> <dd>

Quando termina, questo metodo contiene una matrice che contiene i dati selezionati per il pacchetto.

Per ulteriori informazioni sulla struttura VARIANT, vedere [utilizzo della libreria com](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Viene creato un pacchetto in aria quando un utente sposta una penna accanto al tablet e il cursore si trova all'interno della finestra dell'oggetto agente di raccolta input penna oppure l'utente sposta il mouse all'interno della finestra associata dell'oggetto agente di raccolta input penna. Gli eventi **NewInAirPackets** vengono generati rapidamente e il gestore eventi deve essere troppo veloce o le prestazioni subiscono problemi.

Questo metodo di evento è definito nelle \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents dispatch (DISPINTERFACES) con ID DISPID \_ ICENewInAirPackets.

L'evento **NewInAirPackets** viene generato anche in modalità selezione o cancellazione, non solo quando si inserisce input penna. A tale scopo, è necessario monitorare la modalità di modifica (che è responsabile dell'impostazione) e tenere presente la modalità prima di interpretare l'evento. Il vantaggio di questo requisito è una maggiore libertà di innovazione sulla piattaforma grazie a una maggiore consapevolezza degli eventi della piattaforma.

Per impostare le proprietà contenute in questa matrice, utilizzare la proprietà [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) dell'oggetto agente di raccolta input penna. La matrice restituita dal parametro *PacketData* contiene i dati per tali proprietà.

> [!Note]  
> Sebbene sia possibile modificare i dati dei pacchetti, queste modifiche non vengono mantenute o utilizzate.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkCollector**](inkcollector-class.md)
</dt> <dt>

[**Proprietà DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)
</dt> <dt>

[**Evento NewPackets**](inkcollector-newpackets.md)
</dt> <dt>

[**Interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




