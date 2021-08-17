---
description: Indica le lunghezze delle unità NALU nell'esempio. Si tratta di un BLOB MF impostato su campioni di input compressi nel decodificatore H.264.
ms.assetid: 09F54504-A6CF-4385-BDD7-8D23B1D0125C
title: MF_NALU_LENGTH_INFORMATION attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2020c0086247adda742ce2613045bb3a2004c3b8c13c7cdcb04a0ff3997cf0cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104417"
---
# <a name="mf_nalu_length_information-attribute"></a>Attributo MF \_ NALU \_ LENGTH \_ INFORMATION

Indica le lunghezze delle unità NALU nell'esempio. Si tratta di un **BLOB** MF impostato su campioni di input compressi nel decodificatore H.264.

## <a name="data-type"></a>Tipo di dati

**Blob**

## <a name="remarks"></a>Commenti

Per impostare questo attributo, il supporto deve essere di tipo MEDIASUBTYPE H264 e l'attributo MF NALU LENGTH SET deve essere impostato sul tipo di supporto di \_ input MEDIASUBTYPE [ \_ \_ \_ ](mf-nalu-length-set.md) \_ H264.

Impostare MF NALU LENGTH INFORMATION come BLOB nell'esempio di input, con un \_ \_ valore \_ DWORD per ogni NALU nell'esempio.  Ad esempio, se sono presenti AUD (9 byte), SPS (25 byte), PPS (10 byte), IDR slice1 (50 k), IDR slice 2 (60 k), dovrebbero essere presenti 5 DWORD con valori 9, 25, 10, 50 k, 60 k nel **BLOB**.

In questo esempio il codice che imposta **il BLOB**, dove **rgdwNALULengthInfo** è una matrice di tipo DWORD e **uiNaluLengthIdx** è la lunghezza NALU valida impostata su **BLOB**.


```C++
m_spSample->SetBlob( MF_NALU_LENGTH_INFORMATION, 
                    (UINT8*) m_wpParent->m_pdwNALULengthInfo, 
                    sizeof(DWORD)*uiNaluLengthIdx ), 
                    done );
```



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

 

 




