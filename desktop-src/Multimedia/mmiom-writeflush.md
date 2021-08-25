---
title: MMIOM_WRITEFLUSH messaggio (Mmsystem.h)
description: Il messaggio MMIOM WRITEFLUSH viene inviato a una procedura di I/O dalla funzione mmioWrite per richiedere che i dati siano scritti in un file aperto e che tutti i buffer interni usati dalla procedura di I/O siano scaricati \_ su disco.
ms.assetid: e04acaef-9584-410c-a020-af09fb888490
keywords:
- MMIOM_WRITEFLUSH messaggio Windows Multimediali
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
ms.openlocfilehash: b274536e934f426ef5e545e758c2f7bf918d552c42085650fc7c81a6a47c842e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807091"
---
# <a name="mmiom_writeflush-message"></a>Messaggio WRITEFLUSH MMIOM \_

Il **messaggio MMIOM \_ WRITEFLUSH** viene inviato a una procedura di I/O dalla funzione [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) per richiedere che i dati siano scritti in un file aperto e che tutti i buffer interni usati dalla procedura di I/O siano scaricati su disco.


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

Questo messaggio equivale al messaggio [**MMIOM \_ WRITE,**](mmiom-write.md) ad eccezione del fatto che richiede che la procedura di I/O scarica i buffer interni, se presenti. A meno che una procedura di I/O non esegua la memorizzazione nel buffer interno, questo messaggio può essere gestito esattamente come il **messaggio MMIOM \_ WRITE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h (includere Windows.h)</dt> </dl> |



 

