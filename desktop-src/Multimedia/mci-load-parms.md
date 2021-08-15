---
title: MCI_LOAD_PARMS struttura (Mmsystem.h)
description: La struttura MCI \_ LOAD \_ PARMS contiene il nome file da caricare per il comando MCI \_ LOAD.
ms.assetid: 371d11cc-44db-496b-b51a-66d7b919b794
keywords:
- MCI_LOAD_PARMS struttura Windows Multimediali
topic_type:
- apiref
api_name:
- MCI_LOAD_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52a5c875bbbfff6f94857bc7337a0cba1473571bfdb8edc8ccfa8f3f1a471fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375006"
---
# <a name="mci_load_parms-structure"></a>Struttura MCI \_ LOAD \_ PARMS

La **struttura MCI \_ LOAD \_ PARMS** contiene il nome file da caricare per il [**comando MCI \_ LOAD.**](mci-load.md)

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
} MCI_LOAD_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola più bassa specifica un handle di finestra utilizzato per il flag MCI \_ NOTIFY.

</dd> <dt>

**lpfilename**
</dt> <dd>

Nome del file da caricare.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della [**funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**Strutture MCI**](mci-structures.md)
</dt> <dt>

[**MCI \_ LOAD**](mci-load.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

