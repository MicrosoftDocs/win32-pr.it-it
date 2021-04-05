---
title: MCI_TMSF_FRAME macro (Mciapi. h)
description: La \_ macro MCI TMSF \_ frame Recupera il componente frames da un parametro contenente le informazioni relative a tracce/minuti/secondi/frame (TMSF) compressi.
ms.assetid: 1ba78d4f-4537-4955-abcc-842976b6b5b9
keywords:
- MCI_TMSF_FRAME macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_TMSF_FRAME
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c5a6620137aea397c3f1bc04ff7fe821666d837
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740255"
---
# <a name="mci_tmsf_frame-macro"></a>\_Macro TMSF \_ frame MCI

La macro **MCI \_ TMSF \_ frame** Recupera il componente frames da un parametro contenente le informazioni relative a tracce/minuti/secondi/frame (TMSF) compressi.

## <a name="syntax"></a>Sintassi


```C++
BYTE MCI_TMSF_FRAME(
   DWORD dwTMSF
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwTMSF* 
</dt> <dd>

Ora nel formato TMSF.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il componente frame delle informazioni TMSF specificate.

## <a name="remarks"></a>Commenti

L'ora nel formato TMSF viene espressa come valore **DWORD** con il byte meno significativo contenente le tracce, il successivo byte meno significativo che contiene minuti, il successivo byte meno significativo contenente i secondi e il byte più significativo contenente i frame.

La **macro \_ TMSF \_ frame MCI** è definita nel modo seguente:


```C++
#define MCI_TMSF_FRAME(tmsf) ((BYTE)((tmsf) >> 24)) 
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Macro MCI](mci-macros.md)
</dt> </dl>

 

 





