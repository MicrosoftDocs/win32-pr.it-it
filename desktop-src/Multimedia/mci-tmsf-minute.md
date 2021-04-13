---
title: MCI_TMSF_MINUTE macro (Mciapi. h)
description: La \_ macro MCI TMSF \_ minute Recupera il componente minuti da un parametro contenente le informazioni relative a tracce/minuti/secondi/frame (TMSF) compressi.
ms.assetid: 9a972579-240f-4641-b65e-9088f39cdf9e
keywords:
- MCI_TMSF_MINUTE macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_TMSF_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b69a12c2622f3f97f04bdca89389c8ab9be7e948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517817"
---
# <a name="mci_tmsf_minute-macro"></a>\_Macro TMSF \_ minuto MCI

La macro **MCI \_ TMSF \_ minute** Recupera il componente minuti da un parametro contenente le informazioni relative a tracce/minuti/secondi/frame (TMSF) compressi.

## <a name="syntax"></a>Sintassi


```C++
BYTE MCI_TMSF_MINUTE(
   DWORD dwTMSF
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwTMSF* 
</dt> <dd>

Ora nel formato TMSF.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il componente minuti delle informazioni TMSF specificate.

## <a name="remarks"></a>Commenti

L'ora nel formato TMSF viene espressa come valore **DWORD** con il byte meno significativo contenente le tracce, il successivo byte meno significativo che contiene minuti, il successivo byte meno significativo contenente i secondi e il byte più significativo contenente i frame.

La macro **MCI \_ TMSF \_ minute** viene definita nel modo seguente:


```C++
#define MCI_TMSF_MINUTE(tmsf) ((BYTE)(((WORD)(tmsf)) >> 8)) 
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

 

 





