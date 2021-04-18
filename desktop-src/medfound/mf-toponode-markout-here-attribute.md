---
description: Specifica se la pipeline applica Mark-out a questo nodo. Mark-out è il punto in cui termina una presentazione. Se i componenti della pipeline generano dati oltre il punto di contrassegno, non viene eseguito il rendering dei dati.
ms.assetid: adf2361a-90c7-4650-a486-5c450a41ab54
title: Attributo MF_TOPONODE_MARKOUT_HERE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c5dc21f39f45aa04860f3374bead54d260f0821
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308443"
---
# <a name="mf_toponode_markout_here-attribute"></a>\_Attributo TOPONODE di \_ contrassegno \_ MF

Specifica se la pipeline applica Mark-out a questo nodo. Mark-out è il punto in cui termina una presentazione. Se i componenti della pipeline generano dati oltre il punto di contrassegno, non viene eseguito il rendering dei dati.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Questo attributo si applica a tutti i tipi di nodo.

Se questo attributo è **true**, la pipeline Media Foundation rimuove gli esempi di output da questo nodo in modo da corrispondere all'ora di fine della presentazione. Il caricatore della topologia imposta questo attributo quando risolve una topologia. Per la maggior parte delle applicazioni non è necessario impostare o recuperare questo attributo.

È consigliabile che questo attributo sia impostato su **true** esattamente per un nodo in ogni ramo della topologia. Un ramo della topologia è definito come il percorso da un nodo di origine a un nodo di output. All'interno di un ramo, \_ gli \_ attributi TOPONODE \_ e [MF TOPONODE Markin \_ \_ \_ here](mf-toponode-markin-here-attribute.md) devono essere impostati nello stesso nodo del branch. Non possono essere impostati su nodi diversi all'interno dello stesso ramo.

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

[**MF \_ TOPONODE \_ Markin \_ qui**](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> </dl>

 

 




