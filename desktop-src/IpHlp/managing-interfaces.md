---
description: L'helper IP estende le capacità di gestione delle interfacce di rete. Esiste una corrispondenza uno-a-uno tra le interfacce e gli adapter in un determinato computer. Un'interfaccia è un'astrazione a livello di IP, mentre un adapter è un'astrazione a livello di Datalink.
ms.assetid: 598bbe67-30df-4c02-8f30-2ccf15b5c494
title: Gestione delle interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d79d46ec1ba7606cbc7e79b4312432984239a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227413"
---
# <a name="managing-interfaces"></a>Gestione delle interfacce

L'helper IP estende le capacità di gestione delle interfacce di rete. Esiste una corrispondenza uno-a-uno tra le interfacce e gli adapter in un determinato computer. Un'interfaccia è un'astrazione a livello di IP, mentre un adapter è un'astrazione a livello di Datalink.

Usare le funzioni descritte nei paragrafi seguenti per gestire le interfacce nel computer locale.

La funzione [**GetNumberOfInterfaces**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces) restituisce il numero di interfacce nel computer locale.

La funzione [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) restituisce una tabella che contiene i nomi e gli indici corrispondenti per le interfacce nel computer locale. Per esempi di codice che coinvolgono **GetInterfaceInfo** , vedere [gestione delle interfacce mediante GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).

La funzione [**GetFriendlyIfIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex) accetta un indice di interfaccia e restituisce un indice di interfaccia compatibile con le versioni precedenti, ovvero uno che usa solo i 24 bit inferiori. Questo tipo di indice viene talvolta definito indice di interfaccia "descrittivo".

La funzione [**GetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getifentry) restituisce una struttura [**MIB \_ IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) che contiene informazioni su una particolare interfaccia nel computer locale. Questa funzione richiede che il chiamante fornisca l'indice dell'interfaccia.

La funzione [**GetIfTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getiftable) restituisce una tabella di voci [**MIB \_ IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) , una per ogni interfaccia nel computer.

Utilizzare la funzione [**SetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setifentry) per modificare la configurazione di una particolare interfaccia.

 

 
