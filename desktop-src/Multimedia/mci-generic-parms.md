---
title: Struttura MCI_GENERIC_PARMS (Mciapi. h)
description: La \_ struttura parametri generica MCI \_ contiene l'handle della finestra che riceve i messaggi di notifica. Questa struttura viene utilizzata per i messaggi di comando MCI con elenchi di parametri vuoti.
ms.assetid: 706e406c-d263-4347-932c-e5f125acfe0f
keywords:
- Struttura MCI_GENERIC_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_GENERIC_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1f96482ed5ec7e27253f234031cd099600bf1b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476229"
---
# <a name="mci_generic_parms-structure"></a>\_Struttura parametri generica MCI \_

La **struttura \_ \_ parametri generica MCI** contiene l'handle della finestra che riceve i messaggi di notifica. Questa struttura viene utilizzata per i messaggi di comando MCI con elenchi di parametri vuoti.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD_PTR dwCallback;
} MCI_GENERIC_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le **strutture \_ \_ parametri** di MCI Close e **MCI \_ realizzano \_ parametri** sono identiche alla struttura **\_ \_ parametri generica MCI** .

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.

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

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

