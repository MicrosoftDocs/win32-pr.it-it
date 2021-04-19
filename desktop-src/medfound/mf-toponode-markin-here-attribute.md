---
description: Specifica se la pipeline applica Mark-in a questo nodo.
ms.assetid: 406145e8-e00e-460d-b282-85face457605
title: Attributo MF_TOPONODE_MARKIN_HERE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efa355cc070a7371ff2e294b3ca3ad558a4749b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308446"
---
# <a name="mf_toponode_markin_here-attribute"></a>\_ \_ Attributo Markin qui MF TOPONODE \_

Specifica se la pipeline applica Mark-in a questo nodo. Mark-in è il punto in cui inizia una presentazione. Se i componenti della pipeline generano dati prima del punto di contrassegno, non viene eseguito il rendering dei dati.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per la maggior parte delle applicazioni non è necessario usare questo attributo. Se necessario, la [sessione multimediale](media-session.md) imposta automaticamente questo attributo.

 

Questo attributo si applica a tutti i tipi di nodo. Se l'attributo è **true**, la pipeline Media Foundation rimuove gli esempi di output da questo nodo in modo che corrispondano all'ora di inizio della presentazione. Il caricatore della topologia imposta questo attributo quando risolve una topologia.

È consigliabile che questo attributo sia impostato su **true** esattamente per un nodo in ogni ramo della topologia. Un ramo della topologia è definito come il percorso da un nodo di origine a un nodo di output. All'interno di un ramo, gli attributi [ \_ TOPONODE \_ \_ ](mf-toponode-markout-here-attribute.md) e MF TOPONODE Markin \_ \_ \_ here devono essere impostati nello stesso nodo del branch. Non possono essere impostati su nodi diversi all'interno dello stesso ramo.

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

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**TOPONODE di MF \_ \_ \_**](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> </dl>

 

 




