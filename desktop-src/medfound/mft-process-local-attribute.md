---
description: Specifica se una trasformazione Media Foundation (MFT) viene registrata solo nel processo delle applicazioni.
ms.assetid: e10d6378-8e85-4f73-9fa3-a2e954fc8249
title: MFT_PROCESS_LOCAL_Attribute attributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47afaa812468f185731313cec5a7519bf418c67997d5dc32101cd2403d7b425c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117688860"
---
# <a name="mft_process_local_attribute-attribute"></a>Attributo MFT \_ PROCESS \_ LOCAL \_

Specifica se una Media Foundation (MFT) viene registrata solo nel processo dell'applicazione.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Commenti

Questo attributo viene usato come segue:

1.  L'applicazione registra un MFT locale chiamando la [**funzione MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) o [**MFTRegisterLocalByCLSID.**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) Queste funzioni registrano MFT nel processo dell'applicazione.
2.  La [**funzione MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) viene chiamata per enumerare gli MFT che corrispondono a un determinato set di criteri. L'applicazione potrebbe chiamare direttamente la funzione **MFTEnumEx,** ma più spesso questa funzione viene chiamata dal caricatore della topologia.
3.  La [**funzione MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) recupera una matrice di puntatori [**IMFActivate,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) ognuno dei quali rappresenta un oggetto di attivazione per un MFT. Se un MFT è registrato in locale, l'attributo MFT \_ PROCESS LOCAL Attribute viene impostato su \_ \_ **TRUE** nell'oggetto di attivazione corrispondente.

Il valore predefinito per questo attributo è **FALSE.**

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 R2 \[ \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 




