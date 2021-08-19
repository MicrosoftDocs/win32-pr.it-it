---
title: MCI_WAVE_OPEN_PARMS struttura (Mciapi.h)
description: La struttura MCI WAVE OPEN PARMS contiene informazioni per \_ il comando \_ \_ MCI OPEN per i dispositivi \_ waveform-audio.
ms.assetid: 2fc9383e-4610-4751-acad-b545dc6d8992
keywords:
- MCI_WAVE_OPEN_PARMS struttura Windows Multimediali
topic_type:
- apiref
api_name:
- MCI_WAVE_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 470b00bc818fb184174f27a8ff281359788f235ec7e31b899b051dc90423426c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783785"
---
# <a name="mci_wave_open_parms-structure"></a>Struttura MCI \_ WAVE \_ OPEN \_ PARMS

La **struttura MCI \_ WAVE OPEN \_ \_ PARMS** contiene informazioni per [**il comando MCI \_ OPEN**](mci-open.md) per i dispositivi waveform-audio.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwBufferSeconds;
} MCI_WAVE_OPEN_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola di ordine basso specifica un handle di finestra usato per il flag MCI \_ NOTIFY.

</dd> <dt>

**wDeviceID**
</dt> <dd>

Rientro restituito all'applicazione.

</dd> <dt>

**lpstrDeviceType**
</dt> <dd>

Nome o identificatore costante del tipo di dispositivo. Il nome del dispositivo viene in genere ottenuto dal registro o dal SYSTEM.INI file. Questo membro può essere uno dei valori elencati in [Tipi di dispositivo MCI.](mci-device-types.md)

</dd> <dt>

**lpstrElementName**
</dt> <dd>

Nome dell'elemento del dispositivo (in genere un percorso).

</dd> <dt>

**lpstrAlias**
</dt> <dd>

Alias del dispositivo facoltativo.

</dd> <dt>

**dwBufferSeconds**
</dt> <dd>

Lunghezza del buffer, in secondi.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel *parametro fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.

Se non si usano i membri dati estesi, è possibile usare la struttura [**MCI \_ OPEN \_ PARMS**](mci-open-parms.md) anziché **MCI \_ WAVE OPEN \_ \_ PARMS.**

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

[**MCI \_ OPEN**](mci-open.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[**MCI \_ OPEN \_ PARMS**](mci-open-parms.md)
</dt> </dl>

 

