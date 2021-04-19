---
description: TAPI invia il \_ messaggio di stato del telefono a un'applicazione ogni volta che lo stato di un dispositivo telefonico viene modificato.
ms.assetid: 74e74b62-8387-4056-83e6-2350b3da4077
title: Messaggio di PHONE_STATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db52f16d6c377087fd6ccadc5e70b5bb2865da2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324125"
---
# <a name="phone_state-message"></a>\_Messaggio di stato telefono

TAPI invia il messaggio di **\_ stato del telefono** a un'applicazione ogni volta che lo stato di un dispositivo telefonico viene modificato.


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

Stato del telefono che è stato modificato. Questo parametro usa una delle [**\_ costanti PHONESTATE**](phonestate--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Informazioni dipendenti dallo stato del telefono che descrivono in dettaglio la modifica dello stato. Questo parametro non viene utilizzato se più flag sono impostati in *dwParam1*, perché sono stati modificati più elementi di stato. L'applicazione deve richiamare [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) per ottenere un set completo di informazioni.

Se *dwParam1* è PHONESTATE \_ Owner, *dwParam2* contiene il nuovo numero di proprietari.

Se *dwParam1* è PHONESTATE \_ monitoraggi, *dwParam2* contiene il nuovo numero di monitoraggi.

Se *dwParam1* è PHONESTATE \_ Lamp, *dwParam2* contiene l'identificatore del pulsante o della lampada della lampada che è stata modificata.

Se *dwParam1* è PHONESTATE \_ RINGMODE, *dwParam2* contiene la nuova modalità ring.

Se *dwParam1* è PHONESTATE \_ handset, speaker o headset, *dwParam2* contiene la nuova modalità hookswitch del dispositivo hookswitch. Questo parametro usa una delle [**\_ costanti PHONEHOOKSWITCHMODE**](phonehookswitchmode--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Non utilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

L'invio del messaggio di **\_ stato telefonico** all'applicazione può essere controllato e sottoposto a query usando [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) e [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages). Per impostazione predefinita, questo messaggio è disabilitato per tutte le modifiche di stato ad eccezione di PHONESTATE \_ reinit, che non può essere disabilitato. Questo messaggio viene inviato a tutte le applicazioni che dispongono di un handle per il telefono, incluse quelle che hanno chiamato [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) con il parametro *DWPRIVILEGES* impostato su PHONEPRIVILEGE \_ owner o PHONEPRIVILEGE \_ monitor.

Un messaggio di **\_ stato del telefono** con un proprietario e/o un'indicazione relativa ai monitoraggi viene inviato alle applicazioni che dispongono già di un handle per il telefono. Questo può essere il risultato di un'altra applicazione che modifica la proprietà o il monitoraggio del dispositivo telefonico con [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen), [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) o [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_chiusura telefono**](phone-close.md)
</dt> <dt>

[**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose)
</dt> <dt>

[**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> <dt>

[**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)
</dt> <dt>

[**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages)
</dt> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> <dt>

[**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)
</dt> <dt>

[**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages)
</dt> <dt>

[**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)
</dt> </dl>

 

 




