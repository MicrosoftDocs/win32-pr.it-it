---
description: I programmatori e gli amministratori di sistema utilizzano i programmi di configurazione del servizio per modificare o eseguire query sul database dei servizi installati.
ms.assetid: 8ab97a4b-a4c2-4123-b5f5-27029bc3eb15
title: Programmi di configurazione del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85a2bfc87b093988c1a12c70ce64a4881c79397
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128898"
---
# <a name="service-configuration-programs"></a>Programmi di configurazione del servizio

I programmatori e gli amministratori di sistema utilizzano i programmi di configurazione del servizio per modificare o eseguire query sul database dei servizi installati. È possibile accedere al database anche usando le funzioni del registro di sistema. Tuttavia, è consigliabile usare solo le funzioni di configurazione SCM, che assicurano che il servizio sia installato e configurato correttamente.

Le funzioni di configurazione SCM richiedono un handle per un oggetto SCManager o un handle per un oggetto servizio. Per ottenere questi handle, il programma di configurazione del servizio deve:

1.  Utilizzare la funzione [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) per ottenere un handle per il database SCM in un computer specificato.
2.  Utilizzare la funzione [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) o [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) per ottenere un handle per l'oggetto servizio.

Per altre informazioni, vedere i seguenti argomenti:

-   [Installazione, rimozione ed enumerazione del servizio](service-installation-removal-and-enumeration.md)
-   [Configurazione del servizio](service-configuration.md)
-   [Configurazione di un servizio con SC](configuring-a-service-using-sc.md)

 

 



