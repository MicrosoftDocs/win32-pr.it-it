---
description: I tre tipi di spazi dei nomi in Windows Sockets (Winsock) SPI includono gli spazi dei nomi dinamici, statici e permanenti.
ms.assetid: 2968ac98-bd40-4d37-9dd7-7870c4decd40
title: Tipi di spazi dei nomi in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e40356987c67604755696f1a8b7224de15851ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315762"
---
# <a name="types-of-namespaces-in-the-spi"></a>Tipi di spazi dei nomi in SPI

Sono disponibili tre tipi diversi di spazi dei nomi in cui è possibile registrare un servizio:

-   Dynamic
-   Static
-   Persistente

Gli spazi dei nomi dinamici consentono ai servizi di registrarsi allo spazio dei nomi in tempo reale e ai client di individuare i servizi disponibili in fase di esecuzione. Gli spazi dei nomi dinamici si basano spesso sulle trasmissioni per indicare la disponibilità continua di un servizio di rete. Esempi di spazi dei nomi dinamici includono lo spazio dei nomi SAP usato in un ambiente NetWare e lo spazio dei nomi avvio usato da AppleTalk.

Gli spazi dei nomi statici richiedono la registrazione di tutti i servizi in anticipo, ovvero quando viene creato lo spazio dei nomi. Il DNS è un esempio di uno spazio dei nomi statico. Sebbene esista un metodo programmatico per la risoluzione dei nomi, non esiste alcun modo programmatico per registrare i nomi.

Gli spazi dei nomi permanenti consentono ai servizi di eseguire la registrazione con lo spazio dei nomi in tempo reale. A differenza degli spazi dei nomi dinamici, tuttavia, gli spazi dei nomi persistenti conservano le informazioni di registrazione in una risorsa di archiviazione non volatile dove rimangono fino al momento in cui il servizio richiede la rimozione. Gli spazi dei nomi permanenti sono caratterizzati da servizi directory quali X. 500 e NDS (servizio directory NetWare). Questi ambienti consentono l'aggiunta, l'eliminazione e la modifica delle proprietà del servizio. Inoltre, l'oggetto servizio che rappresenta il servizio all'interno del servizio directory potrebbe avere un'ampia gamma di attributi associati al servizio. L'attributo più importante per le applicazioni client è le informazioni di indirizzamento del servizio.

 

 



