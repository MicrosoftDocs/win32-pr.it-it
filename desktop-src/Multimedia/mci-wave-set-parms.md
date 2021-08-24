---
title: MCI_WAVE_SET_PARMS struttura (Mciapi.h)
description: La struttura MCI \_ WAVE \_ SET \_ PARMS contiene informazioni per il comando MCI \_ SET per i dispositivi audio waveform.
ms.assetid: 24c26124-274f-457e-ab87-887f3bcffce3
keywords:
- MCI_WAVE_SET_PARMS struttura Windows Multimediali
topic_type:
- apiref
api_name:
- MCI_WAVE_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85508ec493ecdc38825b90877e608683fe6c0bb7c099365c187a434890c605d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783751"
---
# <a name="mci_wave_set_parms-structure"></a>Struttura MCI \_ WAVE \_ SET \_ PARMS

La **struttura MCI \_ WAVE SET \_ \_ PARMS** contiene informazioni per il [**comando MCI \_ SET**](mci-set.md) per i dispositivi audio waveform.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  UINT      wInput;
  UINT      wOutput;
  WORD      wFormatTag;
  WORD      wReserved2;
  WORD      nChannels;
  WORD      wReserved3;
  DWORD     nSamplesPerSec;
  DWORD     nAvgBytesPerSec;
  WORD      nBlockAlign;
  WORD      wReserved4;
  WORD      wBitsPerSample;
  WORD      wReserved5;
} MCI_WAVE_SET_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola più bassa specifica un handle di finestra utilizzato per il flag MCI \_ NOTIFY.

</dd> <dt>

**dwTimeFormat**
</dt> <dd>

Formato dell'ora del dispositivo.

</dd> <dt>

**dwAudio**
</dt> <dd>

Numero di canale per l'output audio. Usato in genere quando si attiva o disattiva un canale.

</dd> <dt>

**wInput**
</dt> <dd>

Canale di input audio.

</dd> <dt>

**wOutput**
</dt> <dd>

Dispositivo di output da usare. Ad esempio, questo valore potrebbe essere 2 se un sistema aveva due schede audio installate.

</dd> <dt>

**wFormatTag**
</dt> <dd>

Formato dei dati audio della forma d'onda, ad esempio WAVE \_ FORMAT \_ PCM. I valori possibili sono definiti in Mmreg.h.

</dd> <dt>

**wReserved2**
</dt> <dd>

Riservato.

</dd> <dt>

**nChannels**
</dt> <dd>

Mono (1) o stereo (2).

</dd> <dt>

**wReserved3**
</dt> <dd>

Riservato.

</dd> <dt>

**nSamplesPerSec**
</dt> <dd>

Esempi al secondo.

</dd> <dt>

**nAvgBytesPerSec**
</dt> <dd>

Frequenza di campionamento in byte al secondo.

</dd> <dt>

**nBlockAlign**
</dt> <dd>

Allineamento dei blocchi dei dati.

</dd> <dt>

**wReserved4**
</dt> <dd>

Riservato.

</dd> <dt>

**wBitsPerSample**
</dt> <dd>

Bit per campione.

</dd> <dt>

**wReserved5**
</dt> <dd>

Riservato.

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

[**MCI \_ SET**](mci-set.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

