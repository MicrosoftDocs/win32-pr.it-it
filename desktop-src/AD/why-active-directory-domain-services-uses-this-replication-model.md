---
title: Motivi per cui Active Directory Domain Services utilizza questo modello di replica
description: In questo argomento vengono illustrati i motivi del sistema in formato libero utilizzato da Active Directory Domain Services per un modello di replica.
ms.assetid: 202df900-6d03-4aa8-9099-016238059ef4
ms.tgt_platform: multiple
keywords:
- Modello di replica Active Directory, vantaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538fe291a04953d373ff3cd45cbd4693d3dafab4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855373"
---
# <a name="why-active-directory-domain-services-uses-this-replication-model"></a>Motivi per cui Active Directory Domain Services utilizza questo modello di replica

In questo argomento vengono illustrati i motivi del sistema in formato libero utilizzato da Active Directory Domain Services per un modello di replica.

Active Directory Domain Services sono un sistema in formato libero per i motivi seguenti:

-   I clienti richiedono una soluzione altamente distribuita in cui le parti della directory possono essere distribuite tra le reti e gestite localmente.
-   I clienti di grandi dimensioni crescono spesso fino a milioni di oggetti, centinaia o migliaia di repliche o entrambi.
-   Molte reti clienti forniscono solo la connettività intermittente ad alcune località; ad esempio, le piattaforme di drill-Oil remoto e vengono fornite in mare, quindi il sistema deve essere a tolleranza di operazioni parzialmente connesse o disconnesse.

Non esiste alcun modo per garantire la consapevolezza completa dello stato corrente o futuro di un sistema distribuito, perché la conoscenza delle modifiche di stato deve essere propagata e la propagazione richiede tempo, durante il quale possono verificarsi più modifiche di stato.

I sistemi strettamente collegati gestiscono l'incertezza tentando di eliminarlo. Questa operazione viene eseguita tramite vincoli sugli aggiornamenti, che richiedono che tutti i nodi o la maggior parte dei nodi siano disponibili prima di poter eseguire gli aggiornamenti, usando schemi di blocco distribuiti o un singolo master per le risorse critiche, vincolando la correttezza di tutti i nodi o una combinazione di queste tecniche. I nodi di calcolo più strettamente collegati in un sistema distribuito sono, minore è il limite di scalabilità.

I sistemi a formato libero gestiscono l'incertezza grazie alla tolleranza. Un sistema in formato libero consente ai nodi di avere visualizzazioni diverse dello stato generale del sistema e fornisce gli algoritmi per la risoluzione dei conflitti.

Le soluzioni strettamente associate sono state rifiutate come non idonee per Active Directory Domain Services a causa dei requisiti per l'amministrazione locale, l'operazione disconnessa e la scalabilità a un numero molto elevato di nodi. Il modello a regime di controllo libero scelto, la coerenza di più master sciolto con la convergenza, soddisfa tutti i requisiti.

 

 




