---
title: Struttura MCI_VCR_SETTUNER_PARMS (VCR. h)
description: La \_ struttura parametri di MCI VCR \_ setuner \_ contiene i parametri per il \_ comando MCI setuner per i registratori di nastri video.
ms.assetid: 8254b4c0-80bb-44e4-9f51-1d7434d3b08f
keywords:
- Struttura MCI_VCR_SETTUNER_PARMS di Windows Multimedia
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
ms.openlocfilehash: 891ddf3b4b3dcb9532a2431901b0b2b9d84b0e52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741802"
---
# <a name="mci_vcr_settuner_parms-structure"></a>\_ \_ Struttura parametri del videoregistratore MCI \_

La **struttura \_ parametri di MCI VCR \_ setuner \_** contiene i parametri per il comando [**MCI \_ setuner**](mci-settuner.md) per i registratori di nastri video.

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

La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.

</dd> <dt>

**dwChannel**
</dt> <dd>

Nuovo numero di canale.

</dd> <dt>

**dwNumber**
</dt> <dd>

Sintonizzatore logico influire sul comando [**MCI \_ setuner**](mci-settuner.md) .

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

[**\_SEtuner MCI**](mci-settuner.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

