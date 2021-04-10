---
description: I controlli di Rendezvous TAPI 3 consentono a un programmatore di creare applicazioni in grado di creare e individuare conferenze IP multicast multimediali.
ms.assetid: 4da2046c-00fd-46a8-805f-503729cfa531
title: Conferenza telefonica IP Rendezvous
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1cbfc3a1e07fdc245af0ae6b93277c90083a75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227483"
---
# <a name="rendezvous-ip-telephony-conferencing"></a>Conferenza telefonica IP Rendezvous

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

I controlli di Rendezvous TAPI 3 consentono a un programmatore di creare applicazioni in grado di creare e individuare conferenze IP multicast multimediali.

Componenti chiave di Rendezvous:

I [controlli directory](directory-controls.md) sono un'astrazione degli elenchi di conferenze in un server ILS o NTDS.

I [controlli BLOB della conferenza](conference-blob-controls.md) rappresentano informazioni specifiche per la conferenza, ad esempio l'ora di inizio e di fine. Sono disponibili interfacce speciali per i BLOB del protocollo SDP. Per informazioni dettagliate, vedere il documento RFC 2327 denominato "SDP: Session Description Protocol". Una copia corrente di questa RFC può essere individuata tramite un motore di ricerca Internet.

Le [interfacce com multicast](multicast-com-interfaces.md) sono wrapper com per le funzioni MADCAP, noto in precedenza come mdhcp. Queste interfacce consentono a un'applicazione di ottenere indirizzi multicast da un server di allocazione indirizzi multicast.

Il materiale seguente fornisce una panoramica generale e alcuni esempi di utilizzo dei controlli Rendezvous per la telefonia IP e la conferenza.

 

 



