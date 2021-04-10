---
title: Struttura MCI_VCR_PLAY_PARMS (VCR. h)
description: La \_ struttura parametri di MCI VCR \_ Play contiene i \_ parametri per il \_ comando MCI Play per i registratori di nastri video.
ms.assetid: e180c203-3113-4fdb-bcf1-ea3e45e646e2
keywords:
- Struttura MCI_VCR_PLAY_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_PLAY_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae15eedc69accc88ef7a58a6d7ad435e872de7ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964328"
---
# <a name="mci_vcr_play_parms-structure"></a>\_ \_ Struttura parametri della riproduzione MCI VCR \_

La struttura **parametri di MCI \_ VCR \_ Play \_** contiene i parametri per il comando [**MCI \_ Play**](mci-play.md) per i registratori di nastri video.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMCI_VCR_PLAY_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_PLAY_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.

</dd> <dt>

**dwFrom**
</dt> <dd>

Posizione da cui riprodurre.

</dd> <dt>

**dwTo**
</dt> <dd>

Posizione in cui eseguire la riproduzione.

</dd> <dt>

**dwAt**
</dt> <dd>

Valore di ora che influiscono sul comando [**MCI \_ Play**](mci-play.md) o [**MCI \_ cue**](mci-cue.md) . Per la riproduzione [**MCI \_**](mci-play-parms.md), questo è il momento in cui inizia la riproduzione. Per **MCI \_ cue**, questo è il momento in cui il dispositivo di cui è stato caricato il carico raggiunge la posizione specificata in **dwFrom**.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le posizioni vengono specificate nel formato ora corrente.

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

[**\_cue MCI**](mci-cue.md)
</dt> <dt>

[**\_riproduzione MCI**](mci-play.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

