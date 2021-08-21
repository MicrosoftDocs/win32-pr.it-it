---
description: I controlli TAPI 3 Rendezvous consentono a un programmatore di creare applicazioni in grado di creare e individuare conferenze IP multicast multimediali.
ms.assetid: 4da2046c-00fd-46a8-805f-503729cfa531
title: Rendezvous IP Telephony Conferencing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c1486f2ca730f1efb0391fdea5a3ad22bec65385a31bce9bf233f0f230b7ee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773571"
---
# <a name="rendezvous-ip-telephony-conferencing"></a>Rendezvous IP Telephony Conferencing

\[I controlli e le interfacce di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

I controlli TAPI 3 Rendezvous consentono a un programmatore di creare applicazioni in grado di creare e individuare conferenze IP multicast multimediali.

I componenti chiave di Rendezvous:

[I controlli directory](directory-controls.md) sono un'astrazione di elenchi di conferenze in un server ILS o NTDS.

[I controlli BLOB di](conference-blob-controls.md) conferenze rappresentano informazioni specifiche della conferenza, ad esempio l'ora di inizio e di arresto. Sono disponibili interfacce speciali per i BLOB del protocollo SDP. Per informazioni dettagliate, vedere RFC 2327 intitolata "SDP: Session Description Protocol". Una copia corrente di questa RFC può essere individuata usando un motore di ricerca Internet.

[Le interfacce COM multicast](multicast-com-interfaces.md) sono wrapper COM per le funzioni MADCAP, precedentemente noti come MDHCP. Queste interfacce consentono a un'applicazione di ottenere indirizzi multicast da un server di allocazione di indirizzi multicast.

Il materiale seguente offre una panoramica generale e alcuni esempi di utilizzo dei controlli Rendezvous per la telefonia IP e le conferenze.

 

 



