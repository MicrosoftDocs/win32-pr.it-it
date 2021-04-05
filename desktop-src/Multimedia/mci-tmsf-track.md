---
title: MCI_TMSF_TRACK macro (Mciapi. h)
description: La \_ macro MCI TMSF \_ Track Recupera il componente Tracks da un parametro contenente le informazioni sulle tracce compresse/minuti/secondi/frame (TMSF).
ms.assetid: 3455442c-5c66-47c7-b06b-1a2de0e2dfed
keywords:
- MCI_TMSF_TRACK macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_TMSF_TRACK
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa8512169d0e5b3d6892dd1bf615a220143e6d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873925"
---
# <a name="mci_tmsf_track-macro"></a>\_Macro di \_ rilevamento MCI TMSF

La macro **MCI \_ TMSF \_ Track** Recupera il componente Tracks da un parametro contenente le informazioni sulle tracce compresse/minuti/secondi/frame (TMSF).

## <a name="syntax"></a>Sintassi


```C++
BYTE MCI_TMSF_TRACK(
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

Restituisce il componente Tracks delle informazioni TMSF specificate.

## <a name="remarks"></a>Commenti

L'ora nel formato TMSF viene espressa come valore **DWORD** con il byte meno significativo contenente le tracce, il successivo byte meno significativo che contiene minuti, il successivo byte meno significativo contenente i secondi e il byte più significativo contenente i frame.

La macro **MCI \_ TMSF \_ Track** viene definita nel modo seguente:


```C++
#define MCI_TMSF_TRACK(tmsf) ((BYTE)(tmsf)) 
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

 

 





