---
title: MCI_VCR_STATUS_PARMS struttura (Vcr.h)
description: La struttura MCI VCR STATUS PARMS contiene i parametri per \_ \_ il comando \_ MCI STATUS per i \_ registratori di videocassette.
ms.assetid: 5d7cbb64-a81d-4bdd-8f07-8c20dd7b9ef5
keywords:
- MCI_VCR_STATUS_PARMS struttura Windows Multimediali
topic_type:
- apiref
api_name:
- MCI_VCR_STATUS_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8569a278f697ed816085c4fc8f313502d2994215519fb2452f82e63ce31a80cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783921"
---
# <a name="mci_vcr_status_parms-structure"></a>Struttura \_ PARMS DI \_ STATO DEL \_ VCR MCI

La **struttura MCI \_ VCR STATUS \_ \_ PARMS** contiene i parametri per il [**comando MCI \_ STATUS**](mci-status.md) per i registratori di videocassette.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMCI_VCR_STATUS_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
  DWORD     dwNumber;
} MCI_VCR_STATUS_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola di ordine basso specifica un handle di finestra usato per il flag MCI \_ NOTIFY.

</dd> <dt>

**dwReturn**
</dt> <dd>

Valore restituito dal [**comando MCI \_ STATUS.**](mci-status.md) Il valore restituito varia in base alla richiesta del comando. Per altre informazioni, vedere la descrizione del [**comando MCI \_ STATUS.**](mci-status-parms.md)

</dd> <dt>

**dwItem**
</dt> <dd>

Tipo di informazioni richieste.

</dd> <dt>

**dwTrack**
</dt> <dd>

Traccia audio o video che archivierà le informazioni durante la registrazione successiva. Questo membro viene usato per restituire informazioni quando il [**comando MCI \_ STATUS**](mci-status-parms.md) esegue una richiesta sullo stato della registrazione video o audio.

</dd> <dt>

**dwNumber**
</dt> <dd>

Siner logico a cui è associato il canale corrente. Questo membro viene usato per restituire informazioni quando il [**comando MCI \_ STATUS**](mci-status.md) esegue una richiesta sul numero di canale corrente.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel *parametro fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.

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

[**STATO \_ MCI**](mci-status.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

