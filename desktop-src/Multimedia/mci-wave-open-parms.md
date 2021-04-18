---
title: Struttura MCI_WAVE_OPEN_PARMS (Mciapi. h)
description: La \_ \_ \_ struttura parametri Wave Open di MCI contiene informazioni per il \_ comando di apertura di MCI per i dispositivi audio waveform.
ms.assetid: 2fc9383e-4610-4751-acad-b545dc6d8992
keywords:
- Struttura MCI_WAVE_OPEN_PARMS di Windows Multimedia
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
ms.openlocfilehash: b5a4107c6283edab1ffeaf18297e2898a8b17761
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302028"
---
# <a name="mci_wave_open_parms-structure"></a>\_ \_ Struttura parametri Wave Open di MCI \_

La **struttura \_ \_ \_ parametri Wave Open di MCI** contiene informazioni per il comando di [**\_ apertura di MCI**](mci-open.md) per i dispositivi audio waveform.

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

La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.

</dd> <dt>

**wDeviceID**
</dt> <dd>

Identificatore restituito all'applicazione.

</dd> <dt>

**lpstrDeviceType**
</dt> <dd>

Nome o identificatore costante del tipo di dispositivo. Il nome del dispositivo viene in genere ottenuto dal registro di sistema o dal file di SYSTEM.INI. Questo membro può essere uno dei valori elencati in [tipi di dispositivo MCI](mci-device-types.md).

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

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.

Se non si usano i membri dati estesi, è possibile usare la struttura [**\_ \_ parametri Open**](mci-open-parms.md) di MCI invece di **MCI \_ Wave \_ Open \_ parametri** .

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

[**\_aperto MCI**](mci-open.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[**\_parametri aperto \_ MCI**](mci-open-parms.md)
</dt> </dl>

 

