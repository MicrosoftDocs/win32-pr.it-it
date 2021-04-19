---
description: Il messaggio di rimozione della riga di TAPI \_ viene inviato per informare un'applicazione della rimozione (eliminazione dal sistema) di un dispositivo a linee.
ms.assetid: 21b912d6-34aa-4ac0-b019-be3c851cc96d
title: Messaggio di LINE_REMOVE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 567ead3ad2941845dd22405f0d8706eca74bfbd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328908"
---
# <a name="line_remove-message"></a>\_Rimuovi riga messaggio

Il messaggio **di \_ rimozione della riga** di TAPI viene inviato per informare un'applicazione della rimozione (eliminazione dal sistema) di un dispositivo a linee. In genere, questo non viene usato per le rimozioni temporanee, ad esempio l'estrazione di dispositivi PCMCIA, ma solo per le rimozioni permanenti in cui il dispositivo non viene più segnalato dal provider di servizi se TAPI è stato reinizializzato.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Riservato. Imposta su zero.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Riservato. Imposta su zero.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificatore del dispositivo a linee che è stato rimosso.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Riservato. Imposta su zero.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Riservato. Imposta su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Le applicazioni che supportano TAPI 2,0 o versioni successive vengono inviate un messaggio di **\_ rimozione riga** . In questo modo si informa che il dispositivo è stato rimosso dal sistema. Il messaggio di **\_ rimozione riga** è preceduto da un messaggio di [**\_ chiusura riga**](line-close.md) su ogni handle di riga, se l'applicazione ha la riga aperta. Questo messaggio viene inviato a tutte le applicazioni che supportano la versione 2,0 o successiva di TAPI che hanno chiamato [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), inclusi quelli che non dispongono di alcun dispositivo di linea aperto al momento.

Alle applicazioni precedenti viene inviato un messaggio di [**riga \_ LINEDEVSTATE**](line-linedevstate.md) che specifica LINEDEVSTATE \_ rimosso, seguito da un \_ messaggio di chiusura riga. Diversamente dal messaggio **di \_ rimozione riga** , tuttavia, queste applicazioni meno recenti possono ricevere questi messaggi solo se la riga è aperta quando viene rimossa. Se la riga non è aperta, l'unica indicazione che indica che il dispositivo è stato rimosso è la ricezione di un \_ errore LINEERR NODEVICE quando tentano di accedere al dispositivo.

Dopo la rimozione di un dispositivo, qualsiasi tentativo di accedere al dispositivo mediante il relativo identificatore del dispositivo restituisce un \_ errore LINEERR nodevice. Dopo che tutte le applicazioni TAPI sono state arrestate in modo che TAPI possa essere riavviato e quando viene reinizializzata la funzione TAPI, il dispositivo rimosso non occupa più un identificatore del dispositivo.

> [!Note]  
> Implementazione: è TAPI che restituisce questo LINEERR \_ NODEVICE; dopo la ricezione di un messaggio di **\_ rimozione riga** da un provider di servizi, non vengono effettuate ulteriori chiamate a tale provider di servizi tramite tale identificatore del dispositivo di linea.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_chiusura riga**](line-close.md)
</dt> <dt>

[**LINEA \_ LINEDEVSTATE**](line-linedevstate.md)
</dt> <dt>

[**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




