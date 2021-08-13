---
description: Forza il renderer video avanzato (EVR) a combinare il video all'interno di un rettangolo più piccolo del rettangolo di output e quindi ridimensionare il risultato.
ms.assetid: f85c4114-ac94-4deb-a1cf-896209079f8b
title: EVRConfig_ForceScaling attributo (Uuids.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd85fa67af3cea27564400b86cf6c8e32e3c15645cbb4f84cc97344fbab9ef60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119346201"
---
# <a name="evrconfig_forcescaling-attribute"></a>Attributo ForceScaling EVRConfig \_

Forza il renderer video avanzato (EVR) a combinare il video all'interno di un rettangolo più piccolo del rettangolo di output e quindi ridimensionare il risultato.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Commenti

Questo attributo può essere impostato nel sink del supporto EVR. Per impostare l'attributo, usare **QueryInterface** per eseguire una query sul sink multimediale EVR per [**l'interfaccia IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

L'impostazione di questo attributo ha lo stesso effetto dell'impostazione del flag **\_ ForceScaling MFVideoRenderPrefs** nell'EVR. Per [**una descrizione di questo flag, vedere MFVideoRenderPrefs.**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs)

La costante GUID per questo attributo viene esportata da strmiids.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Uuids.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi Media Foundation alfabetici](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi EVR](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Gestione della qualità video](video-quality-management.md)
</dt> </dl>

 

 




