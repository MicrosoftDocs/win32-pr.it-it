---
description: "Le informazioni di stato e di errore VSS seguenti vengono scritte nel registro eventi dell'applicazione:"
ms.assetid: d0b0f012-ad4f-4bd8-bb97-98f212bcbe81
title: Registrazione degli errori VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9822035f36f56162fb6836bf7ad4c09cdd31b777
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129298"
---
# <a name="vss-error-logging"></a>Registrazione degli errori VSS

Le informazioni di stato e di errore VSS seguenti vengono scritte nel registro eventi dell'applicazione:

-   Errori del richiedente prodotti tramite l'interfaccia [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)
-   Errori del writer generati nell'uso della classe [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) , inclusi i metodi di override
-   Errori generati dal provider predefinito
-   Errori del servizio VSS generati nell'attività di coordinamento del provider, del writer e del richiedente, ad esempio la generazione di eventi.

Questi errori possono avere diverse cause, incluso un errore di programmazione in codice di terze parti o errori di configurazione correlati a VSS.

I driver VSS e le funzionalità di implementazione di livello inferiore scrivono errori nel registro di sistema. Il software di terze parti (richiedente, provider, writer) può scegliere il registro applicazioni, il registro di sistema o entrambi per scrivere le voci del log degli errori.

Si consiglia di usare il registro applicazioni per le applicazioni di livello superiore, ad esempio il codice in modalità utente. Le applicazioni di livello inferiore, ad esempio le interfacce hardware e i driver, devono usare il registro di sistema.

 

 



