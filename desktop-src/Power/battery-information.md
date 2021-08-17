---
description: Le batterie possono fornire alimentazione per computer portatili e computer in esecuzione su un alimentatore (UPS) ininterrotti.
ms.assetid: 3580b37d-611c-46b4-9300-4943833d6852
title: Informazioni sulla batteria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b1afd2461985ec85a07d40bd309c588a5404e4b59be7555a01fc6c147eb221
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143694"
---
# <a name="battery-information"></a>Informazioni sulla batteria

Le batterie possono fornire alimentazione per computer portatili e computer in esecuzione su un alimentatore (UPS) ininterrotti. In questi computer, il sistema operativo fornisce informazioni sullo stato della batteria in modo che le applicazioni possano fornire funzioni utili per l'utente. Alcuni sistemi di batteria e upS non standard meno recenti non sono supportati.

Si noti che questa panoramica presuppone che si abbia familiarità con la [gestione dei dispositivi.](/windows/desktop/DevIO/device-management)

Per ottenere informazioni sullo stato della batteria, usare la [**funzione GetSystemPowerStatus,**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) che restituisce informazioni generali su tutte le fonti di alimentazione nel sistema. È consigliabile usare **GetSystemPowerStatus** quando possibile.

In alcuni casi, tuttavia, sono necessarie informazioni dettagliate su ogni singola batteria. A questo scopo, ogni dispositivo a batteria espone un'interfaccia IOCTL. Le operazioni IOCTL seguenti vengono eseguite usando la [**funzione DeviceIoControl:**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)

<dl>

[**INFORMAZIONI SULLA \_ QUERY DELLA \_ BATTERIA IOCTL \_**](ioctl-battery-query-information.md)  
[**STATO QUERY BATTERIA IOCTL \_ \_ \_**](ioctl-battery-query-status.md)  
[**TAG DI \_ QUERY DELLA \_ BATTERIA IOCTL \_**](ioctl-battery-query-tag.md)  
[**INFORMAZIONI SUL \_ SET DI \_ BATTERIA IOCTL \_**](ioctl-battery-set-information.md)  
</dl>

Per usare questa interfaccia, un'applicazione deve seguire diversi passaggi. In primo luogo, deve usare le routine di configurazione per enumerare tutti i dispositivi che dispongono di un'interfaccia di classe della batteria. Si noti che questi dispositivi rappresentano le porte della batteria, non le batterie effettive presenti nel sistema. L'applicazione deve quindi aprire un handle per ogni dispositivo in modo che possa usare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) per inviare richieste al dispositivo e quindi acquisire tag per le batterie inserite. Dopo aver completato questi passaggi, l'applicazione può inviare query a ogni dispositivo a batteria.

## <a name="battery-tags"></a>Tag batteria

Poiché ogni dispositivo a batteria rappresenta uno slot in cui è possibile inserire una batteria, deve essere possibile determinare quando la batteria viene rimossa e reinserita, sostituita o modificata in qualsiasi altro modo. A tale scopo, a ogni batteria in un determinato slot viene assegnato un tag. Questo tag deve essere usato per tutte le query per ottenere informazioni. Se il tag fornito dall'applicazione non corrisponde alla batteria, la query ha esito negativo, indicando all'applicazione che la batteria è cambiata in qualche modo. Per completare correttamente la query, è necessario un nuovo tag della batteria. Acquisire il tag usando [**l'operazione IOCTL \_ BATTERY QUERY \_ \_ TAG.**](ioctl-battery-query-tag.md) Se nello slot è presente una batteria, il tag restituito può essere passato a qualsiasi altro IOCTL della batteria per eseguire altre funzioni. In un sistema a più batteria, ogni dispositivo a batteria (slot) esercite i tag della batteria in modo indipendente, quindi il tag di due dispositivi separati potrebbe essere a volte identico.

Una modifica nel tag della batteria non significa necessariamente che la batteria sia stata rimossa e reinserita o sostituita. È possibile generare un nuovo tag se viene apportata una modifica ai dati che normalmente sarebbero statici. Ad esempio, al termine della ricarica di una batteria, potrebbe essere cambiata l'ultima capacità completamente carica. Il tag può anche cambiare se la comunicazione della batteria è stata temporaneamente persa o se è stata inviata una notifica non corretta dal BIOS. In alcuni sistemi, il tag della batteria può essere aggiornato ogni volta che cambia lo stato ca. Questo comportamento è dovuto a una caratteristica del sistema a batteria e non è comune.

Ogni volta che il tag della batteria viene aggiornato, la batteria deve essere trattata come se fosse una nuova batteria e tutti i dati memorizzati nella cache devono essere nuovamente letti. Se un'applicazione deve sapere se è presente la stessa batteria fisica, deve controllare il valore **di BatteryUniqueID** nel buffer di output di [**IOCTL BATTERY QUERY \_ \_ \_ INFORMATION**](ioctl-battery-query-information.md) quando viene chiamata con il livello di informazioni **BatteryUniqueID.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul risparmio energia](about-power-management.md)
</dt> <dt>

[Enumerazione dei dispositivi a batteria](enumerating-battery-devices.md)
</dt> </dl>

 

 
