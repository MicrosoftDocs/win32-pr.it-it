---
title: MCI_WAVE_DELETE_PARMS struttura (Mciapi.h)
description: La struttura MCI WAVE DELETE PARMS contiene informazioni sulla posizione per \_ \_ il comando \_ MCI DELETE per i dispositivi \_ waveform-audio.
ms.assetid: 5c0bf0ca-773b-4b96-8b55-9ef7b5a306d9
keywords:
- MCI_WAVE_DELETE_PARMS struttura Windows Multimediali
topic_type:
- apiref
api_name:
- MCI_WAVE_DELETE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11633a1b6b3876f0382669856cf5971767be325906b270c4d42417e8d3f9b51d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783830"
---
# <a name="mci_wave_delete_parms-structure"></a>Struttura MCI \_ WAVE \_ DELETE \_ PARMS

La **struttura MCI \_ WAVE DELETE \_ \_ PARMS** contiene informazioni sulla posizione per il [**comando MCI \_ DELETE**](mci-delete.md) per i dispositivi waveform-audio.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_WAVE_DELETE_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola di ordine basso specifica un handle di finestra usato per il flag MCI \_ NOTIFY.

</dd> <dt>

**dwFrom**
</dt> <dd>

Posizione da cui eseguire l'eliminazione.

</dd> <dt>

**dwTo**
</dt> <dd>

Posizione in cui eliminare.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel *parametro fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.

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

[**MCI \_ DELETE**](mci-delete.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

