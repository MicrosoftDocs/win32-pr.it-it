---
description: Impone al renderer video avanzato (EVR) di combinare il video in un rettangolo di dimensioni minori rispetto al rettangolo di output, quindi ridimensionare il risultato.
ms.assetid: f85c4114-ac94-4deb-a1cf-896209079f8b
title: Attributo EVRConfig_ForceScaling (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b82b7e017d414e86b8b4332fe5646e4808d4009
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049303"
---
# <a name="evrconfig_forcescaling-attribute"></a>\_Attributo ForceScaling di EVRConfig

Impone al renderer video avanzato (EVR) di combinare il video in un rettangolo di dimensioni minori rispetto al rettangolo di output, quindi ridimensionare il risultato.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="remarks"></a>Commenti

Questo attributo può essere impostato sul sink di supporto EVR. Per impostare l'attributo, utilizzare **QueryInterface** per eseguire una query sul sink multimediale EVR per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

L'impostazione di questo attributo ha lo stesso effetto dell'impostazione del flag **MFVideoRenderPrefs \_ FORCESCALING** in EVR. Per una descrizione di questo flag, vedere [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) .

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

 

 




