---
description: Contiene l'identificatore di classe (CLSID) di una trasformazione Media Foundation (MFT).
ms.assetid: 99ee6f50-1de7-41ea-be5b-135730138d5d
title: MFT_TRANSFORM_CLSID_Attribute attributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0122b783d8b321aa2a5c7788a589e19625b6a2bde8e37b0b659b0a1192f8c7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240199"
---
# <a name="mft_transform_clsid_attribute-attribute"></a>Attributo \_ \_ CLSID MFT TRANSFORM \_

Contiene l'identificatore di classe (CLSID) di una trasformazione Media Foundation (MFT).

## <a name="data-type"></a>Tipo di dati

**GUID**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).

Per impostare questo attributo, chiamare [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Commenti

Questo attributo viene impostato sui [**puntatori IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) restituiti dalla [**funzione MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)

Questo attributo viene utilizzato internamente dall'oggetto di attivazione quando crea l'MFT. Le applicazioni non devono usare questo CLSID direttamente per creare il MFT, perché l'oggetto attivazione potrebbe dover inizializzare MFT. Pertanto, per creare un'istanza del MFT, chiamare [**IMFActivate::ActivateObject sull'oggetto**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) attivazione.

Si noti che [**la funzione MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) si comporta in modo diverso rispetto alla [**funzione MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) in questo senso. La **funzione MFTEnum** restituisce i CLSID, che l'applicazione passa alla **funzione CoCreateInstance.** La **funzione MFTEnumEx** restituisce gli oggetti attivazione anziché i CLSID.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 R2 \[ \| app UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 




