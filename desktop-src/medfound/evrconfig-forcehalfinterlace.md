---
description: Impone al renderer video avanzato (EVR) di ignorare il secondo campo di ogni frame interlacciato.
ms.assetid: b79d9230-b127-4e9b-b73b-685ce27aefa9
title: Attributo EVRConfig_ForceHalfInterlace (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfeab4bcb3d05e615962fb8acc5f304ba3ea7e6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305382"
---
# <a name="evrconfig_forcehalfinterlace-attribute"></a>\_Attributo ForceHalfInterlace di EVRConfig

Impone al renderer video avanzato (EVR) di ignorare il secondo campo di ogni frame interlacciato.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="remarks"></a>Commenti

Questo attributo può essere impostato sul sink di supporto EVR. Per impostare l'attributo, utilizzare **QueryInterface** per eseguire una query sul sink multimediale EVR per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

L'impostazione di questo attributo ha lo stesso effetto dell'impostazione del flag **MFVideoMixPrefs \_ FORCEHALFINTERLACE** in EVR. Per una descrizione di questo flag, vedere [**MFVideoMixPrefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) .

La costante GUID per questo attributo viene esportata da strmiids. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                         |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>UUIDs. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi EVR](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Gestione della qualità dei video](video-quality-management.md)
</dt> </dl>

 

 




