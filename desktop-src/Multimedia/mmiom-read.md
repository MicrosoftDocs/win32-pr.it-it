---
title: Messaggio MMIOM_READ (mmsystem. h)
description: Il \_ messaggio di lettura MMIOM viene inviato a una routine di i/O dalla funzione mmioRead per richiedere che un numero specificato di byte venga letto da un file aperto.
ms.assetid: db769a68-f0ac-4a79-931e-6174e438439d
keywords:
- MMIOM_READ messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MMIOM_READ
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5715bf8db51017c16997530256c6dfb83b3b3fc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479373"
---
# <a name="mmiom_read-message"></a>MMIOM \_ leggere il messaggio

Il messaggio di **\_ lettura MMIOM** viene inviato a una routine di i/O dalla funzione [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) per richiedere che un numero specificato di byte venga letto da un file aperto.


```C++
MMIOM_READ 
lParam1 = (LPARAM) lBuffer 
lParam2 = (LPARAM) cbRead 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lBuffer"></span><span id="lbuffer"></span><span id="LBUFFER"></span>*lBuffer*
</dt> <dd>

Puntatore al buffer da riempire con i dati letti dal file.

</dd> <dt>

<span id="cbRead"></span><span id="cbread"></span><span id="CBREAD"></span>*cbRead*
</dt> <dd>

Numero di byte da leggere dal file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di byte effettivamente letti dal file. Se non è possibile leggere altri byte, il valore restituito è 0. Se si verifica un errore, il valore restituito è 1.

## <a name="remarks"></a>Commenti

La procedura di I/O è responsabile dell'aggiornamento del membro **lDiskOffset** della struttura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) in modo da riflettere la nuova posizione del file dopo l'operazione di lettura.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



 

