---
title: MCI_VCR_SETTUNER_PARMS struttura (Vcr.h)
description: La struttura MCI VCR SETTUNER PARMS contiene i parametri per il \_ \_ comando \_ MCI \_ SETTUNER per i registratori di videocassette.
ms.assetid: 8254b4c0-80bb-44e4-9f51-1d7434d3b08f
keywords:
- MCI_VCR_SETTUNER_PARMS struttura Windows Multimediali
topic_type:
- apiref
api_name:
- MCI_VCR_SETTUNER_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa6d297ae86ad50ee9c7bb19a1f98ef69c77d502f4ccd306394436d07de330d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784173"
---
# <a name="mci_vcr_settuner_parms-structure"></a>Struttura MCI \_ VCR \_ SETTUNER \_ PARMS

La **struttura MCI \_ VCR \_ SETTUNER \_ PARMS** contiene i parametri per il [**comando MCI \_ SETTUNER**](mci-settuner.md) per i registratori di videocassette.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMCI_VCR_SETTUNER_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwChannel;
  DWORD     dwNumber;
} MCI_VCR_SETTUNER_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola più bassa specifica un handle di finestra utilizzato per il flag MCI \_ NOTIFY.

</dd> <dt>

**dwChannel**
</dt> <dd>

Nuovo numero di canale.

</dd> <dt>

**dwNumber**
</dt> <dd>

Sintassi logica su cui [**influisce il comando MCI \_ SETTUNER.**](mci-settuner.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della [**funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.

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

[**MCI \_ SETTUNER**](mci-settuner.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

