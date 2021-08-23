---
title: MCI_MAKE_MSF macro (Mciapi.h)
description: La macro MCI MAKE MSF crea un valore temporale in formato \_ \_ MSF (Packed Minutes/Seconds/Frames) dai valori di minuti, secondi e fotogrammi specificati.
ms.assetid: 8c981d84-b049-4448-a820-bff30896065e
keywords:
- MCI_MAKE_MSF macro Windows Multimediali
topic_type:
- apiref
api_name:
- MCI_MAKE_MSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e16f5cfa2b99f7bdbd7eb3029b3f0186904d8b8e94f455614464fadc98cdd20a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690131"
---
# <a name="mci_make_msf-macro"></a>Macro MCI \_ MAKE \_ MSF

La macro **MCI \_ MAKE \_ MSF** crea un valore temporale in formato MSF (Packed Minutes/Seconds/Frames) dai valori di minuti, secondi e fotogrammi specificati.

## <a name="syntax"></a>Sintassi


```C++
DWORD MCI_MAKE_MSF(
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Minuti* 
</dt> <dd>

Numero di minuti.

</dd> <dt>

*secondi* 
</dt> <dd>

Numero di secondi.

</dd> <dt>

*frame* 
</dt> <dd>

Numero di frame.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'ora in formato MSF imballato.

## <a name="remarks"></a>Commenti

L'ora in formato MSF viene espressa come valore **DWORD** con il byte meno significativo contenente minuti, il byte meno significativo successivo contenente i secondi e il byte meno significativo successivo contenente frame. Il byte più significativo è inutilizzato.

La macro **MCI \_ MAKE \_ MSF** è definita come segue:


```C++
#define MCI_MAKE_MSF(m, s, f) ((DWORD)(((BYTE)(m) | \ 
                              ((WORD)(s) << 8)) | \ 
                              (((DWORD)(BYTE)(f)) << 16))) 
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

 

 





