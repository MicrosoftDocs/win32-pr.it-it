---
description: Usare queste linee guida per coprire un'intera Windows installazione del programma di installazione con una firma digitale.
ms.assetid: e70eab94-4615-4a73-bccc-e16bd24551f6
title: Creazione di un'installazione firmata completamente verificata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d105b06e3f063d8cbeb1fac579beb12258b20062bf5cbae2cc6d08e9be6e4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066181"
---
# <a name="authoring-a-fully-verified-signed-installation"></a>Creazione di un'installazione firmata completamente verificata

È possibile usare queste linee guida per coprire un'intera Windows installazione del programma di installazione con una firma digitale.

Gli autori Windows installazioni del programma di installazione devono rispettare quanto segue per garantire che tutte le parti dell'installazione siano coperte da una firma digitale:

-   Usare file CAB interni oppure usare file CAB esterni firmati e creare correttamente la tabella [MsiDigitalSignature](msidigitalsignature-table.md) e [la tabella MsiDigitalCertificate](msidigitalcertificate-table.md).
-   Usare solo le azioni personalizzate archiviate all'interno del pacchetto o installate con il pacchetto.
-   Firmare il pacchetto di installazione.
-   Includere una [tabella MsiPatchCertificate](msipatchcertificate-table.md) nel pacchetto. Per abilitare [l'applicazione di patch](user-account-control--uac--patching.md)a Controllo dell'account utente, questa tabella deve contenere le informazioni usate per identificare i certificati del firmatario usati per firmare digitalmente le patch. L'applicazione di patch di Controllo dell'account utente consente all'autore del pacchetto di installazione di identificare le patch con firma digitale che possono essere applicate in futuro da utenti non amministratori.

Per un esempio che illustra come creare un'installazione firmata usando l'automazione, vedere Creazione di [un'installazione firmata completamente verificata tramite Automazione.](authoring-a-fully-verified-signed-installation-using-automation.md)

 

 



