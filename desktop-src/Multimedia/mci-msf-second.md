---
title: MCI_MSF_SECOND macro (Mciapi. h)
description: La \_ seconda macro del MCI MSF \_ Recupera il componente secondi da un parametro contenente le informazioni sui minuti/secondi/frame (MSF) compressi.
ms.assetid: 2d455ce3-1823-46fa-a59e-b9c5c2fe5eb9
keywords:
- MCI_MSF_SECOND macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MSF_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85dffd36354b335818079ea5b0c88d16752b4501
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873981"
---
# <a name="mci_msf_second-macro"></a>\_ \_ Seconda macro del MCI MSF

La **\_ \_ seconda macro del MCI MSF** Recupera il componente secondi da un parametro contenente le informazioni sui minuti/secondi/frame (MSF) compressi.

## <a name="syntax"></a>Sintassi


```C++
BYTE MCI_MSF_SECOND(
   DWORD dwMSF
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwMSF* 
</dt> <dd>

Tempo in formato MSF.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il componente relativo ai secondi delle informazioni MSF specificate.

## <a name="remarks"></a>Commenti

L'ora nel formato MSF è espressa come valore **DWORD** con il byte meno significativo che contiene minuti, il successivo byte meno significativo contenente i secondi e il successivo byte meno significativo contenente i frame. Il byte più significativo è inutilizzato.

La **\_ \_ seconda** macro del MSF di MCI è definita come segue:


```C++
#define MCI_MSF_SECOND(msf) ((BYTE)(((WORD)(msf)) >> 8)) 
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

 

 





