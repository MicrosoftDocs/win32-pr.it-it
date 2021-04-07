---
title: MCI_HMS_HOUR macro (Mciapi. h)
description: La \_ macro MCI HMS \_ hour Recupera il componente hours da un parametro contenente le informazioni relative a ore/minuti/secondi (HMS) compressi.
ms.assetid: 55968b2b-2bfe-48ac-a50f-5c8741d11e33
keywords:
- MCI_HMS_HOUR macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_HMS_HOUR
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ecab8b5de7712a9c1a5ebd5c0a4401b264d7ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048743"
---
# <a name="mci_hms_hour-macro"></a>\_Macro di ora della settime MCI \_

La macro **MCI \_ HMS \_ hour** Recupera il componente hours da un parametro contenente le informazioni relative a ore/minuti/secondi (HMS) compressi.

## <a name="syntax"></a>Sintassi


```C++
BYTE MCI_HMS_HOUR(
   DWORD dwHMS
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwHMS* 
</dt> <dd>

Tempo in formato HMS.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il componente relativo alle ore delle informazioni di HMS specificate.

## <a name="remarks"></a>Commenti

L'ora nel formato HMS è espressa come valore **DWORD** con il byte meno significativo contenente le ore, il successivo byte meno significativo che contiene minuti e il successivo byte meno significativo contenente i secondi. Il byte più significativo è inutilizzato.

La macro **MCI \_ HMS \_ hour** viene definita nel modo seguente:


```C++
#define MCI_HMS_HOUR(hms) ((BYTE)(hms)) 
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

 

 





