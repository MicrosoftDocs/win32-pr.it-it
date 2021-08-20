---
title: MCI_MAKE_TMSF macro (Mciapi.h)
description: La macro MCI MAKE TMSF crea un valore di ora in formato \_ \_ tracce/minuti/secondi/fotogrammi (TMSF) dai valori di tracce, minuti, secondi e fotogrammi specificati.
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
ms.openlocfilehash: ec038e0eb1e46c46162c9a2139f03881689db5fe1ee5993a8e135e5d92d67984
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138404"
---
# <a name="mci_make_tmsf-macro"></a>Macro \_ TMSF MCI MAKE \_

La macro **\_ MCI MAKE \_ TMSF** crea un valore di ora in formato tracce/minuti/secondi/fotogrammi (TMSF) dai valori di tracce, minuti, secondi e fotogrammi specificati.

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

Restituisce l'ora in formato TMSF in formato packed.

## <a name="remarks"></a>Commenti

L'ora in formato TMSF è espressa come valore **DWORD** con il byte meno significativo contenente tracce, il byte meno significativo successivo contenente minuti, il byte meno significativo successivo contenente i secondi e il byte più significativo contenente frame.

La macro **\_ \_ TMSF MCI MAKE** è definita come segue:


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
| Intestazione<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Macro MCI](mci-macros.md)
</dt> </dl>

 

 





