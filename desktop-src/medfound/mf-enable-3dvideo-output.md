---
description: Specifica in che modo una Media Foundation (MFT) deve eseguire l'output di un flusso video stereoscopico 3D.
ms.assetid: AA75A2FB-DEAC-44E9-93E9-4AC2D9F03B39
title: MF_ENABLE_3DVIDEO_OUTPUT attributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed361ef53d628e0970ffa35f9920750c9d3b0f7efbe81a0ef8759e8ba00a45ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013171"
---
# <a name="mf_enable_3dvideo_output-attribute"></a>Attributo MF \_ ENABLE \_ 3DVIDEO \_ OUTPUT

Specifica in che modo una Media Foundation (MFT) deve eseguire l'output di un flusso video stereoscopico 3D.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il valore dell'attributo è un membro [**dell'enumerazione MF3DVideoOutputType.**](/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype)

Questo attributo si applica solo se MFT restituisce **TRUE** per l'attributo [MFT \_ SUPPORT \_ 3DVIDEO.](mft-support-3dvideo.md)

Per ottenere o impostare questo attributo chiamare [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) per ottenere l'archivio attributi globale di MFT.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                        |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




