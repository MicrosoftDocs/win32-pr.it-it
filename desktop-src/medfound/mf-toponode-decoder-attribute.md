---
description: Specifica se un oggetto sottostante di nodi della topologia è un decodificatore.
ms.assetid: b6d576dc-b12f-49bf-b938-db2c629df400
title: Attributo MF_TOPONODE_DECODER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab16d14a91608fb6b21c901e3fb055ce5e4dfbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233619"
---
# <a name="mf_toponode_decoder-attribute"></a>\_Attributo del \_ decodificatore MF TOPONODE

Specifica se l'oggetto sottostante di un nodo di topologia è un decodificatore.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Questo attributo si applica a tutti i tipi di nodo.

Se il valore di questo attributo è diverso da zero, l'oggetto sottostante del nodo è un decodificatore.

Il caricatore della topologia imposta questo attributo quando crea un nodo del decodificatore. Un'applicazione deve impostare questo attributo se l'applicazione aggiunge manualmente un decodificatore alla topologia.

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

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> </dl>

 

 




