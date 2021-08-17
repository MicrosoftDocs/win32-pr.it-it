---
description: I controlli TAPI 3 Rendezvous forniscono meccanismi per annunciare e individuare conferenze IP multimediali multiparty. Di seguito viene descritto un set di componenti Component Object Model (COM) e interfacce per implementare le conferenze.
ms.assetid: 0ca2edac-b507-497e-9e63-78a10466e2eb
title: Informazioni su Rendezvous IP Telephony Conferencing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 225f7842e0f7efdb97dcadc3d59adc8fa7e5adf0f73cd824b335500a5aa6c11d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117949285"
---
# <a name="about-rendezvous-ip-telephony-conferencing"></a>Informazioni su Rendezvous IP Telephony Conferencing

\[I controlli e le interfacce di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

I controlli TAPI 3 Rendezvous forniscono meccanismi per annunciare e individuare conferenze IP multimediali multiparty. Di seguito viene descritto un set di componenti Component Object Model (COM) e interfacce per implementare le conferenze.

COM è il modello di codifica di base per TAPI 3 e si presuppone una certa familiarità con questo documento. Per informazioni su COM, cercare Platform Software Development Kit (SDK).

## <a name="features"></a>Funzionalità

-   Fornisce l'astrazione di una directory delle conferenze per la modifica degli annunci di conferenze multimediali
-   Fornisce sicurezza tramite autenticazione, crittografia e un livello di controllo di accesso (ACL) per annuncio
-   Fornisce uno schema comune per un annuncio di conferenza, abilitando le ricerche in base ai valori degli attributi
-   Consente estensioni tramite un attributo gestito dal provider (BLOB di conferenze) nello schema
-   Fornisce un wrapper COM per l'API di allocazione di indirizzi multicast (MADCAP)

## <a name="architecture"></a>Architettura

Le descrizioni e il diagramma seguenti illustrano gli aspetti chiave dell'architettura di sistema.

-   Il client può modificare le conferenze archiviate in una directory dinamica ILS o in un server NTDS usando i controlli Rendezvous. Il Lightweight Directory Access Protocol (LDAP) viene usato per comunicare con un server ILS.
-   I controlli Rendezvous forniscono interfacce COM duali per lo scripting e la programmazione.
-   Un server SAP (Session Announcement Protocol) con accesso diretto a Internet è in ascolto degli annunci di conferenza su Internet e popola i server dinamici ILS con le informazioni sulla conferenza. Analogamente, annuncia anche le conferenze create localmente il cui ambito include Internet. Il server SAP non è pianificato per Microsoft Windows 2000.

![Architettura di sistema di rendezvous](images/rend1.png)

 

 



