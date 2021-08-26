---
title: MCI_HMS_SECOND macro (Mciapi.h)
description: La macro MCI HMS SECOND recupera il componente secondi da un parametro contenente le informazioni \_ \_ di ore/minuti/secondi (HMS) contenenti.
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
ms.openlocfilehash: bc61747d891d3c91afd5e4cb7f9a16eef44e13eb3de275bbf9575d8a4f584d40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039231"
---
# <a name="mci_hms_second-macro"></a>Macro MCI \_ HMS \_ SECOND

La macro **MCI \_ HMS \_ SECOND** recupera il componente secondi da un parametro contenente le informazioni di ore/minuti/secondi (HMS) contenenti.

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

Ora in formato HMS.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il componente secondi delle informazioni HMS specificate.

## <a name="remarks"></a>Commenti

L'ora nel formato HMS è espressa come valore **DWORD** con il byte meno significativo contenente ore, il byte meno significativo successivo contenente i minuti e il byte meno significativo successivo contenente i secondi. Il byte più significativo è inutilizzato.

La macro **MCI \_ HMS \_ SECOND** è definita come segue:


```C++
#define MCI_HMS_SECOND(hms) ((BYTE)((hms) >> 16)) 
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

 

 





