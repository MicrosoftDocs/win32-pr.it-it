---
title: MCI_VCR_STEP_PARMS struttura (Vcr.h)
description: La struttura MCI VCR STEP PARMS contiene i parametri per \_ \_ il comando \_ MCI STEP per i \_ registratori di videocassette.
ms.assetid: 57751de6-d174-418f-8167-402d3ead4e24
keywords:
- MCI_VCR_STEP_PARMS struttura Windows Multimediali
topic_type:
- apiref
api_name:
- MCI_VCR_STEP_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f25e79903a694b6537e88d1c58994d1f39ccf958ea95f40f571a267239a055e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783831"
---
# <a name="mci_vcr_step_parms-structure"></a>Struttura MCI \_ VCR \_ STEP \_ PARMS

La **struttura MCI \_ VCR STEP \_ \_ PARMS** contiene i parametri per il [**comando MCI \_ STEP**](mci-step.md) per i registratori di videocassette.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMCI_VCR_STEP_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrames;
} MCI_VCR_STEP_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola di ordine basso specifica un handle di finestra usato per il flag MCI \_ NOTIFY.

</dd> <dt>

**dwFrames**
</dt> <dd>

Numero di fotogrammi da saltare (lunghezza di un singolo passaggio) quando il [**comando MCI \_ STEP**](mci-step.md) avanza o indietro nel contenuto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* [**di mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.

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

[**PASSAGGIO \_ MCI**](mci-step.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

