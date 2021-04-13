---
title: Messaggio MM_MCISIGNAL (mmsystem. h)
description: Il \_ messaggio mm MCISIGNAL viene inviato a una finestra per notificare a un'applicazione che un dispositivo MCI ha raggiunto una posizione definita in un comando precedente ( \_ segnale MCI).
ms.assetid: 12512d23-9a89-4e38-9ec5-88845766f4f6
keywords:
- MM_MCISIGNAL messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_MCISIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d42d4d39f31b82c7461a5bd8d8561b0da1b6bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400805"
---
# <a name="mm_mcisignal-message"></a>\_Messaggio MCISIGNAL mm

Il messaggio **mm \_ MCISIGNAL** viene inviato a una finestra per notificare a un'applicazione che un dispositivo MCI ha raggiunto una posizione definita in un [**comando precedente (**](signal.md) [**\_ segnale MCI**](mci-signal.md)).


```C++
MM_MCISIGNAL 
wParam = (WPARAM) wID      
lParam = (LONG) lUserParm  
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wID"></span><span id="wid"></span><span id="WID"></span>*wID*
</dt> <dd>

Identificatore del dispositivo che avvia il messaggio del segnale.

</dd> <dt>

<span id="lUserParm"></span><span id="luserparm"></span><span id="LUSERPARM"></span>*lUserParm*
</dt> <dd>

Valore passato nel membro **dwUserParm** della struttura del **\_ \_ \_ parametro Signal DGV di MCI** quando il comando **Signal** ha definito questa funzione di callback. In alternativa, può contenere il valore Position.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Messaggi MCI](mci-messages.md)
</dt> <dt>

[**signal**](signal.md)
</dt> </dl>

 

 





