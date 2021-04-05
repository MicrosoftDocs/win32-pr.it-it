---
title: Struttura MCI_VCR_SETVIDEO_PARMS (VCR. h)
description: La \_ \_ struttura parametri MCI VCR sevideo \_ contiene i parametri per il \_ comando MCI sevideo per i registratori di nastri video.
ms.assetid: d14b2c9f-6068-4902-8db6-fc081bcd01c0
keywords:
- Struttura MCI_VCR_SETVIDEO_PARMS di Windows Multimedia
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
ms.openlocfilehash: 050e6452b3952a9d15515de01c2ca94a87af2f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874389"
---
# <a name="mci_vcr_setvideo_parms-structure"></a>\_ \_ Struttura parametri VCR VCR video \_

La **struttura \_ parametri MCI VCR \_ sevideo \_** contiene i parametri per il comando [**MCI \_ sevideo**](mci-setvideo.md) per i registratori di nastri video.

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

La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.

</dd> <dt>

**dwTrack**
</dt> <dd>

Rilevamento interessato.

</dd> <dt>

**dwTo**
</dt> <dd>

Tipo di input o di input monitorato.

</dd> <dt>

**dwNumber**
</dt> <dd>

Input video, del tipo specificato nel membro **dwTo** , da usare.

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

[**VIDEO su MCI \_**](mci-setvideo.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

