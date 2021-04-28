---
description: "Evento InkCollector.NewPackets: si verifica quando l'agente di raccolta input penna riceve un pacchetto."
ms.assetid: 2682e7ba-dabd-497e-aea4-6d3f837f4f10
title: Evento InkCollector.NewPackets (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bab9d13dd2f33689700ef4a9aee2ed5059403e8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110119"
---
# <a name="inkcollectornewpackets-event"></a>Evento InkCollector.NewPackets

Si verifica quando l'agente di raccolta input penna riceve un pacchetto.

## <a name="syntax"></a>Sintassi


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Cursore* \[ Pollici\]
</dt> <dd>

Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato [**l'evento NewInAirPackets.**](inkcollector-newinairpackets.md)

</dd> <dt>

*Tratto* \[ Pollici\]
</dt> <dd>

Specifica [**l'oggetto IInkStrokeDisp.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)

</dd> <dt>

*PacketCount* \[ Pollici\]
</dt> <dd>

Numero di pacchetti ricevuti per un [**oggetto IInkStrokeDisp.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)

</dd> <dt>

*PacketData* \[ in, out\]
</dt> <dd>

Quando questo metodo viene restituito, contiene una matrice che contiene i dati selezionati per il pacchetto.

Per altre informazioni sulla struttura VARIANT, vedere [Uso della libreria COM.](using-the-com-library.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

I pacchetti vengono ricevuti durante la raccolta di un tratto. Gli eventi di pacchetto si verificano rapidamente e un gestore eventi **NewPackets** deve essere veloce o le prestazioni ne risentiranno.

Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID ICENewPackets.

Questo evento deve essere usato con attenzione perché potrebbe avere un effetto negativo sulle prestazioni dell'input penna se viene eseguita una quantità troppo grande di codice nei gestori eventi.

Per impostare le proprietà contenute in questa matrice, usare la [**proprietà DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) dell'oggetto agente di raccolta input penna. La matrice restituita *dal parametro PacketData* contiene i dati per tali proprietà.

> [!Note]  
> Anche se è possibile modificare i dati del pacchetto, queste modifiche non vengono rese persistenti o usate.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkCollector**](inkcollector-class.md)
</dt> <dt>

[**Evento NewInAirPackets**](inkcollector-newinairpackets.md)
</dt> <dt>

[**Interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interfaccia IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




