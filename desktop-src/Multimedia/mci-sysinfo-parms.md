---
title: Struttura MCI_SYSINFO_PARMS (Mciapi. h)
description: La \_ \_ struttura parametri di MCI sysinfo contiene informazioni per il \_ comando MCI sysinfo.
ms.assetid: 433649ed-7c00-440d-84f3-164949e01cc4
keywords:
- Struttura MCI_SYSINFO_PARMS di Windows Multimedia
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
ms.openlocfilehash: bf143bb0d895dc03df38bbb0a657467d506eac77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300958"
---
# <a name="mci_sysinfo_parms-structure"></a>\_ \_ Struttura parametri di MCI sysinfo

La **struttura \_ \_ parametri di MCI sysinfo** contiene informazioni per il comando [**MCI \_ sysinfo**](mci-sysinfo.md) .

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

La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.

</dd> <dt>

**lpstrReturn**
</dt> <dd>

Puntatore a un buffer fornito dall'utente per la stringa restituita. Viene inoltre utilizzato per restituire un valore **DWORD** quando \_ viene utilizzato il flag di quantità di MCI sysinfo \_ .

</dd> <dt>

**dwRetSize**
</dt> <dd>

Dimensione, in byte, del buffer restituito.

</dd> <dt>

**dwNumber**
</dt> <dd>

Numero che indica la posizione del dispositivo nella tabella del dispositivo MCI o nell'elenco di dispositivi aperti se \_ è impostato il flag di apertura di MCI sysinfo \_ .

</dd> <dt>

**wDeviceType**
</dt> <dd>

Tipo di dispositivo. Questo membro può essere uno dei valori elencati in [tipi di dispositivo MCI](mci-device-types.md).

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

[**\_sysinfo MCI**](mci-sysinfo.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

