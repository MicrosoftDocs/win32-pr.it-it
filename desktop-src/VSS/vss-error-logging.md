---
description: "Nel registro eventi dell'applicazione vengono scritte le informazioni seguenti sullo stato e sull'errore vss:"
ms.assetid: d0b0f012-ad4f-4bd8-bb97-98f212bcbe81
title: Registrazione degli errori VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c2743fc6c23458a1059287a7731777e92447e3cd57ebf52e40baf7619c5658
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056229"
---
# <a name="vss-error-logging"></a>Registrazione degli errori VSS

Nel registro eventi dell'applicazione vengono scritte le informazioni seguenti sullo stato e sull'errore vss:

-   Errori del richiedente generati tramite [**l'interfaccia IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)
-   Errori del writer generati nell'uso della [**classe CVssWriter,**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) incluso l'override dei metodi
-   Errori generati dal provider predefinito
-   Errori del servizio VsS generati nell'attività di coordinamento di provider, writer e richiedente (ad esempio la generazione di eventi)

Questi errori possono avere una serie di cause, tra cui un errore di programmazione nel codice di terze parti o errori di configurazione correlati al Servizio Copia Copia Software.

I driver VSS e la funzionalità di implementazione di livello inferiore scrivono errori nel registro di sistema. Il software di terze parti (richiedente, provider, writer) può scegliere il registro applicazioni, il registro di sistema o entrambi per scrivere le voci del log degli errori.

È consigliabile che le applicazioni di alto livello, ad esempio il codice in modalità utente, usino il registro applicazioni. Le applicazioni di livello inferiore, ad esempio le interfacce hardware e i driver, devono usare il registro di sistema.

 

 



