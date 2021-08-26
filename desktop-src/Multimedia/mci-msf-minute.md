---
title: MCI_MSF_MINUTE macro (Mciapi.h)
description: La macro MCI MSF MINUTE recupera il componente minuti da un parametro contenente informazioni di \_ \_ minuti/secondi/fotogrammi (MSF) di tipo pack.
ms.assetid: 60ac6662-d828-4635-a019-2603199523c5
keywords:
- MCI_MSF_MINUTE macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MSF_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8423e63c7e155c072b496a9bf13c332619f96e8c6780cac6fae266f6a924c9f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039141"
---
# <a name="mci_msf_minute-macro"></a>Macro \_ MCI MSF \_ MINUTE

La macro **\_ MCI MSF \_ MINUTE** recupera il componente minuti da un parametro contenente informazioni di minuti/secondi/fotogrammi (MSF) di tipo pack.

## <a name="syntax"></a>Sintassi


```C++
BYTE MCI_MSF_MINUTE(
   DWORD dwMSF
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwMSF* 
</dt> <dd>

Ora in formato MSF.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il componente minuti delle informazioni MSF specificate.

## <a name="remarks"></a>Commenti

L'ora in formato MSF è espressa come valore **DWORD** con il byte meno significativo contenente minuti, il byte meno significativo successivo contenente i secondi e il byte meno significativo successivo contenente frame. Il byte più significativo è inutilizzato.

La macro **\_ MCI MSF \_ MINUTE** è definita come segue:


```C++
#define MCI_MSF_MINUTE(msf) ((BYTE)(msf)) 
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

 

 





