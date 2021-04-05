---
title: Pubblicazione con i punti di connessione del servizio
description: Lo schema Active Directory definisce una classe di oggetti serviceConnectionPoint (SCP) per semplificare la pubblicazione di dati specifici del servizio nella directory da parte di un servizio.
ms.assetid: 3544aa64-ecb0-48a1-ae49-05247a983842
ms.tgt_platform: multiple
keywords:
- Pubblicazione con i punti di connessione del servizio AD
- Active Directory punti di connessione del servizio
- Active Directory punti di connessione del servizio, pubblicazione con
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a458822f6c5e4d764b2e330c7ba084021b586548
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707576"
---
# <a name="publishing-with-service-connection-points"></a>Pubblicazione con i punti di connessione del servizio

Lo schema Active Directory definisce una classe di oggetti **serviceConnectionPoint** (SCP) per semplificare la pubblicazione di dati specifici del servizio nella directory da parte di un servizio. I client del servizio usano i dati in un SCP per individuare, connettersi e autenticare un'istanza del servizio.

In questa sezione viene fornita una panoramica dei punti di connessione del servizio e degli esempi di codice in cui viene illustrato come un'applicazione client/di servizio utilizza convergenza.

L'esempio di codice segue questa procedura per implementare la pubblicazione del servizio con convergenza.

Per ulteriori informazioni e un esempio di codice che esegue questi passaggi, vedere [creazione di un punto di connessione del servizio](creating-a-service-connection-point.md).

**Per creare convergenza nella directory durante l'installazione del servizio**

1.  Eseguire l'associazione all'oggetto computer per il computer host in cui è installata l'istanza del servizio.
2.  Creare un oggetto SCP come figlio dell'oggetto computer, specificando i valori iniziali per gli attributi di SCP.
3.  Impostare le voci di controllo di accesso (ACE) nel descrittore di sicurezza dell'oggetto SCP per consentire al servizio di modificare le proprietà SCP in fase di esecuzione.
4.  Memorizzare nella cache il **objectGUID** del SCP nel registro di sistema del computer host del servizio.

Per ulteriori informazioni e un esempio di codice che esegue questi passaggi, vedere [aggiornamento di un punto di connessione del servizio](updating-a-service-connection-point.md).

**Per aggiornare gli attributi SCP all'avvio del servizio**

1.  Recuperare **objectGUID** dal registro di sistema e usarlo per l'associazione al SCP.
2.  Recuperare gli attributi, ad esempio **serviceDNSName** e **SERVICEBINDINGINFORMATION**, dal SCP. Confrontare questi valori con i valori correnti e aggiornare SCP se necessario.

Per ulteriori informazioni e un esempio di codice che esegue questi passaggi, vedere [modalità di individuazione e utilizzo di un punto di connessione del servizio](how-clients-find-and-use-a-service-connection-point.md)da parte dei client.

**Per trovare e usare un SCP da un'applicazione client**

1.  Eseguire l'associazione al catalogo globale e cercare gli oggetti con un attributo **Keywords** corrispondente al GUID del prodotto del servizio. Ogni oggetto trovato è un'istanza del servizio. Selezionare un'istanza e recuperare il nome distinto del SCP.
2.  Usare il nome distinto per l'associazione all'SCP.
3.  Recuperare i valori di diversi attributi da SCP, ad esempio **serviceDNSName** e **serviceBindingInformation**. Usare questi valori per connettersi all'istanza del servizio e autenticarla.

Per ulteriori informazioni sui ruoli che possono creare e aggiornare un SCP, vedere [problemi di protezione per la pubblicazione del servizio](security-issues-for-service-publication.md).

Per ulteriori informazioni sulla creazione di un punto di connessione del [servizio, vedere la posizione in cui creare un punto di connessione del servizio](where-to-create-a-service-connection-point.md).

Per altre informazioni sul tipo di dati da archiviare in un SCP, vedere [proprietà del punto di connessione del servizio](service-connection-point-properties.md).

Per ulteriori informazioni sull'interazione tra un programma di installazione del servizio e il servizio per mantenere i dati correnti in un SCP, vedere [creazione e gestione di un punto di connessione del servizio](creating-and-maintaining-a-service-connection-point.md).

 

 




