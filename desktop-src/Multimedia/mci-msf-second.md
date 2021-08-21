---
title: MCI_MSF_SECOND macro (Mciapi.h)
description: La macro MCI MSF SECOND recupera il componente secondi da un parametro contenente informazioni di \_ \_ minuti/secondi/fotogrammi (MSF).
ms.assetid: 2d455ce3-1823-46fa-a59e-b9c5c2fe5eb9
keywords:
- MCI_MSF_SECOND macro Windows Multimediali
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
ms.openlocfilehash: eb09643ae8d3ecdf59c6f3631c9dc28f43bba7ee0434ebabed3e4260c3fec01d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138360"
---
# <a name="mci_msf_second-macro"></a>Macro \_ MCI MSF \_ SECOND

La macro **\_ MCI MSF \_ SECOND** recupera il componente secondi da un parametro contenente informazioni di minuti/secondi/fotogrammi (MSF).

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

Ora in formato MSF.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il componente secondi delle informazioni MSF specificate.

## <a name="remarks"></a>Commenti

L'ora in formato MSF viene espressa come valore **DWORD** con il byte meno significativo contenente minuti, il byte meno significativo successivo contenente i secondi e il byte meno significativo successivo contenente frame. Il byte più significativo è inutilizzato.

La macro **\_ MCI MSF \_ SECOND** è definita come segue:


```C++
#define MCI_MSF_SECOND(msf) ((BYTE)(((WORD)(msf)) >> 8)) 
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

 

 





