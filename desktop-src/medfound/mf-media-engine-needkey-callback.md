---
description: Attributo passato in IMFMediaEngineNeedKeyNotify al motore multimediale al momento della creazione.
ms.assetid: B9625B3C-00AC-4F46-BD76-5C77822F5829
title: Attributo MF_MEDIA_ENGINE_NEEDKEY_CALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3de502bbe1d7f83dfd8ee7478e20786244f654e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320717"
---
# <a name="mf_media_engine_needkey_callback-attribute"></a>\_Attributo di \_ \_ callback NEEDKEY del motore multimediale MF \_

Attributo passato in [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) al motore multimediale al momento della creazione.

## <a name="data-type"></a>Tipo di dati

**IMFMediaEngineNeedKeyNotify \* *_ archiviato come _* IUnknown\***

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Per impostare questo attributo, chiamare [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un puntatore all'interfaccia [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) , implementata dall'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                 |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




