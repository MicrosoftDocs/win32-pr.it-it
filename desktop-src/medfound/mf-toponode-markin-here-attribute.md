---
description: Specifica se la pipeline applica il mark-in in questo nodo.
ms.assetid: 406145e8-e00e-460d-b282-85face457605
title: MF_TOPONODE_MARKIN_HERE attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c105dae6792e995e281309d2b693b78a0ec01e67c4412dc6d62056df09ebe9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874878"
---
# <a name="mf_toponode_markin_here-attribute"></a>Attributo MF \_ TOPONODE \_ MARKIN \_ HERE

Specifica se la pipeline applica il mark-in in questo nodo. Il mark-in è il punto in cui inizia una presentazione. Se i componenti della pipeline generano dati prima del punto di inserimento, non viene eseguito il rendering dei dati.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

> [!Note]  
> La maggior parte delle applicazioni non deve usare questo attributo. La [sessione multimediale](media-session.md) imposta automaticamente questo attributo, se necessario.

 

Questo attributo si applica a tutti i tipi di nodo. Se l'attributo è **TRUE,** Media Foundation pipeline taglia gli esempi di output da questo nodo in modo che corrispondano all'ora di inizio della presentazione. Il caricatore della topologia imposta questo attributo quando risolve una topologia.

È consigliabile che esattamente un nodo in ogni ramo della topologia abbia questo attributo impostato su **TRUE.** Un ramo della topologia è definito come percorso da un nodo di origine a un nodo di output. All'interno di un ramo, gli attributi [MF \_ TOPONODE \_ MARKOUT \_ HERE](mf-toponode-markout-here-attribute.md) e MF \_ TOPONODE MARKIN HERE devono essere impostati nello stesso nodo \_ del \_ ramo. Non possono essere impostate su nodi diversi all'interno dello stesso ramo.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**MF \_ TOPONODE \_ MARKOUT \_ QUI**](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> </dl>

 

 




