---
description: 'Altre informazioni su: considerazioni sulla programmazione per la scrittura di gestori di risorse'
ms.assetid: 7f1e61e8-15e1-4a25-b864-eeadcac61108
title: Considerazioni sulla programmazione per la scrittura di gestori di risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bae64ead32c747a0e8499dcdc8821d36f01f06e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313363"
---
# <a name="programming-considerations-for-writing-resource-managers"></a>Considerazioni sulla programmazione per la scrittura di gestori di risorse

Quando si usa l'API di gestione transazioni kernel per aggiungere il supporto delle transazioni alle applicazioni, tenere presente quanto segue:

-   Quando si scrive il proprio Resource Manager, è necessario disporre di una conoscenza approfondita del funzionamento delle tecniche e dei protocolli di gestione delle transazioni.
-   Se non si scrivono correttamente i gestori delle risorse, è possibile danneggiare i propri dati con operazioni di ripristino gestite in modo non corretto. È anche possibile aggiungere la parte finale del log delle transazioni e riempire la file system con i log delle transazioni.
-   Se i criteri per le dimensioni del log non sono impostati in modo da impedire l'aumento delle dimensioni del log, Resource Manager non arresterà le transazioni. Resource Manager deve arrestare l'aggiornamento del sistema in modo da non sovraccaricare le risorse file system.
-   I gestori di risorse devono usare gli elenchi di controllo di accesso (ACL) per controllare l'accesso ai file di log. in caso contrario, sono possibili attacchi di tipo Denial of Service.
-   Qualsiasi gestore di risorse o partecipante alla transazione che memorizza nella cache i dati deve integrarsi per le notifiche di pre-preparazione. Quando viene ricevuta una notifica preliminare, è necessario scaricare tutti i dati, in modo che qualsiasi gestore di risorse downstream possa integrarsi prima della fase di preparazione. Eventuali ulteriori operazioni nella transazione non devono essere memorizzate nella cache.
-   Non chiudere un handle di integrazione mentre la transazione è ancora attiva. in questo modo verrà eseguito il rollback della transazione.

 

 



