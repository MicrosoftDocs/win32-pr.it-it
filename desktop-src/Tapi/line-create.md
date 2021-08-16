---
description: Il messaggio TAPI LINE \_ CREATE viene inviato per informare l'applicazione della creazione di un nuovo dispositivo di linea.
ms.assetid: d4735eab-392f-49d9-a1d9-5895d9232624
title: LINE_CREATE messaggio (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab18245dc151f074588216d272c305c3a4cbd6aaa85c650ec9854710f5b9eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762275"
---
# <a name="line_create-message"></a>Messaggio LINE \_ CREATE

Il messaggio TAPI **LINE \_ CREATE** viene inviato per informare l'applicazione della creazione di un nuovo dispositivo di linea.


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

Alle applicazioni meno recenti (che hanno negoziato TAPI versione 1.3) viene inviato un messaggio [**LINE \_ LINEDEVSTATE**](line-linedevstate.md) che specifica LINEDEVSTATE REINIT, che richiede di arrestare l'uso dell'API e chiamare nuovamente lineInitialize per ottenere il nuovo numero \_ di dispositivi. [](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) A differenza delle versioni precedenti di TAPI, tuttavia, questa versione non richiede l'arresto di tutte le applicazioni prima di consentire la reinizializzazione delle applicazioni. La reinizializzazione può essere completata immediatamente quando viene creato un nuovo dispositivo. L'arresto completo è comunque necessario quando un provider di servizi viene rimosso dal sistema.

Alle applicazioni che supportano TAPI versione 1.4 o successiva viene inviato un **messaggio LINE \_ CREATE.** In questo modo vengono informati dell'esistenza del nuovo dispositivo e del relativo nuovo identificatore di dispositivo. L'applicazione può quindi scegliere se provare o meno a lavorare con il nuovo dispositivo in qualsiasi momento. Questo messaggio viene inviato a tutte le applicazioni che supportano questa o versioni successive dell'API che hanno chiamato [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) o [**lineInitializeEx,**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)incluse quelle che non hanno dispositivi line aperti al momento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINE \_ LINEDEVSTATE**](line-linedevstate.md)
</dt> <dt>

[**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




