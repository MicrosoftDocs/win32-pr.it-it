---
title: Struttura MCI_GETDEVCAPS_PARMS (Mciapi. h)
description: La \_ struttura GETDEVCAPS \_ parametri di MCI contiene informazioni sulle funzionalità del dispositivo per il \_ comando MCI GETDEVCAPS.
ms.assetid: a7b128c5-2121-49cd-b668-3a8466d49a73
keywords:
- Struttura MCI_GETDEVCAPS_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_GETDEVCAPS_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a981f6fb9f156cecfa1b4b73046b1b3c654b32e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048057"
---
# <a name="mci_getdevcaps_parms-structure"></a>\_Struttura parametri GETDEVCAPS di MCI \_

La **struttura \_ GETDEVCAPS \_ parametri di MCI** contiene informazioni sulle funzionalità del dispositivo per il comando [**MCI \_ GETDEVCAPS**](mci-getdevcaps.md) .

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
} MCI_GETDEVCAPS_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.

</dd> <dt>

**dwReturn**
</dt> <dd>

Contiene informazioni sull'uscita.

</dd> <dt>

**dwItem**
</dt> <dd>

Funzionalità sottoposta a query. Questo membro può essere una delle costanti elencate nel materiale di riferimento per il comando [**MCI \_ GETDEVCAPS**](mci-getdevcaps.md) .

</dd> </dl>

## <a name="remarks"></a>Commenti

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

[**\_GETDEVCAPS MCI**](mci-getdevcaps.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

