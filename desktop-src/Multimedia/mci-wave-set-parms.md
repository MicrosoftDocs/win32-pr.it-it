---
title: Struttura MCI_WAVE_SET_PARMS (Mciapi. h)
description: La \_ struttura parametri di MCI WAVE \_ set \_ contiene informazioni per il \_ comando set di MCI per i dispositivi Waveform-Audio.
ms.assetid: 24c26124-274f-457e-ab87-887f3bcffce3
keywords:
- Struttura MCI_WAVE_SET_PARMS di Windows Multimedia
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
ms.openlocfilehash: 11446eda931da1a645b9bb6218c93898862b59bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874454"
---
# <a name="mci_wave_set_parms-structure"></a>\_ \_ Struttura parametri set Wave MCI \_

La struttura **parametri di MCI \_ Wave \_ set \_** contiene informazioni per il comando [**\_ set di MCI**](mci-set.md) per i dispositivi Waveform-Audio.

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

La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.

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

Dispositivo di output da usare. Questo valore, ad esempio, può essere 2 Se un sistema ha due schede audio installate.

</dd> <dt>

**wFormatTag**
</dt> <dd>

Formato dei dati audio della forma d'onda, come il \_ formato Wave \_ PCM. I valori possibili sono definiti in mmreg. h.

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

Campioni al secondo.

</dd> <dt>

**nAvgBytesPerSec**
</dt> <dd>

Frequenza di campionamento in byte al secondo.

</dd> <dt>

**nBlockAlign**
</dt> <dd>

Blocca l'allineamento dei dati.

</dd> <dt>

**wReserved4**
</dt> <dd>

Riservato.

</dd> <dt>

**wBitsPerSample**
</dt> <dd>

BITS per campione.

</dd> <dt>

**wReserved5**
</dt> <dd>

Riservato.

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

[**SET di MCI \_**](mci-set.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

