---
description: Specifica se un oggetto sottostante di un nodo della topologia è una Decrypter.
ms.assetid: 211789d8-5e51-485c-b8f1-cd0ae3e39250
title: Attributo MF_TOPONODE_DECRYPTOR (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a8129e82fc2ebc01ee8cf21aabda77dc26970e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318048"
---
# <a name="mf_toponode_decryptor-attribute"></a>\_Attributo di \_ decrittografia MF TOPONODE

Specifica se l'oggetto sottostante di un nodo della topologia è una Decrypter.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Questo attributo si applica a tutti i tipi di nodo.

Se il valore di questo attributo è diverso da zero, l'oggetto sottostante del nodo è un oggetto Decrypter.

Le applicazioni in genere non utilizzano direttamente questo attributo. La sessione multimediale imposta questo attributo quando crea un nodo per una Decrypter, ottenuta dal metodo [**IMFInputTrustAuthority:: Decryptor**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) .

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

 

 




