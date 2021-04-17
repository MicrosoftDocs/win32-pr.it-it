---
title: Struttura MCI_VCR_SEEK_PARMS (VCR. h)
description: La \_ struttura parametri di MCI VCR \_ Seek \_ contiene i parametri per il \_ comando di ricerca MCI per i registratori di nastri video.
ms.assetid: 40a9cef0-abdb-4698-b11e-5c3f67ea846b
keywords:
- Struttura MCI_VCR_SEEK_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SEEK_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302011a3e4bf10eb3a81db4a163f94f4322dea98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476006"
---
# <a name="mci_vcr_seek_parms-structure"></a>\_ \_ Struttura parametri di ricerca VCR MCI \_

La struttura **parametri di MCI \_ VCR \_ Seek \_** contiene i parametri per il comando di [**\_ ricerca MCI**](mci-seek.md) per i registratori di nastri video.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMCI_VCR_SEEK_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTo;
  DWORD     dwMark;
  DWORD     dwAt;
} MCI_VCR_SEEK_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.

</dd> <dt>

**dwTo**
</dt> <dd>

Posizione in cui eseguire la ricerca.

</dd> <dt>

**dwMark**
</dt> <dd>

Contrassegno numerato da cercare.

</dd> <dt>

**dwAt**
</dt> <dd>

Ora di inizio della ricerca.

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

[**\_ricerca MCI**](mci-seek.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

