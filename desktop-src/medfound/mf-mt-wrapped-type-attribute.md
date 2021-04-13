---
description: Contiene un tipo di supporto di cui è stato eseguito il wrapper in un altro tipo di supporto.
ms.assetid: 3bd94523-0206-44d8-83a2-e569e4ab7815
title: Attributo MF_MT_WRAPPED_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad09c69f7b99c2c376a207270cadb034e735546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401528"
---
# <a name="mf_mt_wrapped_type-attribute"></a>\_ \_ Attributo tipo con wrapper MF mt \_

Contiene un tipo di supporto di cui è stato eseguito il wrapper in un altro tipo di supporto.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="remarks"></a>Commenti

Questo attributo viene utilizzato nella funzione [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) , che esegue il wrapping di un tipo di supporto all'interno di un altro tipo di supporto.

La funzione [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) esegue le operazioni seguenti:

1.  Converte il tipo di supporto originale in una matrice binaria.
2.  Imposta l'attributo del **\_ \_ \_ tipo di incapsulamento MF mt** sul nuovo tipo di supporto. Il valore dell'attributo è la matrice binaria.

Le applicazioni in genere non utilizzano direttamente questo attributo. Per annullare il wrapping del tipo di supporto originale, chiamare [**MFUnwrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfunwrapmediatype).

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows Vista app \[ \| UWP\]<br/>                              |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2008 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: seblob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 




