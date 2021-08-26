---
title: MCI_HMS_HOUR macro (Mciapi.h)
description: La macro HOUR di MCI HMS recupera il componente hours da un parametro contenente le informazioni di \_ \_ ore/minuti/secondi (HMS) in formato pack.
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
ms.openlocfilehash: 97b8000e642d18f8499be5f8622a1cf7540fefbd041b7d34f23e1fd5e231815a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039271"
---
# <a name="mci_hms_hour-macro"></a>Macro HOUR \_ di MCI HMS \_

La macro **HOUR \_ di MCI HMS \_** recupera il componente hours da un parametro contenente le informazioni di ore/minuti/secondi (HMS) in formato pack.

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

Ora in formato HMS.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il componente ore delle informazioni HMS specificate.

## <a name="remarks"></a>Commenti

L'ora nel formato HMS è espressa come valore **DWORD** con il byte meno significativo contenente ore, il byte meno significativo successivo contenente i minuti e il byte meno significativo successivo contenente i secondi. Il byte più significativo è inutilizzato.

La macro **HOUR \_ di MCI HMS \_** è definita come segue:


```C++
#define MCI_HMS_HOUR(hms) ((BYTE)(hms)) 
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

 

 





