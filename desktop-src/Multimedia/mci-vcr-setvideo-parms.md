---
title: MCI_VCR_SETVIDEO_PARMS struttura (Vcr.h)
description: La struttura MCI VCR SETVIDEO PARMS contiene i parametri per il \_ \_ comando \_ MCI \_ SETVIDEO per i registratori di videocassette.
ms.assetid: d14b2c9f-6068-4902-8db6-fc081bcd01c0
keywords:
- MCI_VCR_SETVIDEO_PARMS struttura Windows Multimediali
topic_type:
- apiref
api_name:
- MCI_VCR_SETVIDEO_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf260804a6e993ba133ca450a51802a0f43db3aa3d0e557ba684b8a86bcfb7dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784131"
---
# <a name="mci_vcr_setvideo_parms-structure"></a>Struttura MCI \_ VCR \_ SETVIDEO \_ PARMS

La **struttura MCI \_ VCR \_ SETVIDEO \_ PARMS** contiene i parametri per il [**comando MCI \_ SETVIDEO**](mci-setvideo.md) per i registratori di videocassette.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMCI_VCR_SETVIDEO_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTrack;
  DWORD     dwTo;
  DWORD     dwNumber;
} MCI_VCR_SETVIDEO_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola di ordine basso specifica un handle di finestra usato per il flag MCI \_ NOTIFY.

</dd> <dt>

**dwTrack**
</dt> <dd>

Traccia interessata.

</dd> <dt>

**dwTo**
</dt> <dd>

Tipo di input o input monitorato.

</dd> <dt>

**dwNumber**
</dt> <dd>

Input video (del tipo specificato nel membro **dwTo)** da usare.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel *parametro fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vcr.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**Strutture MCI**](mci-structures.md)
</dt> <dt>

[**MCI \_ SETVIDEO**](mci-setvideo.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

