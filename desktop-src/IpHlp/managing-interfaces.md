---
description: L'helper IP estende le capacità di gestione delle interfacce di rete. Esiste una corrispondenza uno-a-uno tra le interfacce e le schede in un determinato computer. Un'interfaccia è un'astrazione a livello di IP, mentre un adattatore è un'astrazione a livello di datalink.
ms.assetid: 598bbe67-30df-4c02-8f30-2ccf15b5c494
title: Gestione delle interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb46ecba6f1c5780960f6d8e363db9ec04d0cc3611da1caf023ec95bf5a99a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146694"
---
# <a name="managing-interfaces"></a>Gestione delle interfacce

L'helper IP estende le capacità di gestione delle interfacce di rete. Esiste una corrispondenza uno-a-uno tra le interfacce e le schede in un determinato computer. Un'interfaccia è un'astrazione a livello di IP, mentre un adattatore è un'astrazione a livello di datalink.

Usare le funzioni descritte nei paragrafi seguenti per gestire le interfacce nel computer locale.

La [**funzione GetNumberOfInterfaces**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces) restituisce il numero di interfacce nel computer locale.

La [**funzione GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) restituisce una tabella che contiene i nomi e gli indici corrispondenti per le interfacce nel computer locale. Per esempi di codice **che coinvolgono GetInterfaceInfo,** vedere [Gestione delle interfacce tramite GetInterfaceInfo.](managing-interfaces-using-getinterfaceinfo.md)

La [**funzione GetFriendlyIfIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex) accetta un indice di interfaccia e restituisce un indice di interfaccia compatibile con le versioni precedenti, che usa solo i 24 bit inferiori. Questo tipo di indice viene talvolta definito indice di interfaccia "descrittivo".

La [**funzione GetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getifentry) restituisce una [**struttura \_ MIB IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) che contiene informazioni su una particolare interfaccia nel computer locale. Questa funzione richiede al chiamante di fornire l'indice dell'interfaccia.

La [**funzione GetIfTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getiftable) restituisce una tabella di [**voci \_ IFROW MIB,**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) una per ogni interfaccia nel computer.

Usare la [**funzione SetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setifentry) per modificare la configurazione di una determinata interfaccia.

 

 
