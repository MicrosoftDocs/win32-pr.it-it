---
title: Perché Active Directory Domain Services questo modello di replica
description: In questo argomento vengono illustrati i motivi del sistema in formato libero utilizzato Active Directory Domain Services per un modello di replica.
ms.assetid: 202df900-6d03-4aa8-9099-016238059ef4
ms.tgt_platform: multiple
keywords:
- Modello di replica Active Directory , vantaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79c137fadf768c97b6d8be962b22c74b45e30bc41c7dfb7e9ea67e1f145cd92d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181992"
---
# <a name="why-active-directory-domain-services-uses-this-replication-model"></a>Perché Active Directory Domain Services questo modello di replica

In questo argomento vengono illustrati i motivi del sistema in formato libero utilizzato Active Directory Domain Services per un modello di replica.

Active Directory Domain Services sono un sistema in formato libero per i motivi seguenti:

-   I clienti richiedono una soluzione altamente distribuita in cui parti della directory possono essere distribuite tra le reti e amministrate in locale.
-   I clienti di grandi dimensioni spesso aumentano fino a milioni di oggetti, centinaia o migliaia di repliche o entrambi.
-   Molte reti dei clienti forniscono solo connettività intermittente ad alcune località; Ad esempio, le piattaforme remote di esemplificazioni di olio e le navi in acqua, quindi il sistema deve essere a tolleranza di operazioni parzialmente connesse o disconnesse.

Non è possibile garantire la completa consapevolezza dello stato corrente o futuro di un sistema distribuito, perché la conoscenza delle modifiche di stato deve essere propagata e la propagazione richiede tempo, durante il quale possono verificarsi più modifiche di stato.

I sistemi strettamente accoppiati gestiscono l'incertezza provando a eliminarlo. Questa operazione viene eseguita tramite vincoli sugli aggiornamenti, che richiedono che tutti i nodi o la maggior parte dei nodi siano disponibili prima di poter eseguire gli aggiornamenti, usando schemi di blocco distribuiti o single-mastering per le risorse critiche, vincolando tutti i nodi a una connessione efficace o una combinazione di queste tecniche. Più strettamente accoppiati i nodi di calcolo in un sistema distribuito sono, più basso è il limite di scalabilità.

I sistemi in formato libero gestiscono l'incertezza tollerando l'incertezza. Un sistema in formato libero consente ai nodi di avere visualizzazioni diverse dello stato generale del sistema e fornisce algoritmi per la risoluzione dei conflitti.

Le soluzioni strettamente accoppiate sono state rifiutate come non idonee per Active Directory Domain Services a causa dei requisiti per l'amministrazione locale, il funzionamento disconnesso e la scalabilità per un numero molto elevato di nodi. Il modello a controllo libero scelto, la coerenza libero multi-master con convergenza, soddisfa tutti i requisiti.

 

 




