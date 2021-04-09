---
description: Il decodificatore video Media Foundation DV è una trasformazione Media Foundation che decodifica il video DV.
ms.assetid: 97e5ba52-92fc-49e4-9c22-6f61bfda2003
title: Decoder video DV
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed277c3e4dd1aaa031d4dcf4694c7c3051fe37ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749258"
---
# <a name="dv-video-decoder"></a>Decoder video DV

Il decodificatore video Media Foundation DV è una [trasformazione Media Foundation](media-foundation-transforms.md) che decodifica il video DV.

Il decodificatore video DV supporta i tipi di input seguenti:



| Subtype                 | Descrizione                  |
|-------------------------|------------------------------|
| **\_DVC MFVideoFormat**  | Video su DVC/DV                 |
| **\_DVHD MFVideoFormat** | HD-DVCR (1125-60 o 1250-50) |
| **\_DVSD MFVideoFormat** | SDL-DVCR (525-60 o 625-50)  |
| **\_DVSL MFVideoFormat** | SD-DVCR (525-60 o 625-50)   |



 

Supporta un solo tipo di output:



| Subtype             | Descrizione |
|---------------------|-------------|
| \_YUY2 MFVideoFormat | Video di YUY2  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                             |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                |
| DLL<br/>                      | <dl> <dt>Mfdvdec.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> <dt>

[Formati multimediali supportati in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Tipi di supporti video](video-media-types.md)
</dt> </dl>

 

 




