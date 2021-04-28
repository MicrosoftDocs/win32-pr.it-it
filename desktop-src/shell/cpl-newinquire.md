---
description: "CPL_NEWINQUIRE messaggio: inviato alla funzione CPlApplet di un'applicazione Pannello di controllo per richiedere informazioni su una finestra di dialogo che l'applicazione supporta."
title: CPL_NEWINQUIRE messaggio (Cpl.h)
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
ms.openlocfilehash: 90c5adf31c01fbab1b62aafd0714d165092f4e23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104439"
---
# <a name="cpl_newinquire-message"></a>CPL \_ NEWINQUIRE message

Inviato alla funzione [**CPlApplet di**](/windows/win32/api/cpl/nc-cpl-applet_proc) un'Pannello di controllo per richiedere informazioni su una finestra di dialogo che l'applicazione supporta.

## <a name="parameters"></a>Parametri

<dl> <dt>

*uAppNum* 
</dt> <dd>

Numero della finestra di dialogo. Questo numero deve essere compreso nell'intervallo da zero a uno minore del valore restituito in risposta al messaggio [**\_ GETCOUNT CPL**](cpl-getcount.md) (CPL \_ GETCOUNT – 1).

</dd> <dt>

*lpncpli* 
</dt> <dd>

Indirizzo di una [**struttura NEWCPLINFO.**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) L Pannello di controllo appalto dovrebbe riempire questa struttura con informazioni sulla finestra di dialogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la [**funzione CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) elabora correttamente questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Per ottenere prestazioni migliori, la maggior parte delle applicazioni deve **ignorare CPL \_ NEWINQUIRE** ed elaborare invece il [**messaggio \_ CPL INQUIRE.**](cpl-inquire.md)

Il Pannello di controllo invia il messaggio **CPL \_ NEWINQUIRE** una volta per ogni finestra di dialogo supportata dall'applicazione. Il Pannello di controllo invia anche un [**messaggio CPL \_ INQUIRE**](cpl-inquire.md) per ogni finestra di dialogo. Questi messaggi vengono inviati immediatamente dopo il [**messaggio \_ GETCOUNT CPL.**](cpl-getcount.md) Tuttavia, il sistema non garantisce l'ordine in cui vengono inviati i messaggi **CPL \_ INQUIRE** e **CPL \_ NEWINQUIRE.**

È possibile eseguire l'inizializzazione per la finestra di dialogo quando si riceve [**CPL \_ INQUIRE**](cpl-inquire.md). Se è necessario allocare memoria, eseguire questa operazione in risposta al [**messaggio \_ CPL INIT.**](cpl-init.md)

[**Libreria CPL \_ INQUIRE**](cpl-inquire.md) è il messaggio preferito. Ciò è dovuto al **fatto che CPL \_ NEWINQUIRE restituisce** informazioni in un formato che il sistema non può memorizzare nella cache. Di conseguenza, le applicazioni che elaborano **CPL \_ NEWINQUIRE** devono essere caricate ogni volta che il Pannello di controllo necessita delle informazioni, con conseguente riduzione significativa delle prestazioni.

Le uniche applicazioni che devono usare **CPL \_ NEWINQUIRE** sono quelle che devono modificare l'icona o visualizzare le stringhe in base allo stato del computer. In questo caso, il gestore [**CPL \_ INQUIRE**](cpl-inquire.md) deve specificare il valore CPL DYNAMIC RES per i membri \_ \_ **idIcon**, **idName** o **idInfo** della struttura [**CPLINFO,**](/windows/win32/api/cpl/ns-cpl-cplinfo) anziché specificare un identificatore di risorsa valido. In questo modo il Pannello di controllo invia il messaggio **CPL \_ NEWINQUIRE** ogni volta che sono necessarie l'icona e le stringhe di visualizzazione, consentendo di specificare le informazioni in base allo stato corrente del computer. Naturalmente, questa operazione è notevolmente più lenta rispetto all'uso di informazioni memorizzate nella cache.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows XP \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Cpl.h</dt> </dl> |



 

 
