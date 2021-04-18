---
description: Le batterie possono fornire potenza per computer portatili e computer in esecuzione in un gruppo di continuità (UPS, Power Supply).
ms.assetid: 3580b37d-611c-46b4-9300-4943833d6852
title: Informazioni sulla batteria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4f9838a2a95db037b9655f116f07e3cf2e072d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312062"
---
# <a name="battery-information"></a>Informazioni sulla batteria

Le batterie possono fornire potenza per computer portatili e computer in esecuzione in un gruppo di continuità (UPS, Power Supply). In questi computer, il sistema operativo fornisce informazioni sullo stato della batteria, in modo che le applicazioni possano fornire funzioni utili per l'utente. Alcuni sistemi a batteria non standard meno recenti e UPS non sono supportati.

Si noti che questa panoramica presuppone che l'utente abbia familiarità con la [gestione dei dispositivi](/windows/desktop/DevIO/device-management).

Per ottenere informazioni sullo stato della batteria, usare la funzione [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) , che restituisce informazioni generali su tutte le fonti di alimentazione del sistema. Quando possibile, è consigliabile usare **GetSystemPowerStatus** .

In alcuni casi, tuttavia, sono necessarie informazioni dettagliate su ogni singola batteria. A questo scopo, ogni dispositivo della batteria espone un'interfaccia IOCTL. Le operazioni IOCTL seguenti vengono eseguite utilizzando la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) :

<dl>

[**\_ \_ informazioni sulle query della batteria IOCTL \_**](ioctl-battery-query-information.md)  
[**\_stato della \_ query della batteria IOCTL \_**](ioctl-battery-query-status.md)  
[**\_tag di \_ query della batteria IOCTL \_**](ioctl-battery-query-tag.md)  
[**\_ \_ informazioni sui set di batterie IOCTL \_**](ioctl-battery-set-information.md)  
</dl>

Per utilizzare questa interfaccia, un'applicazione deve eseguire diversi passaggi. Per prima cosa, è necessario usare routine di installazione per enumerare tutti i dispositivi che dispongono di un'interfaccia di classe della batteria. Si noti che questi dispositivi rappresentano le porte della batteria, non le batterie effettive presenti nel sistema. L'applicazione deve quindi aprire un handle per ogni dispositivo, in modo che possa usare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) per inviare richieste al dispositivo e quindi acquisire i tag per tutte le batterie inserite. Dopo aver completato questi passaggi, l'applicazione può inviare query a ogni dispositivo della batteria.

## <a name="battery-tags"></a>Tag della batteria

Poiché ogni dispositivo della batteria rappresenta uno slot in cui è possibile inserire una batteria, è necessario un modo per determinare quando la batteria viene rimossa e reinserita, sostituita o modificata in altro modo. A tale scopo, a ogni batteria in un particolare slot viene assegnato un tag. Questo tag deve essere usato per tutte le query per le informazioni. Se il tag fornito dall'applicazione non corrisponde alla batteria, la query ha esito negativo, indicando all'applicazione che la batteria è stata modificata in qualche modo. Per completare correttamente la query, è necessario un nuovo tag della batteria. Acquisire il tag usando l'operazione di [**\_ tag di \_ query \_ della batteria IOCTL**](ioctl-battery-query-tag.md) . Se in tale slot è presente una batteria, il tag restituito può essere passato a qualsiasi altro IOCTL della batteria per eseguire altre funzioni. In un sistema a più batterie, ogni dispositivo batteria (slot) rilascia tag della batteria in modo indipendente, quindi il tag di due dispositivi distinti potrebbe essere identico a volte.

Una modifica nel tag della batteria non significa necessariamente che la batteria è stata rimossa e reinserita o sostituita. È possibile generare un nuovo tag se è presente una modifica in uno dei dati normalmente statici. Ad esempio, quando si esegue una ricarica della batteria, è possibile che sia stata modificata l'ultima capacità completamente caricata. Il tag può anche cambiare se la comunicazione della batteria è stata persa temporaneamente o se si è verificata una notifica non corretta dal BIOS. In alcuni sistemi, il tag della batteria può essere aggiornato ogni volta che viene modificato lo stato AC. Questo comportamento è dovuto a una caratteristica del sistema di batteria e non è comune.

Ogni volta che viene aggiornato il tag della batteria, la batteria deve essere considerata come una nuova batteria e tutti i dati memorizzati nella cache devono essere letti nuovamente. Se un'applicazione deve stabilire se è presente la stessa batteria fisica, deve controllare il valore di **BatteryUniqueID** nel buffer di output delle [**\_ \_ \_ informazioni sulle query della batteria IOCTL**](ioctl-battery-query-information.md) quando viene chiamato con il livello di informazioni **BatteryUniqueID** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul risparmio energia](about-power-management.md)
</dt> <dt>

[Enumerazione dei dispositivi della batteria](enumerating-battery-devices.md)
</dt> </dl>

 

 
