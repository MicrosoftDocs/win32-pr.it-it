---
description: Specifica l'ora di inizio della presentazione.
ms.assetid: a2a64cac-0dc1-41b0-b59c-a477c7304ba1
title: Attributo MF_TOPONODE_MEDIASTART (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab00727cc328bfd6ba780050160fb21eecbb96f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320668"
---
# <a name="mf_toponode_mediastart-attribute"></a>\_Attributo MF TOPONODE \_ MEDIASTART

Specifica l'ora di inizio della presentazione.

## <a name="data-type"></a>Tipo di dati

**UINT64**

Considera come valore **LONGLONG** .

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a>Commenti

Questo attributo specifica la posizione nell'origine in cui viene avviata la riproduzione, in unità 100-nanosecondi, rispetto all'avvio dell'origine. Se l'attributo non è impostato, la riproduzione inizia da zero (l'inizio del file). Ad esempio, per avviare la riproduzione in corrispondenza del contrassegno di 5 secondi, impostare questo attributo su 50 milioni. Impostare l'attributo sui nodi di origine nella topologia (nodi con tipo uguale a **MF \_ topologia \_ SOURCESTREAM \_ nodo**). Impostare l'attributo prima di chiamare [**IMFMediaSession::**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)SetAttribute.

> [!Note]  
> Se si inserisce manualmente un decodificatore nella topologia, è necessario impostare anche gli attributi [MF \_ TOPONODE \_ Markin \_ qui](mf-toponode-markin-here-attribute.md) e [MF \_ TOPONODE \_ Mark out \_ here](mf-toponode-markout-here-attribute.md) nel nodo decodificatore.

 

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

[**MF \_ TOPONODE \_ MEDIASTOP**](mf-toponode-mediastop-attribute.md)
</dt> </dl>

 

 




