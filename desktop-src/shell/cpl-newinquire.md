---
description: Inviato alla funzione CPlApplet di un'applicazione del pannello di controllo per richiedere informazioni su una finestra di dialogo supportata dall'applicazione.
title: Messaggio CPL_NEWINQUIRE (cpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: af52889c-7180-4690-8ed1-a0eb0a9dff35
api_name:
- CPL_NEWINQUIRE
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 72992d4ea867bc091c29feaa99cc1a22c2a02b2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977346"
---
# <a name="cpl_newinquire-message"></a>\_Messaggio NEWINQUIRE cpl

Inviato alla funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) di un'applicazione del pannello di controllo per richiedere informazioni su una finestra di dialogo supportata dall'applicazione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*uAppNum* 
</dt> <dd>

Numero della finestra di dialogo. Questo numero deve essere compreso tra zero e uno minore del valore restituito in risposta al messaggio [**cpl \_ GetCount**](cpl-getcount.md) (cpl \_ GetCount-1).

</dd> <dt>

*lpncpli* 
</dt> <dd>

Indirizzo di una struttura [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) . L'applicazione del pannello di controllo deve riempire questa struttura con le informazioni sulla finestra di dialogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) elabora correttamente questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Per ottenere prestazioni ottimali, la maggior parte delle applicazioni deve ignorare **cpl \_ NEWINQUIRE** ed elaborare invece il messaggio [**cpl \_ Inquirer**](cpl-inquire.md) .

Il pannello di controllo Invia il messaggio **\_ NEWINQUIRE cpl** una volta per ogni finestra di dialogo supportata dall'applicazione. Il pannello di controllo Invia anche un messaggio di [**\_ richiesta cpl**](cpl-inquire.md) per ogni finestra di dialogo. Questi messaggi vengono inviati immediatamente dopo il messaggio [**cpl \_ GetCount**](cpl-getcount.md) . Tuttavia, il sistema non garantisce l'ordine in cui vengono inviati i messaggi **cpl \_ Inquirer** e **cpl \_ NEWINQUIRE** .

È possibile eseguire l'inizializzazione per la finestra di dialogo quando si riceve la [**\_ richiesta di cpl**](cpl-inquire.md). Se è necessario allocare memoria, eseguire questa operazione in risposta al messaggio [**cpl \_ init**](cpl-init.md) .

[**Cpl \_ DOMANDi**](cpl-inquire.md) è il messaggio preferito. Questo perché **cpl \_ NEWINQUIRE** restituisce informazioni in un modulo che il sistema non è in grado di memorizzare nella cache. Di conseguenza, le applicazioni che elaborano **cpl \_ NEWINQUIRE** devono essere caricate ogni volta che il pannello di controllo necessita di informazioni, causando una riduzione significativa delle prestazioni.

Le uniche applicazioni che devono usare **cpl \_ NEWINQUIRE** sono quelle che devono modificare l'icona o visualizzare le stringhe in base allo stato del computer. In questo caso, il gestore delle [**\_ richieste cpl**](cpl-inquire.md) deve specificare il \_ \_ valore res dinamico cpl per i membri **idIcon**, **idName** o **idInfo** della struttura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) , anziché specificare un identificatore di risorsa valido. In questo modo, il pannello di controllo invierà il messaggio **cpl \_ NEWINQUIRE** ogni volta che è necessaria l'icona e le stringhe di visualizzazione, consentendo di specificare le informazioni in base allo stato corrente del computer. Naturalmente, questo è molto più lento rispetto all'uso delle informazioni memorizzate nella cache.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                      |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Cpl. h</dt> </dl> |



 

 
