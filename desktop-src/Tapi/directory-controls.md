---
description: Il diagramma seguente illustra gli oggetti principali che coinvolgono i controlli directory di TAPI 3 Rendezvous. Le interfacce visualizzate sono collegate con collegamento ipertestuale nelle pagine di riferimento pertinenti.
ms.assetid: f5ca1d61-5266-4406-8199-338e6a712db8
title: Controlli di directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87a7b9c0b11c76aac6067e1a3f67c3899552f1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307202"
---
# <a name="directory-controls"></a>Controlli di directory

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il diagramma seguente illustra gli oggetti principali che coinvolgono i controlli directory di TAPI 3 Rendezvous. Le interfacce visualizzate sono collegate con collegamento ipertestuale nelle pagine di riferimento pertinenti.

![interfacce e oggetti di controllo della directory Rendezvous](images/renddir.png)

L'interfaccia di controllo della directory principale è [**ITRendezvous**](/windows/desktop/api/Rend/nn-rend-itrendezvous), che deve essere creata chiamando **CoCreateInstance**. L'oggetto Rendezvous espone metodi per ottenere elenchi di directory disponibili e per creare nuove directory o oggetti directory.

Una directory risiede in un server ed è un elenco di oggetti directory insieme a informazioni descrittive. I metodi associati a [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory) possono ottenere informazioni associate alla directory nel suo complesso, ad esempio se si tratta di una directory ILS.

Un oggetto directory può rappresentare una conferenza o un utente. L'interfaccia [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject) fornisce metodi che consentono di recuperare o modificare informazioni generiche in un oggetto directory, ad esempio l'indirizzo di connessione remota.

Le informazioni relative a conferenze e utenti, ad esempio l'URL di una conferenza o il telefono IP primario di un utente, vengono modificate dai metodi forniti nelle interfacce [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) e [**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser) .

 

 



