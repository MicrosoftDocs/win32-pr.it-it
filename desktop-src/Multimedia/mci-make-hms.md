---
title: MCI_MAKE_HMS macro (Mciapi. h)
description: Il MCI \_ make \_ HMS macro crea un valore di ora in formato ore/minuti/secondi (HMS) compresso tra i valori di ore, minuti e secondi specificati.
ms.assetid: 470e89eb-36e1-4b05-babd-4c986adc88dd
keywords:
- MCI_MAKE_HMS macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MAKE_HMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f37c95df89ed6a799575e964ae274e01e329ef1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743143"
---
# <a name="mci_make_hms-macro"></a>MCI \_ make \_ HMS macro

Il **MCI \_ make \_ HMS** macro crea un valore di ora in formato ore/minuti/secondi (HMS) compresso tra i valori di ore, minuti e secondi specificati.

## <a name="syntax"></a>Sintassi


```C++
DWORD MCI_MAKE_HMS(
   BYTE hours,
   BYTE minutes,
   BYTE seconds
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ore* 
</dt> <dd>

Numero di ore.

</dd> <dt>

*minuti* 
</dt> <dd>

Numero di minuti.

</dd> <dt>

*secondi* 
</dt> <dd>

Numero di secondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'ora nel formato HMS compresso.

## <a name="remarks"></a>Commenti

L'ora nel formato HMS è espressa come valore **DWORD** con il byte meno significativo contenente le ore, il successivo byte meno significativo che contiene minuti e il successivo byte meno significativo contenente i secondi. Il byte più significativo è inutilizzato.

Il **MCI \_ make \_ HMS** macro viene definito come segue:


```C++
#define MCI_MAKE_HMS(h, m, s) ((DWORD)(((BYTE)(h) | \ 
                              ((WORD)(m) << 8)) | \ 
                              (((DWORD)(BYTE)(s)) << 16))) 
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

 

 





