---
title: Pubblicazione con punti di connessione del servizio
description: Lo schema di Active Directory definisce una classe di oggetti serviceConnectionPoint (SCP) per semplificare la pubblicazione di dati specifici del servizio nella directory.
ms.assetid: 3544aa64-ecb0-48a1-ae49-05247a983842
ms.tgt_platform: multiple
keywords:
- Pubblicazione con punti di connessione del servizio AD
- punti di connessione del servizio AD
- punti di connessione del servizio AD , pubblicazione con
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058c0a0e1f488ecdb50c14eb04788470b6bc25a0a3442457f1c57ced4b13efd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184945"
---
# <a name="publishing-with-service-connection-points"></a>Pubblicazione con punti di connessione del servizio

Lo schema di Active Directory definisce una classe di oggetti **serviceConnectionPoint** (SCP) per semplificare la pubblicazione di dati specifici del servizio nella directory. I client del servizio usano i dati in un SCP per individuare, connettersi e autenticare un'istanza del servizio.

Questa sezione offre una panoramica dei punti di connessione del servizio ed esempi di codice che illustrano come un'applicazione client/servizio usa i punti di connessione del servizio.

L'esempio di codice segue questi passaggi per implementare la pubblicazione del servizio con scp.

Per altre informazioni e un esempio di codice che esegue questi passaggi, vedere [Creazione di un punto di connessione del servizio](creating-a-service-connection-point.md).

**Per creare provider di servizi di configurazione nella directory durante l'installazione del servizio**

1.  Eseguire il binding all'oggetto computer per il computer host in cui è installata l'istanza del servizio.
2.  Creare un oggetto SCP come figlio dell'oggetto computer, specificando i valori iniziali per gli attributi di SCP.
3.  Impostare le voci di controllo di accesso (ACE) nel descrittore di sicurezza dell'oggetto SCP per consentire al servizio di modificare le proprietà SCP in fase di esecuzione.
4.  Memorizzare **nella cache il valore objectGUID** di SCP nel Registro di sistema nel computer host del servizio.

Per altre informazioni e un esempio di codice che esegue questi passaggi, vedere [Aggiornamento di un punto di connessione del servizio](updating-a-service-connection-point.md).

**Per aggiornare gli attributi SCP all'avvio del servizio**

1.  Recuperare **objectGUID dal** Registro di sistema e usarlo per l'associazione al SCP.
2.  Recuperare gli attributi, ad esempio **serviceDNSName** e **serviceBindingInformation,** da SCP. Confrontare questi valori con i valori correnti e aggiornare SCP, se necessario.

Per altre informazioni e un esempio di codice che esegue questi passaggi, vedere Come i [client trovano e usano un punto di connessione del servizio](how-clients-find-and-use-a-service-connection-point.md).

**Per trovare e usare un SCP da un'applicazione client**

1.  Eseguire l'associazione al catalogo globale e cercare gli oggetti con un attributo **keywords** corrispondente al GUID del prodotto del servizio. Ogni oggetto trovato è un'istanza del servizio. Selezionare un'istanza e recuperare il nome distinto del SCP.
2.  Usare il nome distinto per l'associazione all'SCP.
3.  Recuperare i valori di vari attributi da SCP, ad esempio **serviceDNSName** e **serviceBindingInformation**. Usare questi valori per connettersi all'istanza del servizio e autenticarla.

Per altre informazioni sui ruoli che possono creare e aggiornare un SCP, vedere [Problemi di sicurezza per la pubblicazione del servizio](security-issues-for-service-publication.md).

Per altre informazioni sulla posizione in cui creare un punto di connessione del servizio, vedere [Dove creare un punto di connessione del servizio](where-to-create-a-service-connection-point.md).

Per altre informazioni sul tipo di dati da archiviare in un SCP, vedere Proprietà del punto di [connessione del servizio](service-connection-point-properties.md).

Per altre informazioni sul funzionamento di un programma di installazione del servizio e del servizio per mantenere i dati correnti in un SCP, vedere Creazione e gestione di [un punto di connessione del servizio](creating-and-maintaining-a-service-connection-point.md).

 

 




