---
description: Il messaggio del pulsante del telefono TAPI \_ viene inviato per notificare all'applicazione che il pulsante di monitoraggio è abilitato se è stato rilevato un pulsante premuto sul telefono locale.
ms.assetid: fe47eed7-89d1-488b-b945-9e1aedc1f63c
title: Messaggio di PHONE_BUTTON (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da810630a937f8415e070373f359dca06a694e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329211"
---
# <a name="phone_button-message"></a>\_Messaggio del pulsante telefonico

Il messaggio **del \_ pulsante del telefono** TAPI viene inviato per notificare all'applicazione che il pulsante di monitoraggio è abilitato se è stato rilevato un pulsante premuto sul telefono locale.


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

Identificatore pulsante/Lamp del pulsante premuto. Si noti che gli identificatori di pulsante da zero a 11 sono sempre i pulsanti del TASTIERino, con ' 0' come identificatore del pulsante zero,' 1' è l'identificatore del pulsante 1 (e così via tramite l'identificatore del pulsante 9) e con '' è l'identificatore del \* pulsante 10 è \# ' è l'identificatore del pulsante 11. Altre informazioni su un identificatore di pulsante sono disponibili con [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) e [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Modalità del pulsante. Questo parametro usa una delle [**\_ costanti PHONEBUTTONMODE**](phonebuttonmode--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Specifica se si tratta di un evento di un pulsante o di un pulsante. Questo parametro usa una delle [**\_ costanti PHONEBUTTONSTATE**](phonebuttonstate--constants.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Un messaggio di un **\_ pulsante telefonico** viene inviato ogni volta che viene modificato lo stato di un pulsante. A un'applicazione viene garantito che per ogni evento button down viene inviato un evento Button up corrispondente. Un provider di servizi che non è in grado di rilevare il pulsante effettivo attivo è necessario per generare il messaggio di riattivazione del pulsante subito dopo il messaggio premuto per ogni pressione del pulsante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)
</dt> <dt>

[**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




