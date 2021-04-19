---
description: Specifica se la sessione multimediale usa il preroll sul sink multimediale rappresentato da questo nodo di topologia.
ms.assetid: 1781f3a0-6baa-4e06-b2eb-9a8f572aa040
title: Attributo MF_TOPONODE_DISABLE_PREROLL (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3d031a4ee50262e717731ae517d4441e9be9a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318045"
---
# <a name="mf_toponode_disable_preroll-attribute"></a>MF \_ TOPONODE \_ disabilitare l' \_ attributo preroll

Specifica se la sessione multimediale usa il preroll sul sink multimediale rappresentato da questo nodo di topologia.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Questo attributo si applica ai nodi di output (**\_ nodo di \_ output \_ della topologia MF**).

Se il valore di questo attributo è **true**, la sessione multimediale non esegue la preregistrazione dei dati nel sink multimediale, anche se il sink multimediale espone l'interfaccia [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) . Se il valore è **false**, la sessione multimediale esegue il prerolling dei dati se il sink multimediale implementa **IMFMediaSinkPreroll**. Il valore predefinito è **false**.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> </dl>

 

 




