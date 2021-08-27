---
description: Il messaggio TAPI PHONE \_ CREATE viene inviato per informare le applicazioni della creazione di un nuovo dispositivo telefonico.
ms.assetid: 62895b10-76ce-456e-ad02-e2b7764616a8
title: PHONE_CREATE messaggio (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18633ca9f3d45e08c3e2e054d51261dabe6494f42055567a5a68707408f94d5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072911"
---
# <a name="phone_create-message"></a>MESSAGGIO PHONE \_ CREATE

Il messaggio TAPI **PHONE \_ CREATE** viene inviato per informare le applicazioni della creazione di un nuovo dispositivo telefonico.


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

Alle applicazioni che hanno negoziato l'API versione 1.3 viene inviato un messaggio [**PHONE \_ STATE**](phone-state.md) che specifica PHONESTATE REINIT, che richiede di arrestare l'uso dell'API e chiamare \_ nuovamente [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize) per ottenere il nuovo numero di dispositivi. Tuttavia, TAPI versione 1.4 e successive non richiedono l'arresto di tutte le applicazioni prima di consentire la reinizializzazione delle applicazioni. La reinizializzazione può essere verificata immediatamente quando viene creato un nuovo dispositivo.

Alle applicazioni che supportano TAPI versione 1.4 o successiva viene inviato un **messaggio PHONE \_ CREATE.** In questo modo vengono informati dell'esistenza del nuovo dispositivo e del relativo nuovo identificatore di dispositivo. L'applicazione può quindi scegliere se provare o meno a lavorare con il nuovo dispositivo in qualsiasi momento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**STATO \_ TELEFONO**](phone-state.md)
</dt> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




