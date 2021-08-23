---
description: I tre tipi di spazi dei nomi Windows Sockets (Winsock) SPI includono spazi dei nomi dinamici, statici e persistenti.
ms.assetid: 2968ac98-bd40-4d37-9dd7-7870c4decd40
title: Tipi di spazi dei nomi in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ec933650825e891a723cbbc041ad4f631c6f54b7b2b4f6a255359b640509ef3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733191"
---
# <a name="types-of-namespaces-in-the-spi"></a>Tipi di spazi dei nomi in SPI

Esistono tre diversi tipi di spazi dei nomi in cui è possibile registrare un servizio:

-   Dynamic
-   Static
-   Persistente

Gli spazi dei nomi dinamici consentono ai servizi di registrarsi con lo spazio dei nomi in tempo reale e ai client di individuare i servizi disponibili in fase di esecuzione. Gli spazi dei nomi dinamici si basano spesso sulle trasmissioni per indicare la disponibilità continua di un servizio di rete. Esempi di spazi dei nomi dinamici includono lo spazio dei nomi SAP usato all'interno di un ambiente NetWare e lo spazio dei nomi NBP usato da AppleTalk.

Gli spazi dei nomi statici richiedono che tutti i servizi siano registrati in anticipo, ad esempio quando viene creato lo spazio dei nomi. IL DNS è un esempio di spazio dei nomi statico. Anche se esiste un modo a livello di codice per risolvere i nomi, non esiste alcun modo a livello di codice per registrare i nomi.

Gli spazi dei nomi persistenti consentono ai servizi di registrarsi con lo spazio dei nomi in tempo reale. A differenza degli spazi dei nomi dinamici, tuttavia, gli spazi dei nomi permanenti mantengono le informazioni di registrazione nell'archiviazione non volatile in cui rimangono fino a quando il servizio non richiede la rimozione. Gli spazi dei nomi persistenti sono tipiizzati dai servizi directory, ad esempio X.500 e NDS (NetWare Directory Service). Questi ambienti consentono l'aggiunta, l'eliminazione e la modifica delle proprietà del servizio. Inoltre, l'oggetto servizio che rappresenta il servizio all'interno del servizio directory potrebbe avere un'ampia gamma di attributi associati al servizio. L'attributo più importante per le applicazioni client è l'indirizzamento delle informazioni del servizio.

 

 



