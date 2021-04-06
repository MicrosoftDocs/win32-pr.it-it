---
title: Struttura MCI_VCR_SETAUDIO_PARMS (VCR. h)
description: La \_ struttura parametri di MCI VCR \_ contiene i \_ parametri per il \_ comando MCI sefonica per i registratori di nastri video.
ms.assetid: 328d8e63-7ddd-4c9b-85d6-2e56fd802dbc
keywords:
- Struttura MCI_VCR_SETAUDIO_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SETAUDIO_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 143345f494f381054335d2dfec3b0c10222adca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873429"
---
# <a name="mci_vcr_setaudio_parms-structure"></a>\_ \_ Struttura parametri del videoregistratore \_ MCI

La **struttura \_ \_ \_ parametri di MCI VCR** contiene i parametri per il comando [**MCI \_ sefonica**](mci-setaudio.md) per i registratori di nastri video.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMCI_VCR_SETAUDIO_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTrack;
  DWORD     dwTo;
  DWORD     dwNumber;
} MCI_VCR_SETAUDIO_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.

</dd> <dt>

**dwTrack**
</dt> <dd>

Traccia audio.

</dd> <dt>

**dwTo**
</dt> <dd>

Tipo di input o di input monitorato.

</dd> <dt>

**dwNumber**
</dt> <dd>

Input audio (del tipo specificato nel membro **dwTo** ) da usare.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VCR. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Strutture MCI**](mci-structures.md)
</dt> <dt>

[**sefonica MCI \_**](mci-setaudio.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

