---
description: Il messaggio TAPI PHONE BUTTON viene inviato per notificare all'applicazione che il monitoraggio della pressione del pulsante è abilitato se è stato rilevato un pulsante \_ premuto sul telefono locale.
ms.assetid: fe47eed7-89d1-488b-b945-9e1aedc1f63c
title: PHONE_BUTTON messaggio (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aec64f754725e5926a8cab1d98b25e4cb379a444bf4208d6e8f3e976dafee82f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073001"
---
# <a name="phone_button-message"></a>MESSAGGIO \_ DEL PULSANTE DI TELEFONO

Il messaggio TAPI **PHONE \_ BUTTON viene** inviato per notificare all'applicazione che il monitoraggio della pressione del pulsante è abilitato se è stato rilevato un pulsante premuto sul telefono locale.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPhone* 
</dt> <dd>

Handle per il dispositivo telefonico.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback dell'applicazione fornita all'apertura del dispositivo telefonico.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificatore del pulsante o della lampadina del pulsante premuto. Si noti che gli identificatori di pulsante da zero a 11 sono sempre i pulsanti KEYPAD, con '0' come identificatore di pulsante zero, '1' come identificatore di pulsante 1 (e così via tramite l'identificatore del pulsante 9) e con ' come identificatore di pulsante 10 e ' come identificatore \* \# di pulsante 11. Altre informazioni sull'identificatore di un pulsante sono disponibili [**con phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) [**e phoneGetButtonInfo.**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)

</dd> <dt>

*dwParam2* 
</dt> <dd>

Modalità del pulsante. Questo parametro usa una delle [**costanti PHONEBUTTONMODE \_**](phonebuttonmode--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Specifica se si tratta di un evento button-down o di un evento button-up. Questo parametro usa una delle [**costanti PHONEBUTTONSTATE \_**](phonebuttonstate--constants.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Un **messaggio PHONE \_ BUTTON** viene inviato ogni volta che lo stato di un pulsante cambia. Un'applicazione garantisce che, per ogni evento button down, alla fine viene inviato un evento button up corrispondente. Un provider di servizi che non è in grado di rilevare l'effettivo pulsante in alto è necessario per generare il messaggio del pulsante in alto subito dopo il messaggio di pressione del pulsante per ogni pressione del pulsante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)
</dt> <dt>

[**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




