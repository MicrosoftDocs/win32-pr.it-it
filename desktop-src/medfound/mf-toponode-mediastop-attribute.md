---
description: Specifica l'ora di arresto della presentazione.
ms.assetid: c1022538-ea9f-41e9-9075-c106e8b16b7b
title: MF_TOPONODE_MEDIASTOP attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea2abc172151afe404f3acc6cf8c75d03bd0ac495564cb0f322283998677f83b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663871"
---
# <a name="mf_toponode_mediastop-attribute"></a>Attributo \_ MF TOPONODE \_ MEDIASTOP

Specifica l'ora di arresto della presentazione.

## <a name="data-type"></a>Tipo di dati

**UINT64**

Considerare come **valore LONGLONG.**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Si applica a

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a>Commenti

Questo attributo specifica la posizione nell'origine in cui si interrompe la riproduzione, in unità di 100 nanosecondi, rispetto all'inizio dell'origine. Se l'attributo non è impostato, la riproduzione si interrompe alla fine dell'origine. Ad esempio, per arrestare la riproduzione in corrispondenza del contrassegno di 5 secondi, impostare questo attributo su 50000000. Impostare l'attributo nei nodi di origine nella topologia (nodi con tipo uguale a **MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE**). Impostare l'attributo prima di [**chiamare IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).

> [!Note]  
> Se si inserisce manualmente un decodificatore nella topologia, è necessario impostare anche gli attributi [MF \_ TOPONODE \_ MARKIN \_ HERE](mf-toponode-markin-here-attribute.md) e [MF \_ TOPONODE \_ MARKOUT \_ HERE](mf-toponode-markout-here-attribute.md) nel nodo del decodificatore.

 

Dopo aver impostato la topologia, l'impostazione di questo attributo non ha alcun effetto.

Questo attributo è un valore con segno, anche se viene archiviato come **UINT64.** Tuttavia, i valori negativi non sono significativi.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Tempi di presentazione delle sequenze](sequence-presentation-times.md)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> <dt>

[**MF \_ TOPONODE \_ MEDIASTART**](mf-toponode-mediastart-attribute.md)
</dt> </dl>

 

 




