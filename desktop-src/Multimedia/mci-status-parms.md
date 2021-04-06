---
title: Struttura MCI_STATUS_PARMS (Mciapi. h)
description: La \_ \_ struttura parametri status MCI contiene informazioni per il \_ comando MCI status.
ms.assetid: c4897b34-4184-46aa-af17-2127edfbf82d
keywords:
- Struttura MCI_STATUS_PARMS di Windows Multimedia
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
ms.openlocfilehash: 8295f2e747752889c10083c6bb794ba2df7ac273
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963875"
---
# <a name="mci_status_parms-structure"></a>\_ \_ Struttura parametri stato MCI

La **struttura \_ \_ parametri status MCI** contiene informazioni per il comando [**MCI \_ status**](mci-status.md) .

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

La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.

</dd> <dt>

**dwReturn**
</dt> <dd>

Contiene informazioni sulla restituzione.

</dd> <dt>

**dwItem**
</dt> <dd>

Funzionalità sottoposta a query.

</dd> <dt>

**dwTrack**
</dt> <dd>

Lunghezza o numero di tracce.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il \_ \_ flag elemento stato MCI deve essere impostato nel parametro *FdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare il membro **dwItem** , che deve contenere una delle costanti che indicano le informazioni sullo stato richieste.

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

[**\_stato MCI**](mci-status.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

