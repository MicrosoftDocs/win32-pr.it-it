---
title: Struttura MCI_BREAK_PARMS (Mciapi. h)
description: La \_ \_ struttura parametri di MCI break contiene il codice della chiave virtuale e le informazioni della finestra per il \_ comando MCI break.
ms.assetid: c8df8c55-cc6b-4dd7-b275-784d3eb9dce1
keywords:
- Struttura MCI_BREAK_PARMS di Windows Multimedia
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
ms.openlocfilehash: e66b52992827b447b6d4b5585ca3f98564142680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517631"
---
# <a name="mci_break_parms-structure"></a>\_ \_ Struttura parametri break MCI

La **struttura \_ \_ parametri di MCI break** contiene il codice della chiave virtuale e le informazioni della finestra per il comando [**MCI \_ break**](mci-break.md) .

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

La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.

</dd> <dt>

**nVirtKey**
</dt> <dd>

Codice di chiave virtuale per la chiave di break.

</dd> <dt>

**hwndBreak**
</dt> <dd>

Handle per la finestra che deve essere la finestra corrente per il rilevamento delle interruzioni.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri. Vengono definiti i flag seguenti:

\_HWND Interrompi MCI \_

Convalida il membro **hwndBreak** specificando la finestra che deve avere lo stato attivo per abilitare il rilevamento delle interruzioni.

\_chiave di pausa MCI \_

Convalida il membro **nVirtKey** specificando il codice della chiave virtuale da usare per la chiave di break.

interruzione di MCI \_ \_

Disabilita qualsiasi chiave di break esistente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Strutture MCI**](mci-structures.md)
</dt> <dt>

[**\_interruzioni MCI**](mci-break.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

