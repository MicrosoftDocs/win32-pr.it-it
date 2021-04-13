---
title: Struttura MCI_WAVE_DELETE_PARMS (Mciapi. h)
description: La \_ \_ \_ struttura parametri per l'eliminazione di MCI Wave contiene informazioni sulla posizione per il \_ comando MCI Delete per i dispositivi audio waveform.
ms.assetid: 5c0bf0ca-773b-4b96-8b55-9ef7b5a306d9
keywords:
- Struttura MCI_WAVE_DELETE_PARMS di Windows Multimedia
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
ms.openlocfilehash: 286c6443a229da266dae4992687c0e9ead5640bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475683"
---
# <a name="mci_wave_delete_parms-structure"></a>\_ \_ Struttura parametri Delete Wave MCI \_

La **struttura \_ \_ \_ parametri** per l'eliminazione di MCI Wave contiene informazioni sulla posizione per il comando [**MCI \_ Delete**](mci-delete.md) per i dispositivi audio waveform.

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

La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.

</dd> <dt>

**dwFrom**
</dt> <dd>

Posizione da cui eliminare.

</dd> <dt>

**dwTo**
</dt> <dd>

Posizione da eliminare.

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

[**eliminazione di MCI \_**](mci-delete.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

