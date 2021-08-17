---
description: Il Media Foundation decodificatore video DV è un Media Foundation transform che decodifica il video DV.
ms.assetid: 97e5ba52-92fc-49e4-9c22-6f61bfda2003
title: Decodificatore video DV
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd91cf325d9ba715d75aae884e29665d05d449ca39f01c195f9b13e2e1f8c1fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118064094"
---
# <a name="dv-video-decoder"></a>Decodificatore video DV

Il Media Foundation decodificatore video DV è un [Media Foundation transform](media-foundation-transforms.md) che decodifica il video DV.

Il decodificatore video DV supporta i tipi di input seguenti:



| Subtype                 | Descrizione                  |
|-------------------------|------------------------------|
| **MFVideoFormat \_ DVC**  | DVC/DV Video                 |
| **MFVideoFormat \_ DVHD** | HD-DVCR (1125-60 o 1250-50) |
| **MFVideoFormat \_ DVSD** | SDL-DVCR (525-60 o 625-50)  |
| **MFVideoFormat \_ DVSL** | SD-DVCR (525-60 o 625-50)   |



 

Supporta un singolo tipo di output:



| Subtype             | Descrizione |
|---------------------|-------------|
| MFVideoFormat \_ YUY2 | Video yuy2  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                |
| DLL<br/>                      | <dl> <dt>Mfdvdec.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> <dt>

[Formati multimediali supportati in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Tipi di supporti video](video-media-types.md)
</dt> </dl>

 

 




