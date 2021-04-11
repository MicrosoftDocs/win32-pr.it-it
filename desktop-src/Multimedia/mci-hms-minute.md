---
title: MCI_HMS_MINUTE macro (Mciapi. h)
description: La \_ macro MCI HMS \_ minute Recupera il componente minuti da un parametro che contiene le informazioni relative a ore/minuti/secondi (HMS) compressi.
ms.assetid: d083f769-9825-48cc-80f9-34ce3ef66ad6
keywords:
- MCI_HMS_MINUTE macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_HMS_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c91d2dcb13ea6b206df2a0dbc0d6a2e7096e59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121458"
---
# <a name="mci_hms_minute-macro"></a>Macro di MCI \_ HMS \_ minute

La macro **MCI \_ HMS \_ minute** Recupera il componente minuti da un parametro che contiene le informazioni relative a ore/minuti/secondi (HMS) compressi.

## <a name="syntax"></a>Sintassi


```C++
BYTE MCI_HMS_MINUTE(
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

Restituisce il componente minuti delle informazioni di HMS specificate.

## <a name="remarks"></a>Commenti

L'ora nel formato HMS è espressa come valore **DWORD** con il byte meno significativo contenente le ore, il successivo byte meno significativo che contiene minuti e il successivo byte meno significativo contenente i secondi. Il byte più significativo è inutilizzato.

La macro **MCI \_ HMS \_ minute** viene definita nel modo seguente:


```C++
#define MCI_HMS_MINUTE(hms) ((BYTE)(((WORD)(hms)) >> 8)) 
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

 

 





