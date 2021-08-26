---
title: MCI_BREAK_PARMS struttura (Mciapi.h)
description: La struttura MCI BREAK PARMS contiene il codice della chiave virtuale e \_ le informazioni sulla finestra per il comando \_ MCI \_ BREAK.
ms.assetid: c8df8c55-cc6b-4dd7-b275-784d3eb9dce1
keywords:
- MCI_BREAK_PARMS struttura Windows Multimediali
topic_type:
- apiref
api_name:
- MCI_BREAK_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efaff8841e0e8ef0387535aa8d42723cf9477887511b7111f02a6ee0cb2b527b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039511"
---
# <a name="mci_break_parms-structure"></a>Struttura MCI \_ BREAK \_ PARMS

La **struttura MCI \_ BREAK \_ PARMS** contiene il codice della chiave virtuale e le informazioni sulla finestra per il [**comando MCI \_ BREAK.**](mci-break.md)

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD_PTR dwCallback;
  int       nVirtKey;
  HWND      hwndBreak;
} MCI_BREAK_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola di ordine basso specifica un handle di finestra usato per il flag MCI \_ NOTIFY.

</dd> <dt>

**nVirtKey**
</dt> <dd>

Codice della chiave virtuale per la chiave di interruzione.

</dd> <dt>

**hwndBreak**
</dt> <dd>

Handle per la finestra che deve essere la finestra corrente per il rilevamento delle interruzioni.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel *parametro fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri. Sono definiti i flag seguenti:

MCI \_ BREAK \_ HWND

Convalida il **membro hwndBreak** specificando la finestra che deve avere lo stato attivo per abilitare il rilevamento delle interruzioni.

TASTO DI \_ INTERRUZIONE \_ MCI

Convalida il **membro nVirtKey** che specifica il codice della chiave virtuale da usare per la chiave di interruzione.

INTERRUZIONE \_ MCI \_

Disabilita qualsiasi tasto di interruzione esistente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**Strutture MCI**](mci-structures.md)
</dt> <dt>

[**INTERRUZIONE \_ MCI**](mci-break.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

