---
description: Fornisce un'istanza di IMFMuxStreamAttributesManager che gestisce gli IMFAttributes che descrivono i sottoflussi di un'origine multimediale con multiplexing.
ms.assetid: 0149BD8B-8C9D-47FD-9EC1-BEBEE73BC73E
title: Attributo MF_DEVICESTREAM_MULTIPLEXED_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b495b4054337aaa709bee430ae78ff4bed658911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309573"
---
# <a name="mf_devicestream_multiplexed_manager-attribute"></a>\_Attributo di \_ Gestione multiplex MF DEVICESTREAM \_

Fornisce un'istanza di [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager) che gestisce gli [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) che descrivono i sottoflussi di un'origine multimediale con multiplexing.

## <a name="data-type"></a>Tipo di dati

**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**

## <a name="remarks"></a>Commenti

Passare questo valore in [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) per determinare se l'origine multimediale fornisce flussi multiplexati e, in caso affermativo, ottenere un'istanza di [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1703 \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 
