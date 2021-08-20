---
title: MCI_TMSF_TRACK macro (Mciapi.h)
description: La macro MCI TMSF TRACK recupera il componente tracks da un parametro contenente le informazioni di \_ \_ traccia/minuti/secondi/fotogrammi (TMSF).
ms.assetid: 3455442c-5c66-47c7-b06b-1a2de0e2dfed
keywords:
- MCI_TMSF_TRACK macro Windows Multimediali
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
ms.openlocfilehash: 7090a2a9b652d7c989aadd70d8843ece04bf467bbbe353c22c3f76fee8a9712b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137952"
---
# <a name="mci_tmsf_track-macro"></a>Macro MCI \_ TMSF \_ TRACK

La macro **MCI \_ TMSF \_ TRACK** recupera il componente tracks da un parametro contenente le informazioni di traccia/minuti/secondi/fotogrammi (TMSF).

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

Ora in formato TMSF.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il componente tracks delle informazioni TMSF specificate.

## <a name="remarks"></a>Commenti

L'ora in formato TMSF viene espressa come valore **DWORD** con il byte meno significativo contenente tracce, il byte meno significativo successivo contenente minuti, il byte meno significativo successivo contenente secondi e il byte più significativo contenente frame.

La macro **MCI \_ TMSF \_ TRACK** è definita come segue:


```C++
#define MCI_TMSF_TRACK(tmsf) ((BYTE)(tmsf)) 
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Macro MCI](mci-macros.md)
</dt> </dl>

 

 





