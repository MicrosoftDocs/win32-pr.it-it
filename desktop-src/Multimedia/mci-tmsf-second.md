---
title: MCI_TMSF_SECOND macro (Mciapi.h)
description: La macro MCI TMSF SECOND recupera il componente secondi da un parametro contenente le informazioni di \_ \_ traccia/minuti/secondi/fotogrammi (TMSF) in pacchetto.
ms.assetid: 0f431545-bde0-4898-9a9d-993847aedf50
keywords:
- MCI_TMSF_SECOND macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_TMSF_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92dc8f7771df35e9ddc712d263e805ba1e844ca42cde607d7204dc6dc7b350d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784200"
---
# <a name="mci_tmsf_second-macro"></a>Macro MCI \_ TMSF \_ SECOND

La macro **MCI \_ TMSF \_ SECOND** recupera il componente secondi da un parametro contenente le informazioni di traccia/minuti/secondi/fotogrammi (TMSF) in pacchetto.

## <a name="syntax"></a>Sintassi


```C++
BYTE MCI_TMSF_SECOND(
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

Restituisce il componente secondi delle informazioni TMSF specificate.

## <a name="remarks"></a>Commenti

L'ora in formato TMSF è espressa come valore **DWORD** con il byte meno significativo contenente tracce, il byte meno significativo successivo contenente minuti, il byte meno significativo successivo contenente i secondi e il byte più significativo contenente frame.

La macro **MCI \_ TMSF \_ SECOND** è definita come segue:


```C++
#define MCI_TMSF_SECOND(tmsf) ((BYTE)((tmsf) >> 16)) 
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

 

 





