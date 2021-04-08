---
title: Struttura MCI_LOAD_PARMS (mmsystem. h)
description: La \_ \_ struttura parametri Load MCI contiene il nome file da caricare per il \_ comando MCI Load.
ms.assetid: 371d11cc-44db-496b-b51a-66d7b919b794
keywords:
- Struttura MCI_LOAD_PARMS di Windows Multimedia
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
ms.openlocfilehash: 04697a52eb9f8bb33db6063eb47e791be674f1d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742946"
---
# <a name="mci_load_parms-structure"></a>\_ \_ Struttura parametri Load MCI

La **struttura \_ \_ parametri Load MCI** contiene il nome file da caricare per il comando [**MCI \_ Load**](mci-load.md) .

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

La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.

</dd> <dt>

**lpfilename**
</dt> <dd>

Nome del file da caricare.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Strutture MCI**](mci-structures.md)
</dt> <dt>

[**\_carico MCI**](mci-load.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

