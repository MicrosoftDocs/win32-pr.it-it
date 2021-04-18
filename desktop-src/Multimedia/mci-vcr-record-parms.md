---
title: Struttura MCI_VCR_RECORD_PARMS (VCR. h)
description: La \_ \_ struttura parametri del record MCI VCR \_ contiene i parametri per il \_ comando MCI record per i registratori di nastri video.
ms.assetid: a95a6dab-9854-4c44-989a-032dff680106
keywords:
- Struttura MCI_VCR_RECORD_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_RECORD_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4089b6b7977959b5eb0d0ac60dd4e612b17b823d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301374"
---
# <a name="mci_vcr_record_parms-structure"></a>\_ \_ Struttura parametri del record VCR MCI \_

La **struttura \_ \_ \_ parametri del record MCI VCR** contiene i parametri per il comando [**MCI \_ record**](mci-record.md) per i registratori di nastri video.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMCI_VCR_RECORD_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_RECORD_PARMS;
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

Valore di ora che influiscono sul comando [**MCI \_ record**](mci-record.md) o [**MCI \_ cue**](mci-cue.md) . Per **il \_ record MCI**, questo è il momento in cui inizia la registrazione. Per **MCI \_ cue**, questo è il momento in cui il dispositivo di cui è stato caricato il carico raggiunge la posizione specificata in **dwFrom**.

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

[**\_record MCI**](mci-record.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

