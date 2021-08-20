---
title: MCI_SYSINFO_PARMS struttura (Mciapi.h)
description: La struttura MCI \_ SYSINFO \_ PARMS contiene informazioni per il comando \_ MCI SYSINFO.
ms.assetid: 433649ed-7c00-440d-84f3-164949e01cc4
keywords:
- MCI_SYSINFO_PARMS struttura Windows Multimediali
topic_type:
- apiref
api_name:
- MCI_SYSINFO_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708d37f4d011997352a95b80dc80b8b9afd28730feeeb0e285a07d68c8c8eed5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803131"
---
# <a name="mci_sysinfo_parms-structure"></a>Struttura MCI \_ SYSINFO \_ PARMS

La **struttura MCI \_ SYSINFO \_ PARMS** contiene informazioni per il [**comando \_ MCI SYSINFO.**](mci-sysinfo.md)

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPTSTR    lpstrReturn;
  DWORD     dwRetSize;
  DWORD     dwNumber;
  UINT      wDeviceType;
} MCI_SYSINFO_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola più bassa specifica un handle di finestra utilizzato per il flag MCI \_ NOTIFY.

</dd> <dt>

**lpstrReturn**
</dt> <dd>

Puntatore a un buffer fornito dall'utente per la stringa restituita. Viene inoltre usato per restituire un **valore DWORD** quando viene usato il \_ flag MCI SYSINFO \_ QUANTITY.

</dd> <dt>

**dwRetSize**
</dt> <dd>

Dimensione, in byte, del buffer restituito.

</dd> <dt>

**dwNumber**
</dt> <dd>

Numero che indica la posizione del dispositivo nella tabella dei dispositivi MCI o nell'elenco dei dispositivi aperti se è impostato il \_ flag MCI SYSINFO \_ OPEN.

</dd> <dt>

**wDeviceType**
</dt> <dd>

Tipo di dispositivo. Questo membro può essere uno dei valori elencati in [McI Device Types](mci-device-types.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della [**funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.

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

[**MCI \_ SYSINFO**](mci-sysinfo.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

