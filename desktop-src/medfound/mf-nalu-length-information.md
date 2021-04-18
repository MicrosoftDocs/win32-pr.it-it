---
description: Indica le lunghezze di NALUs nell'esempio. Si tratta di un BLOB MF impostato su esempi di input compressi per il decodificatore H. 264.
ms.assetid: 09F54504-A6CF-4385-BDD7-8D23B1D0125C
title: Attributo MF_NALU_LENGTH_INFORMATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46d9a0b7cbec92c4cde40548b8d3baecf955b50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310824"
---
# <a name="mf_nalu_length_information-attribute"></a>\_ \_ \_ Attributo delle informazioni sulla lunghezza di MF Nalu

Indica le lunghezze di NALUs nell'esempio. Si tratta di un **BLOB** MF impostato su esempi di input compressi per il decodificatore H. 264.

## <a name="data-type"></a>Tipo di dati

**BLOB**

## <a name="remarks"></a>Commenti

Per impostare questo attributo, è necessario che il supporto sia di tipo MEDIASUBTYPE \_ H264 e che l'attributo [ \_ set di \_ lunghezza \_ MF Nalu](mf-nalu-length-set.md) sia impostato sul tipo di supporto di input di MEDIASUBTYPE \_ H264.

Impostare MF \_ Nalu \_ length \_ Information come **BLOB** nell'esempio di input, con un valore DWORD per ogni Nalu nell'esempio. Se ad esempio sono presenti AUD (9 byte), SPS (25 byte), PPS (10 byte), IDR slice1 (50 k), IDR Slice 2 (60 k), dovrebbero essere presenti 5 DWORD con valori 9, 25, 10, 50 k, 60 k nel **BLOB**.

Di seguito è riportato il codice che imposta il **BLOB**, dove **rgdwNALULengthInfo** è una matrice di tipo DWORD e **uiNaluLengthIdx** è la lunghezza Nalu valida impostata sul **BLOB**.


```C++
m_spSample->SetBlob( MF_NALU_LENGTH_INFORMATION, 
                    (UINT8*) m_wpParent->m_pdwNALULengthInfo, 
                    sizeof(DWORD)*uiNaluLengthIdx ), 
                    done );
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 




