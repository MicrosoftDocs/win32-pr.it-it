---
description: Specifica il modo in cui un Media Foundation Transform (MFT) deve restituire un flusso video stereoscopico 3D.
ms.assetid: AA75A2FB-DEAC-44E9-93E9-4AC2D9F03B39
title: Attributo MF_ENABLE_3DVIDEO_OUTPUT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd0123a574ec74ed4aa9fa0aea3b2cabecbb29da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880234"
---
# <a name="mf_enable_3dvideo_output-attribute"></a>\_Abilita l' \_ \_ attributo output 3DVIDEO

Specifica il modo in cui un Media Foundation Transform (MFT) deve restituire un flusso video stereoscopico 3D.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il valore dell'attributo è un membro dell'enumerazione [**MF3DVideoOutputType**](/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype) .

Questo attributo si applica solo se MFT restituisce **true** per l' [attributo \_ \_ 3DVIDEO del supporto MFT](mft-support-3dvideo.md) .

Per ottenere o impostare questo attributo, chiamare [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) per ottenere l'archivio di attributi globale di MFT.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




