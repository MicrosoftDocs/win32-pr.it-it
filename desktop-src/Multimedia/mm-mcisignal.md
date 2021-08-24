---
title: MM_MCISIGNAL messaggio (Mmsystem.h)
description: Il messaggio MM MCISIGNAL viene inviato a una finestra per notificare a un'applicazione che un dispositivo MCI ha raggiunto una posizione definita in un comando di segnale \_ precedente (MCI \_ SIGNAL).
ms.assetid: 12512d23-9a89-4e38-9ec5-88845766f4f6
keywords:
- MM_MCISIGNAL di Windows multimediali
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
ms.openlocfilehash: cb54b56d35ad34d10d95c2a34b52b370fb856d9c958dd42223c7f0a08ddbdfb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807441"
---
# <a name="mm_mcisignal-message"></a>MM \_ MCISIGNAL message

Il **messaggio MM \_ MCISIGNAL** viene inviato a una finestra per notificare a un'applicazione che un dispositivo MCI ha raggiunto una posizione definita in un segnale precedente [**(**](signal.md) [**MCI \_ SIGNAL**](mci-signal.md)).


```C++
MM_MCISIGNAL 
wParam = (WPARAM) wID      
lParam = (LONG) lUserParm  
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wID"></span><span id="wid"></span><span id="WID"></span>*Wid*
</dt> <dd>

Identificatore del dispositivo che avvia il messaggio di segnale.

</dd> <dt>

<span id="lUserParm"></span><span id="luserparm"></span><span id="LUSERPARM"></span>*lUserParm*
</dt> <dd>

Valore passato nel **membro dwUserParm** della struttura **MCI \_ DGV \_ SIGNAL \_ PARAMS** quando il **comando signal** ha definito questa funzione di callback. In alternativa, può contenere il valore della posizione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Messaggi MCI](mci-messages.md)
</dt> <dt>

[**Segnale**](signal.md)
</dt> </dl>

 

 





