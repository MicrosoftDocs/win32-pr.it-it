---
description: Inviato alla funzione CPlApplet di un'applicazione del pannello di controllo per richiedere informazioni su una finestra di dialogo supportata dall'applicazione.
title: Messaggio CPL_INQUIRE (cpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: daca87b7-f1ee-40f4-95d2-3150b595151e
api_name:
- CPL_INQUIRE
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8f4c75a2610dab9e94a97eb7920c9de43cf44efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128463"
---
# <a name="cpl_inquire-message"></a>\_Messaggio di richiesta cpl

Inviato alla funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) di un'applicazione del pannello di controllo per richiedere informazioni su una finestra di dialogo supportata dall'applicazione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*uAppNum* 
</dt> <dd>

Numero della finestra di dialogo. Questo numero deve essere compreso tra zero e uno minore del valore restituito in risposta al messaggio [**cpl \_ GetCount**](cpl-getcount.md) (cpl \_ GetCount-1).

</dd> <dt>

*lpcpli* 
</dt> <dd>

Indirizzo di una struttura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) . L'applicazione deve riempire questa struttura con gli identificatori di risorsa per l'icona, il nome breve, la descrizione e qualsiasi valore definito dall'utente associato alla finestra di dialogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) elabora correttamente questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Il pannello di controllo Invia il messaggio di **\_ richiesta cpl** una volta per ogni finestra di dialogo supportata dall'applicazione. Il pannello di controllo Invia anche un messaggio [**cpl \_ NEWINQUIRE**](cpl-newinquire.md) per ogni finestra di dialogo. Questi messaggi vengono inviati immediatamente dopo il messaggio [**cpl \_ GetCount**](cpl-getcount.md) . Tuttavia, il sistema non garantisce l'ordine in cui vengono inviati i messaggi **cpl \_ Inquirer** e **cpl \_ NEWINQUIRE** .

È possibile eseguire l'inizializzazione per la finestra di dialogo quando si riceve la **\_ richiesta di cpl**. Se è necessario allocare memoria, eseguire questa operazione in risposta al messaggio [**cpl \_ init**](cpl-init.md) .

Il messaggio [**cpl \_ NEWINQUIRE**](cpl-newinquire.md) restituisce informazioni in un modulo che il sistema non è in grado di memorizzare nella cache. Per questo motivo, la maggior parte delle funzioni [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) deve elaborare **cpl \_ Inquirer** e ignorare **cpl \_ NEWINQUIRE**.

Le uniche applicazioni che devono usare [**cpl \_ NEWINQUIRE**](cpl-newinquire.md) sono quelle che devono modificare l'icona o visualizzare le stringhe in base allo stato del computer. In questo caso, il gestore delle **\_ richieste cpl** deve specificare il \_ \_ valore res dinamico cpl per i membri **idIcon**, **idName** o **idInfo** della struttura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) , anziché specificare un identificatore di risorsa valido. In questo modo, il pannello di controllo invierà il messaggio **cpl \_ NEWINQUIRE** ogni volta che è necessaria l'icona e le stringhe di visualizzazione, consentendo di specificare le informazioni in base allo stato corrente del computer. Questa operazione è notevolmente più lenta rispetto all'utilizzo di informazioni memorizzate nella cache.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                      |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Cpl. h</dt> </dl> |



 

 
