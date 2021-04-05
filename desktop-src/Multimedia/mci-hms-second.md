---
title: MCI_HMS_SECOND macro (Mciapi. h)
description: La \_ macro MCI HMS \_ Second Recupera il componente secondi da un parametro contenente le informazioni relative a ore/minuti/secondi (HMS) compressi.
ms.assetid: b6895bec-524f-4345-ae65-e75168855df2
keywords:
- MCI_HMS_SECOND macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_HMS_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30b869141d6480ba0d986450ce950097ba240009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874558"
---
# <a name="mci_hms_second-macro"></a>\_Terza macro MCI HMS \_ Second

La macro **MCI \_ HMS \_ Second** Recupera il componente secondi da un parametro contenente le informazioni relative a ore/minuti/secondi (HMS) compressi.

## <a name="syntax"></a>Sintassi


```C++
BYTE MCI_HMS_SECOND(
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

Restituisce il componente relativo ai secondi delle informazioni di HMS specificate.

## <a name="remarks"></a>Commenti

L'ora nel formato HMS è espressa come valore **DWORD** con il byte meno significativo contenente le ore, il successivo byte meno significativo che contiene minuti e il successivo byte meno significativo contenente i secondi. Il byte più significativo è inutilizzato.

La macro **MCI \_ HMS \_ Second** viene definita nel modo seguente:


```C++
#define MCI_HMS_SECOND(hms) ((BYTE)((hms) >> 16)) 
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

 

 





