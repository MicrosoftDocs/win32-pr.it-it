---
description: Il messaggio di creazione del telefono TAPI \_ viene inviato per informare le applicazioni della creazione di un nuovo dispositivo telefonico.
ms.assetid: 62895b10-76ce-456e-ad02-e2b7764616a8
title: Messaggio di PHONE_CREATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92dfaad5d4007279f18890021f5cb39c22c4da9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325278"
---
# <a name="phone_create-message"></a>Telefono \_ Creazione messaggio

Il messaggio **di \_ creazione del telefono** TAPI viene inviato per informare le applicazioni della creazione di un nuovo dispositivo telefonico.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPhone* 
</dt> <dd>

Non utilizzato.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Non utilizzato.

</dd> <dt>

*dwParam1* 
</dt> <dd>

*HDeviceID* del dispositivo appena creato.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Non utilizzato.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Non utilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Le applicazioni che hanno negoziato l'API versione 1,3 ricevono un messaggio di [**\_ stato del telefono**](phone-state.md) che specifica PHONESTATE \_ reinit, per cui è necessario arrestare l'uso dell'API e chiamare di nuovo [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize) per ottenere il nuovo numero di dispositivi. Tuttavia, la versione 1,4 e successive di TAPI non richiedono l'arresto di tutte le applicazioni prima di consentire la reinizializzazione delle applicazioni. la reinizializzazione può avvenire immediatamente quando viene creato un nuovo dispositivo.

Le applicazioni che supportano TAPI 1,4 o versioni successive vengono inviate un messaggio di **\_ creazione telefono** . In questo modo vengono segnalati l'esistenza del nuovo dispositivo e il nuovo identificatore del dispositivo. L'applicazione può quindi scegliere se provare a usare il nuovo dispositivo per lo svago.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_stato telefono**](phone-state.md)
</dt> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




