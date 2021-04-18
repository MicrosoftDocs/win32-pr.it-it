---
title: MCI_MAKE_TMSF macro (Mciapi. h)
description: La \_ macro MCI make \_ TMSF crea un valore di ora in formato tracce/minuti/secondi/frame (TMSF) compresso dai valori di tracce, minuti, secondi e frame specificati.
ms.assetid: ff2d6938-0ff7-46d5-92be-42b4b6f35524
keywords:
- MCI_MAKE_TMSF macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MAKE_TMSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f06cd6a400f742b49dc29063e8473465ad7e32dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302630"
---
# <a name="mci_make_tmsf-macro"></a>MCI \_ make \_ TMSF (macro)

La macro **MCI \_ make \_ TMSF** crea un valore di ora in formato tracce/minuti/secondi/frame (TMSF) compresso dai valori di tracce, minuti, secondi e frame specificati.

## <a name="syntax"></a>Sintassi


```C++
DWORD MCI_MAKE_TMSF(
   BYTE tracks,
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*brani* 
</dt> <dd>

Numero di tracce.

</dd> <dt>

*minuti* 
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

Restituisce l'ora nel formato TMSF compresso.

## <a name="remarks"></a>Commenti

L'ora nel formato TMSF viene espressa come valore **DWORD** con il byte meno significativo contenente le tracce, il successivo byte meno significativo che contiene minuti, il successivo byte meno significativo contenente i secondi e il byte più significativo contenente i frame.

La macro **MCI \_ make \_ TMSF** è definita nel modo seguente:


```C++
#define MCI_MAKE_TMSF(t, m, s, f) ((DWORD)(((BYTE)(t) | \ 
                                  ((WORD)(m) << 8)) | \ 
                                  (((DWORD)(BYTE)(s) | \ 
                                  ((WORD)(f) << 8)) << 16))) 
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

 

 





