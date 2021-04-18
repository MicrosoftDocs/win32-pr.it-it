---
description: Il \_ messaggio Creazione linea TAPI viene inviato per informare l'applicazione della creazione di un nuovo dispositivo a linee.
ms.assetid: d4735eab-392f-49d9-a1d9-5895d9232624
title: Messaggio di LINE_CREATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9973849c3942b5427dfb6b3fe7c47bc4d2a716
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328127"
---
# <a name="line_create-message"></a>\_Creazione riga messaggio

Il messaggio **\_ creazione linea** TAPI viene inviato per informare l'applicazione della creazione di un nuovo dispositivo a linee.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
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

Le applicazioni meno recenti (che hanno negoziato TAPI versione 1,3) ricevono un messaggio di [**riga \_ LINEDEVSTATE**](line-linedevstate.md) che specifica LINEDEVSTATE \_ reinit, per cui è necessario arrestare l'uso dell'API e chiamare di nuovo [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) per ottenere il nuovo numero di dispositivi. Diversamente dalle versioni precedenti di TAPI, tuttavia, questa versione non richiede l'arresto di tutte le applicazioni prima di consentire la reinizializzazione delle applicazioni. la reinizializzazione può avvenire immediatamente quando viene creato un nuovo dispositivo. l'arresto completo è ancora necessario quando un provider di servizi viene rimosso dal sistema.

Le applicazioni che supportano TAPI 1,4 o versione successiva vengono inviate un messaggio di **\_ creazione riga** . In questo modo vengono segnalati l'esistenza del nuovo dispositivo e il nuovo identificatore del dispositivo. L'applicazione può quindi scegliere se provare a usare il nuovo dispositivo per lo svago. Questo messaggio viene inviato a tutte le applicazioni che supportano questa o le versioni successive dell'API che hanno chiamato [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) o [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), inclusi quelli che non hanno dispositivi linea aperti al momento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINEA \_ LINEDEVSTATE**](line-linedevstate.md)
</dt> <dt>

[**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




