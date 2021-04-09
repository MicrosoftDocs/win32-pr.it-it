---
description: Contiene l'identificatore di classe (CLSID) di una trasformazione Media Foundation (MFT).
ms.assetid: 99ee6f50-1de7-41ea-be5b-135730138d5d
title: Attributo MFT_TRANSFORM_CLSID_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5ca1aa6a9d7691200761509e1a5e407a6c7db6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966989"
---
# <a name="mft_transform_clsid_attribute-attribute"></a>\_ \_ Attributo attributo CLSID Transform MFT \_

Contiene l'identificatore di classe (CLSID) di una trasformazione Media Foundation (MFT).

## <a name="data-type"></a>Tipo di dati

**GUID**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).

Per impostare questo attributo, chiamare [**IMFAttributes:: Seguid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Commenti

Questo attributo viene impostato sui puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) restituiti dalla funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

Questo attributo viene utilizzato internamente dall'oggetto Activation quando crea il MFT. Le applicazioni non devono utilizzare direttamente questo CLSID per creare il MFT, perché l'oggetto di attivazione potrebbe dover inizializzare il MFT. Pertanto, per creare un'istanza di MFT, chiamare [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) sull'oggetto Activation.

Si noti che la funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) si comporta in modo diverso rispetto alla funzione [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) in questo senso. La funzione **MFTEnum** Restituisce CLSID, che l'applicazione passa alla funzione **CoCreateInstance** . La funzione **MFTEnumEx** restituisce oggetti attivazione anziché CLSID.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | App desktop di Windows Server 2008 R2 \[ \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 




