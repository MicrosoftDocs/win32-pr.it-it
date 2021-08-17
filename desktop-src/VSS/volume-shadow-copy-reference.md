---
description: Il Servizio Copia Shadow del volume (VSS) è un set di API COM e C++ che consentono l'esecuzione di backup dei volumi mentre le applicazioni nel sistema (denominate writer) continuano a scrivere nei volumi.
ms.assetid: 94d9504b-2838-4516-8031-daa7bd9d2fec
title: Informazioni di riferimento per l'API Copia Shadow del volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fbc2d0bec6d68572a67a1dc80327fb80028d7f8d98487f24fec24e2c2e65f95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751528"
---
# <a name="volume-shadow-copy-api-reference"></a>Informazioni di riferimento per l'API Copia Shadow del volume

Il Servizio Copia Shadow del volume (VSS) è un set di API COM e C++ che consentono l'esecuzione di backup dei volumi mentre le applicazioni nel sistema (denominate writer) continuano a scrivere nei volumi.

Il Servizio Copia Shadow del volume supporta questi backup tramite la creazione di copie shadow, un duplicato del volume originale in un determinato momento.

Gli sviluppatori di terze parti possono usare l'API del Servizio Copia Shadow del volume per creare richiedenti,ad esempio un'applicazione di backup, per creare e gestire copie shadow.

Le operazioni effettive di creazione e rappresentazione di copie shadow vengono eseguite da applicazioni a livello di sistema note come provider.

Gli sviluppatori possono anche usare l'API per costruire writer: applicazioni che sono in grado di coordinare le operazioni di I/O con la creazione e la manipolazione di copie shadow.

-   [Classi dell'API Copia Shadow del volume](volume-shadow-copy-api-classes.md)
-   [Tipi di dati dell'API Copia Shadow del volume](volume-shadow-copy-api-data-types.md)
-   [Enumerazioni dell'API Copia Shadow del volume](volume-shadow-copy-api-enumeration-types.md)
-   [Funzioni dell'API Copia Shadow del volume](volume-shadow-copy-api-functions.md)
-   [Interfacce DELL'API Copia Shadow del volume](volume-shadow-copy-api-interfaces.md)
-   [Strutture dell'API Copia Shadow del volume](volume-shadow-copy-api-structures.md)
-   [Glossario della Copia Shadow del volume](volume-shadow-copy-glossary.md)

Per altre informazioni sulla scrittura di richiedenti e writer, vedere [Using the Servizio Copia Shadow del volume](using-the-volume-shadow-copy-service.md).

 

 



