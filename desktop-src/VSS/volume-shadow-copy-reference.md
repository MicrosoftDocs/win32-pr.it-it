---
description: Il Servizio Copia Shadow del volume (VSS) è un set di API COM e C++ che consentono di eseguire i backup del volume mentre le applicazioni nel sistema (denominate writer) continuano a scrivere nei volumi.
ms.assetid: 94d9504b-2838-4516-8031-daa7bd9d2fec
title: Informazioni di riferimento sull'API copia shadow del volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea8651c987c01ce67f1383f2ab1a24ca3fea8bbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526293"
---
# <a name="volume-shadow-copy-api-reference"></a>Informazioni di riferimento sull'API copia shadow del volume

Il Servizio Copia Shadow del volume (VSS) è un set di API COM e C++ che consentono di eseguire i backup del volume mentre le applicazioni nel sistema (denominate writer) continuano a scrivere nei volumi.

VSS supporta questi backup tramite la creazione di copie shadow, un duplicato del volume originale in un determinato momento.

Gli sviluppatori di terze parti possono utilizzare l'API VSS per creare richiedenti, ad esempio un'applicazione di backup, per creare e gestire copie shadow.

Il lavoro effettivo di creazione e rappresentazione delle copie shadow viene eseguito dalle applicazioni a livello di sistema note come provider.

Gli sviluppatori possono anche usare l'API per costruire Writer: applicazioni compatibili con VSS in grado di coordinare le operazioni di I/O con la creazione e la manipolazione delle copie shadow.

-   [Classi API copia shadow del volume](volume-shadow-copy-api-classes.md)
-   [Tipi di dati dell'API copia shadow del volume](volume-shadow-copy-api-data-types.md)
-   [Enumerazioni API copia shadow del volume](volume-shadow-copy-api-enumeration-types.md)
-   [Funzioni API copia shadow del volume](volume-shadow-copy-api-functions.md)
-   [Interfacce API copia shadow del volume](volume-shadow-copy-api-interfaces.md)
-   [Strutture API copia shadow del volume](volume-shadow-copy-api-structures.md)
-   [Glossario copia shadow del volume](volume-shadow-copy-glossary.md)

Per ulteriori informazioni sulla scrittura di richiedenti e writer, vedere [utilizzo del servizio Copia Shadow del volume](using-the-volume-shadow-copy-service.md).

 

 



