---
description: Specifica l'ora di arresto della presentazione.
ms.assetid: c1022538-ea9f-41e9-9075-c106e8b16b7b
title: Attributo MF_TOPONODE_MEDIASTOP (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5b763d1d5adabc520900dde6839d1599ddcb3d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320716"
---
# <a name="mf_toponode_mediastop-attribute"></a>\_Attributo MF TOPONODE \_ MEDIASTOP

Specifica l'ora di arresto della presentazione.

## <a name="data-type"></a>Tipo di dati

**UINT64**

Considera come valore **LONGLONG** .

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a>Commenti

Questo attributo specifica la posizione nell'origine in cui la riproduzione viene arrestata, in unità 100-nanosecondi, rispetto all'avvio dell'origine. Se l'attributo non è impostato, la riproduzione viene arrestata alla fine dell'origine. Ad esempio, per arrestare la riproduzione al contrassegno di 5 secondi, impostare questo attributo su 50 milioni. Impostare l'attributo sui nodi di origine nella topologia (nodi con tipo uguale a **MF \_ topologia \_ SOURCESTREAM \_ nodo**). Impostare l'attributo prima di chiamare [**IMFMediaSession::**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)SetAttribute.

> [!Note]  
> Se si inserisce manualmente un decodificatore nella topologia, è necessario impostare anche gli attributi [MF \_ TOPONODE \_ Markin \_ qui](mf-toponode-markin-here-attribute.md) e [MF \_ TOPONODE \_ Mark out \_ here](mf-toponode-markout-here-attribute.md) nel nodo decodificatore.

 

Dopo aver impostato la topologia, l'impostazione di questo attributo non ha alcun effetto.

Questo attributo è un valore con segno, sebbene venga archiviato come **UInt64**. Tuttavia, i valori negativi non sono significativi.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Tempi di presentazione sequenza](sequence-presentation-times.md)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> <dt>

[**MF \_ TOPONODE \_ MEDIASTART**](mf-toponode-mediastart-attribute.md)
</dt> </dl>

 

 




