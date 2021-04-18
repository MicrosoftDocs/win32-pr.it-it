---
title: MCI_MSF_MINUTE macro (Mciapi. h)
description: La \_ macro del \_ momento MSF di MCI Recupera il componente minuti da un parametro contenente le informazioni relative a minuti/secondi/frame (MSF) compressi.
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
ms.openlocfilehash: f65f978c13fc1b3fbf86266c35786b21612c4e7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302629"
---
# <a name="mci_msf_minute-macro"></a>\_Macro del minuto MSF di MCI \_

La macro del **\_ \_ momento MSF di MCI** Recupera il componente minuti da un parametro contenente le informazioni relative a minuti/secondi/frame (MSF) compressi.

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

Tempo in formato MSF.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il componente minuti delle informazioni MSF specificate.

## <a name="remarks"></a>Commenti

L'ora nel formato MSF è espressa come valore **DWORD** con il byte meno significativo che contiene minuti, il successivo byte meno significativo contenente i secondi e il successivo byte meno significativo contenente i frame. Il byte più significativo è inutilizzato.

La macro del **\_ \_ minuto MSF di MCI** è definita come segue:


```C++
#define MCI_MSF_MINUTE(msf) ((BYTE)(msf)) 
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

 

 





