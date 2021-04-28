---
description: "CPL_INQUIRE messaggio: inviato alla funzione CPlApplet di un'applicazione Pannello di controllo per richiedere informazioni su una finestra di dialogo che l'applicazione supporta."
title: CPL_INQUIRE messaggio (Cpl.h)
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
ms.openlocfilehash: f9962ff94e8bf80041d7b61ecf97220d573131fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104469"
---
# <a name="cpl_inquire-message"></a>Messaggio \_ CPL INQUIRE

Inviato alla [**funzione CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) di un'Pannello di controllo per richiedere informazioni su una finestra di dialogo che l'applicazione supporta.

## <a name="parameters"></a>Parametri

<dl> <dt>

*uAppNum* 
</dt> <dd>

Numero della finestra di dialogo. Questo numero deve essere compreso nell'intervallo compreso tra zero e uno minore del valore restituito in risposta al messaggio [**\_ GETCOUNT CPL**](cpl-getcount.md) (CPL \_ GETCOUNT – 1).

</dd> <dt>

*lpcpli* 
</dt> <dd>

Indirizzo di una [**struttura CPLINFO.**](/windows/win32/api/cpl/ns-cpl-cplinfo) L'applicazione deve riempire questa struttura con identificatori di risorsa per l'icona, il nome breve, la descrizione e qualsiasi valore definito dall'utente associato alla finestra di dialogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la [**funzione CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) elabora correttamente questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Il Pannello di controllo invia il messaggio **CPL \_ INQUIRE** una volta per ogni finestra di dialogo supportata dall'applicazione. Il Pannello di controllo invia anche un [**messaggio CPL \_ NEWINQUIRE**](cpl-newinquire.md) per ogni finestra di dialogo. Questi messaggi vengono inviati immediatamente dopo il [**messaggio \_ GETCOUNT CPL.**](cpl-getcount.md) Tuttavia, il sistema non garantisce l'ordine in cui vengono inviati i messaggi **CPL \_ INQUIRE** e **CPL \_ NEWINQUIRE.**

È possibile eseguire l'inizializzazione per la finestra di dialogo quando si riceve **CPL \_ INQUIRE**. Se è necessario allocare memoria, eseguire questa operazione in risposta al messaggio [**\_ CPL INIT.**](cpl-init.md)

Il [**messaggio CPL \_ NEWINQUIRE**](cpl-newinquire.md) restituisce informazioni in un formato che il sistema non può memorizzare nella cache. Per questo motivo, la maggior [**parte delle funzioni CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) deve elaborare **CPL \_ INQUIRE** e ignorare **CPL \_ NEWINQUIRE**.

Le uniche applicazioni che devono usare [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) sono quelle che devono modificare l'icona o visualizzare le stringhe in base allo stato del computer. In questo caso, il gestore **CPL \_ INQUIRE** deve specificare il valore CPL DYNAMIC RES per i membri \_ \_ **idIcon**, **idName** o **idInfo** della struttura [**CPLINFO,**](/windows/win32/api/cpl/ns-cpl-cplinfo) anziché specificare un identificatore di risorsa valido. In questo modo il Pannello di controllo invia il messaggio **CPL \_ NEWINQUIRE** ogni volta che sono necessarie l'icona e le stringhe di visualizzazione, consentendo di specificare le informazioni in base allo stato corrente del computer. Questa operazione è notevolmente più lenta rispetto all'uso di informazioni memorizzate nella cache.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows XP \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Cpl.h</dt> </dl> |



 

 
