---
description: Imposta la modalità di elaborazione del Stabilizzazione video MFT.
ms.assetid: 0D49892A-8628-4F2B-B41B-51160A19DC9B
title: Attributo MF_VIDEODSP_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88383e6bdd197e4912c660657eefa6b9e812fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130127"
---
# <a name="mf_videodsp_mode-attribute"></a>\_ \_ Attributo modalità MF VIDEODSP

Imposta la modalità di elaborazione del [**stabilizzazione video MFT**](video-stabilization-mft.md).

## <a name="data-type"></a>Tipo di dati

**MFVideoDSPMode** archiviato come **UIINT32**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un valore di enumerazione [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) . Questo attributo può essere usato per abilitare o disabilitare la stabilizzazione dell'immagine e può essere aggiornato per ogni esempio di output.

Per impostare l'attributo:

1.  Chiamare [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) sulla MFT per la stabilizzazione video per ottenere un puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
2.  Chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) SetAttribute per impostare l'attributo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Stabilizzazione video MFT**](video-stabilization-mft.md)
</dt> </dl>

 

 




