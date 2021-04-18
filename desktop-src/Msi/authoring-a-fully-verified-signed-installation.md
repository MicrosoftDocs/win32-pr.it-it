---
description: Usare queste linee guida per coprire un'intera Windows Installer installazione mediante una firma digitale.
ms.assetid: e70eab94-4615-4a73-bccc-e16bd24551f6
title: Creazione di un'installazione firmata completamente verificata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9e76bbfb77eab8b020cb1591847d2a36d09c96a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311048"
---
# <a name="authoring-a-fully-verified-signed-installation"></a>Creazione di un'installazione firmata completamente verificata

È possibile usare queste linee guida per coprire un'intera Windows Installer installazione mediante una firma digitale.

Gli autori di Windows Installer installazioni devono rispettare quanto segue per garantire che tutte le parti dell'installazione siano coperte da una firma digitale:

-   Utilizzare file CAB interni oppure utilizzare file CAB esterni firmati e creare correttamente la [tabella MsiDigitalSignature](msidigitalsignature-table.md) e la [tabella MsiDigitalCertificate](msidigitalcertificate-table.md).
-   Utilizzare solo le azioni personalizzate archiviate nel pacchetto o installate con il pacchetto.
-   Firmare il pacchetto di installazione.
-   Includere una [tabella MsiPatchCertificate](msipatchcertificate-table.md) nel pacchetto. Per abilitare l'applicazione di patch per il [controllo dell'account utente (UAC)](user-account-control--uac--patching.md), questa tabella deve contenere le informazioni utilizzate per identificare i certificati del firmatario utilizzati per la firma digitale delle patch. L'applicazione di patch del controllo dell'account utente consente all'autore del pacchetto di installazione di identificare patch firmate digitalmente che possono essere applicate in futuro da utenti non amministratori.

Per un esempio che illustra come creare un'installazione firmata usando l'automazione, vedere [creazione di un'installazione firmata completamente verificata usando l'automazione](authoring-a-fully-verified-signed-installation-using-automation.md).

 

 



