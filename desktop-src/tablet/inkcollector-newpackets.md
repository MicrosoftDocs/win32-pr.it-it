---
description: Si verifica quando l'agente di raccolta input penna riceve un pacchetto.
ms.assetid: 2682e7ba-dabd-497e-aea4-6d3f837f4f10
title: Evento InkCollector. NewPackets (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b03e1a561a61c9b291bca8e59f990dc12b4e2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342811"
---
# <a name="inkcollectornewpackets-event"></a>Evento InkCollector. NewPackets

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

*Cursore* \[ in\]
</dt> <dd>

Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento [**NewInAirPackets**](inkcollector-newinairpackets.md) .

</dd> <dt>

*Tratto* \[ in\]
</dt> <dd>

Specifica l'oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .

</dd> <dt>

*PacketCount* \[ in\]
</dt> <dd>

Numero di pacchetti ricevuti per un oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .

</dd> <dt>

*PacketData* \[ in uscita\]
</dt> <dd>

Quando termina, questo metodo contiene una matrice che contiene i dati selezionati per il pacchetto.

Per ulteriori informazioni sulla struttura VARIANT, vedere [utilizzo della libreria com](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

I pacchetti vengono ricevuti durante la raccolta di un tratto. Gli eventi di pacchetti si verificano rapidamente e un gestore dell'evento **NewPackets** deve avere una velocità elevata o prestazioni ridotte.

Il metodo dell'evento TThis è definito nelle \_ \_ interfacce di solo invio IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (DISPINTERFACES) con ID DISPID \_ ICENewPackets.

Questo evento deve essere usato con cautela perché potrebbe avere un effetto negativo sulle prestazioni dell'input penna se nei gestori eventi viene eseguita una quantità eccessiva di codice.

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

[**Evento NewInAirPackets**](inkcollector-newinairpackets.md)
</dt> <dt>

[**Interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interfaccia IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




