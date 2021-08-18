---
description: Contiene il tipo di supporto principale per un nodo della topologia. Questo attributo viene impostato quando il caricamento della topologia non riesce perché non è stato trovato il decodificatore corretto.
ms.assetid: eb837fe6-12c9-479c-a0be-63b24093e6fd
title: MF_TOPONODE_ERROR_MAJORTYPE attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e32752f74708272c367e3f15b208ed66fb0d476baab75b8032ed028e1b9e4162
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875151"
---
# <a name="mf_toponode_error_majortype-attribute"></a>Attributo MF \_ TOPONODE \_ ERROR \_ MAJORTYPE

Contiene il tipo di supporto principale per un nodo della topologia. Questo attributo viene impostato quando il caricamento della topologia non riesce perché non è stato trovato il decodificatore corretto.

## <a name="data-type"></a>Tipo di dati

**GUID**

## <a name="remarks"></a>Commenti

Questo attributo si applica a tutti i tipi di nodo.

Il caricatore della topologia potrebbe impostare l'attributo . Le applicazioni leggono in genere questo attributo ma non lo impostano.

Per un elenco dei valori possibili, vedere [Tipi di supporti principali](media-type-guids.md).

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

[**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> </dl>

 

 




