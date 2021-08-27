---
title: MCI_VCR_SEEK_PARMS struttura (Vcr.h)
description: La struttura MCI VCR SEEK PARMS contiene i parametri \_ \_ per il comando \_ MCI SEEK per i \_ registratori di videocassette.
ms.assetid: 40a9cef0-abdb-4698-b11e-5c3f67ea846b
keywords:
- MCI_VCR_SEEK_PARMS struttura Windows Multimediali
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
ms.openlocfilehash: ee25352925681ef548310d9e009808499ce0a36f80472e50ee2a0daa71ed8dd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038201"
---
# <a name="mci_vcr_seek_parms-structure"></a>Struttura MCI \_ VCR \_ SEEK \_ PARMS

La **struttura MCI \_ VCR SEEK \_ \_ PARMS** contiene i parametri per il [**comando MCI \_ SEEK**](mci-seek.md) per i registratori di videocassette.

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

La parola più bassa specifica un handle di finestra utilizzato per il flag MCI \_ NOTIFY.

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

Le posizioni vengono specificate nel formato di ora corrente.

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

[**MCI \_ SEEK**](mci-seek.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

