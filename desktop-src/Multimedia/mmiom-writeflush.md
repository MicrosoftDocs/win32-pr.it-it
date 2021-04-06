---
title: Messaggio MMIOM_WRITEFLUSH (mmsystem. h)
description: Il \_ messaggio MMIOM WRITEFLUSH viene inviato a una routine di i/o dalla funzione mmioWrite per richiedere che i dati vengano scritti in un file aperto e che i buffer interni utilizzati dalla procedura di i/o vengano scaricati su disco.
ms.assetid: e04acaef-9584-410c-a020-af09fb888490
keywords:
- MMIOM_WRITEFLUSH messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MMIOM_WRITEFLUSH
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b294d4c461970a3304f09088cf63a6564acd50c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743359"
---
# <a name="mmiom_writeflush-message"></a>\_Messaggio MMIOM WRITEFLUSH

Il messaggio **MMIOM \_ WRITEFLUSH** viene inviato a una routine di i/o dalla funzione [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) per richiedere che i dati vengano scritti in un file aperto e che i buffer interni utilizzati dalla procedura di i/o vengano scaricati su disco.


```C++
MMIOM_WRITEFLUSH 
lParam1 = (LPARAM) lpBuffer 
lParam2 = (LPARAM) cbWrite 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*
</dt> <dd>

Puntatore a un buffer contenente i dati da scrivere nel file.

</dd> <dt>

<span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*
</dt> <dd>

Numero di byte da scrivere nel file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di byte effettivamente scritti nel file. Se si verifica un errore, il valore restituito è 1.

## <a name="remarks"></a>Commenti

La procedura di I/O è responsabile dell'aggiornamento del membro **lDiskOffset** della struttura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) in modo da riflettere la nuova posizione del file dopo l'operazione di scrittura.

Questo messaggio è equivalente al messaggio [**di \_ scrittura MMIOM**](mmiom-write.md) con la differenza che richiede che la procedura di i/O scarichi i buffer interni, se presenti. A meno che una routine di I/O esegua il buffering interno, questo messaggio può essere gestito esattamente come il messaggio di **\_ scrittura MMIOM** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



 

