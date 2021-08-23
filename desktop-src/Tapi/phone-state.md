---
description: TAPI invia il messaggio PHONE STATE a un'applicazione ogni volta che cambia lo stato \_ di un dispositivo telefonico.
ms.assetid: 74e74b62-8387-4056-83e6-2350b3da4077
title: PHONE_STATE messaggio (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90003eaa67cb3384b123c62827fcf52bae524b1e20f9f14c2391c46dc89a367c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796761"
---
# <a name="phone_state-message"></a>MESSAGGIO \_ DI STATO DEL TELEFONO

TAPI invia il **messaggio PHONE \_ STATE** a un'applicazione ogni volta che cambia lo stato di un dispositivo telefonico.


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

Stato del telefono modificato. Questo parametro usa una delle [**costanti PHONESTATE \_**](phonestate--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Telefono informazioni dipendenti dallo stato che dettaglino la modifica dello stato. Questo parametro non viene usato se in *dwParam1* sono impostati più flag, perché sono stati modificati più elementi di stato. L'applicazione deve [**richiamare phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) per ottenere un set completo di informazioni.

Se *dwParam1* è PHONESTATE \_ OWNER, *dwParam2* contiene il nuovo numero di proprietari.

Se *dwParam1* è PHONESTATE \_ MONITORS, *dwParam2* contiene il nuovo numero di monitoraggi.

Se *dwParam1* è PHONESTATE \_ LAMP, *dwParam2* contiene l'identificatore pulsante/lamp della lampadina modificata.

Se *dwParam1* è PHONESTATE \_ RINGMODE, *dwParam2 contiene* la nuova modalità anello.

Se *dwParam1 è* PHONESTATE \_ HANDSET, SPEAKER o HEADSET, *dwParam2* contiene la nuova modalità hookswitch del dispositivo hookswitch. Questo parametro usa una delle [**costanti \_ PHONEHOOKSWITCHMODE**](phonehookswitchmode--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Non utilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

**L'invio del messaggio PHONE \_ STATE** all'applicazione può essere controllato e sottoposto a query usando [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) [**e phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages). Per impostazione predefinita, questo messaggio è disabilitato per tutte le modifiche di stato ad eccezione di PHONESTATE \_ REINIT, che non può essere disabilitato. Questo messaggio viene inviato a tutte le applicazioni che hanno un handle al telefono, incluse quelle che hanno chiamato [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) con il *parametro dwPrivileges* impostato su PHONEPRIVILEGE OWNER o \_ PHONEPRIVILEGE \_ MONITOR.

Un **messaggio DI STATO \_ DEL** TELEFONO con un'indicazione Proprietari e/o Monitoraggi viene inviato alle applicazioni che hanno già un handle per il telefono. Ciò può essere il risultato di un'altra applicazione che modifica la proprietà o il monitoraggio del dispositivo telefonico con [**phoneOpen,**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) o [**phoneShutdown.**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CHIUSURA \_ TELEFONO**](phone-close.md)
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

 

 




