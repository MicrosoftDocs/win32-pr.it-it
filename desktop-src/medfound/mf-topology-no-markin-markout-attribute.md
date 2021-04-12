---
description: Specifica se la pipeline esegue il trim degli esempi.
ms.assetid: 4ba66d18-3854-4994-9509-967303dc7d98
title: Attributo MF_TOPOLOGY_NO_MARKIN_MARKOUT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03d7b0152798379406887619a3e691cc528a6993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226632"
---
# <a name="mf_topology_no_markin_markout-attribute"></a>\_ \_ Nessun \_ \_ attributo Markin per la topologia MF

Specifica se la pipeline esegue il trim degli esempi.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, la pipeline rimuove gli esempi in base ai tempi di presentazione corretti. Il trimming viene eseguito nei nodi della topologia con gli attributi [**MF \_ TOPONODE \_ Markin \_ qui**](mf-toponode-markin-here-attribute.md) e [**MF \_ TOPONODE \_ Mark out \_ here**](mf-toponode-markout-here-attribute.md) . Se la **\_ topologia \_ MF \_ No Markin \_ Mark** Out attribute è impostata su **true** nella topologia, la pipeline non taglia gli esempi e gli attributi **MF \_ TOPONODE \_ Markin \_ here** e **MF \_ TOPONODE Mark out \_ \_ here** sono ignorati. Se l'attributo non è impostato o ha il valore **false**, la pipeline esegue il trim degli esempi.

Un'applicazione potrebbe impostare la **\_ topologia MF \_ No \_ Markin \_ Mark** Out attribute su **true** se l'applicazione riceve campioni compressi dalla pipeline ed è necessario ottenere tutti i fotogrammi chiave, che altrimenti potrebbero essere eliminati.

Il valore predefinito di questo attributo è **false**.

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

[**MF \_ TOPONODE \_ Markin \_ qui**](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[**TOPONODE di MF \_ \_ \_**](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[Attributi della topologia](topology-attributes.md)
</dt> </dl>

 

 




