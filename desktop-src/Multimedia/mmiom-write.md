---
title: Messaggio MMIOM_WRITE (mmsystem. h)
description: Il \_ messaggio di scrittura MMIOM viene inviato a una routine di i/O dalla funzione mmioWrite per richiedere che i dati vengano scritti in un file aperto.
ms.assetid: 46e2dd9a-c4a7-4c99-86e4-a67b424411d1
keywords:
- MMIOM_WRITE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MMIOM_WRITE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27cf96827f803608c369cc9022faa6235add9ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964837"
---
# <a name="mmiom_write-message"></a>MMIOM \_ Scrivi messaggio

Il messaggio di **\_ scrittura MMIOM** viene inviato a una routine di i/O dalla funzione [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) per richiedere che i dati vengano scritti in un file aperto.


```C++
MMIOM_WRITE 
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

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



 

