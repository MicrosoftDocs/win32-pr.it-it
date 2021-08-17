---
description: Indica che le informazioni sulla lunghezza NALU verranno inviate come BLOB con ogni campione H.264 compresso.
ms.assetid: 71B50B44-6025-4EEC-8B37-53D80CF37B07
title: MF_NALU_LENGTH_SET attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f409cb3c1846667ac21e7d46c559eefb0afc4fe4efbce1f454454d286733157
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104387"
---
# <a name="mf_nalu_length_set-attribute"></a>Attributo \_ MF NALU \_ LENGTH \_ SET

Indica che le informazioni sulla lunghezza NALU verranno inviate come **BLOB** con ogni campione H.264 compresso.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Impostare questo attributo sul tipo di supporto di input MEDIASUBTYPE \_ H264.

Impostare MF NALU LENGTH SET sul tipo di supporto di input del decodificatore \_ \_ H.264, indicando che per ogni campione di input sarà disponibile una lunghezza NALU e ogni esempio di input contiene un'immagine principale \_ completa.

Il **BLOB contenente** le informazioni sulla lunghezza NALU può essere recuperato dall'attributo [MF \_ NALU LENGTH \_ \_ INFORMATION](mf-nalu-length-information.md) nell'esempio di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                  |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 




