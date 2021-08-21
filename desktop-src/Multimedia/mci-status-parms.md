---
title: MCI_STATUS_PARMS struttura (Mciapi.h)
description: La struttura MCI \_ STATUS \_ PARMS contiene informazioni per il comando MCI \_ STATUS.
ms.assetid: c4897b34-4184-46aa-af17-2127edfbf82d
keywords:
- MCI_STATUS_PARMS struttura Windows Multimediali
topic_type:
- apiref
api_name:
- MCI_STATUS_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2685ec70f10dc8dcecb0149f3bcf1af6c9814dd360e8f7e185d31710c24d5527
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138097"
---
# <a name="mci_status_parms-structure"></a>Struttura \_ PARMS DI STATO MCI \_

La **struttura MCI \_ STATUS \_ PARMS** contiene informazioni per il [**comando MCI \_ STATUS.**](mci-status.md)

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD_PTR dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
} MCI_STATUS_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola di ordine basso specifica un handle di finestra usato per il flag MCI \_ NOTIFY.

</dd> <dt>

**dwReturn**
</dt> <dd>

Contiene informazioni sulla restituzione.

</dd> <dt>

**dwItem**
</dt> <dd>

Funzionalità su cui viene eseguita una query.

</dd> <dt>

**dwTrack**
</dt> <dd>

Lunghezza o numero di tracce.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il flag MCI STATUS ITEM deve essere impostato nel parametro \_ \_ *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare il membro **dwItem,** che deve contenere una delle costanti che indicano le informazioni sullo stato richieste.

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

[**STATO \_ MCI**](mci-status.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

