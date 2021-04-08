---
title: MCI_MAKE_MSF macro (Mciapi. h)
description: La \_ macro MCI make \_ MSF crea un valore di ora in formato minuti/secondi/frame (MSF) compresso dai valori di minuti, secondi e frame specificati.
ms.assetid: 8c981d84-b049-4448-a820-bff30896065e
keywords:
- MCI_MAKE_MSF macro Windows Multimedia
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
ms.openlocfilehash: ae7e8566986337d6b9b5161c85bcc62cecc52be0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964913"
---
# <a name="mci_make_msf-macro"></a>MCI \_ creare una \_ macro MSF

La macro **MCI \_ make \_ MSF** crea un valore di ora in formato minuti/secondi/frame (MSF) compresso dai valori di minuti, secondi e frame specificati.

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

Restituisce l'ora nel formato MSF compresso.

## <a name="remarks"></a>Commenti

L'ora nel formato MSF è espressa come valore **DWORD** con il byte meno significativo che contiene minuti, il successivo byte meno significativo contenente i secondi e il successivo byte meno significativo contenente i frame. Il byte più significativo è inutilizzato.

La macro **MCI \_ make \_ MSF** viene definita nel modo seguente:


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
| Intestazione<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Macro MCI](mci-macros.md)
</dt> </dl>

 

 





