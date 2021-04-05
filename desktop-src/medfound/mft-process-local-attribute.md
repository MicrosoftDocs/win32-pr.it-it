---
description: Specifica se una trasformazione Media Foundation (MFT) viene registrata solo nel processo di applicazioni.
ms.assetid: e10d6378-8e85-4f73-9fa3-a2e954fc8249
title: Attributo MFT_PROCESS_LOCAL_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1d3595ef530008b8d09f27e3e76fad81a06039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753943"
---
# <a name="mft_process_local_attribute-attribute"></a>\_Attributo dell' \_ attributo locale del processo MFT \_

Specifica se una trasformazione Media Foundation (MFT) viene registrata solo nel processo dell'applicazione.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="remarks"></a>Commenti

Questo attributo viene utilizzato come segue:

1.  L'applicazione registra una MFT locale chiamando la funzione [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) o [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) . Queste funzioni registrano il MFT nel processo dell'applicazione.
2.  Viene chiamata la funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) per enumerare MFTS che corrispondono a un particolare set di criteri. L'applicazione può chiamare direttamente la funzione **MFTEnumEx** , ma più spesso questa funzione viene chiamata dal caricatore della topologia.
3.  La funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) recupera una matrice di puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , ognuno dei quali rappresenta un oggetto Activation per un MFT. Se una MFT è registrata localmente, l' \_ attributo dell' \_ attributo locale del processo MFT \_ viene impostato su **true** nell'oggetto Activation corrispondente.

Il valore predefinito di questo attributo è **false**.

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

 

 




