---
description: Specifica se il caricatore della topologia modificherà i tipi di supporto in una trasformazione Media Foundation (MFT). Le applicazioni in genere non utilizzano questo attributo.
ms.assetid: 96a99f35-f9db-407e-a4e3-7adc3caccb19
title: Attributo MF_ACTIVATE_MFT_LOCKED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4d6dcb6cb60f760d87761a18b2b83545937878c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130726"
---
# <a name="mf_activate_mft_locked-attribute"></a>MF \_ Activate \_ - \_ attributo bloccato MFT

Specifica se il caricatore della topologia modificherà i tipi di supporto in una trasformazione Media Foundation (MFT). Le applicazioni in genere non utilizzano questo attributo.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Se il valore di questo attributo è diverso da zero, il caricatore della topologia non modificherà i tipi di supporto in MFT. Il caricatore della topologia imposta questo attributo dopo aver caricato la topologia.

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

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 




