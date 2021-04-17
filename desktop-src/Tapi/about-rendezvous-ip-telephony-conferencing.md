---
description: I controlli TAPI 3 Rendezvous forniscono i meccanismi per annunciare e individuare le conferenze dell'IP multimediale a più parti. Di seguito viene descritto un set di componenti e interfacce di Component Object Model (COM) per implementare la conferenza.
ms.assetid: 0ca2edac-b507-497e-9e63-78a10466e2eb
title: Informazioni sulle conferenze telefoniche IP Rendezvous
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4bd06fb848088a42e34bd7b176358a7507e3d2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558982"
---
# <a name="about-rendezvous-ip-telephony-conferencing"></a>Informazioni sulle conferenze telefoniche IP Rendezvous

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

I controlli TAPI 3 Rendezvous forniscono i meccanismi per annunciare e individuare le conferenze dell'IP multimediale a più parti. Di seguito viene descritto un set di componenti e interfacce di Component Object Model (COM) per implementare la conferenza.

COM è il modello di codifica di base per TAPI 3 e la loro familiarità si presuppone in questo documento. Per informazioni su COM, cercare Platform Software Development Kit (SDK).

## <a name="features"></a>Funzionalità

-   Fornisce l'astrazione di una directory di conferenza per la modifica degli annunci di conferenze multimediali
-   Fornisce sicurezza tramite autenticazione, crittografia e un livello di controllo di accesso (ACL) per annuncio
-   Fornisce uno schema comune per un annuncio della conferenza, abilitando le ricerche in base ai valori di attributo
-   Consente le estensioni tramite un attributo gestito dal provider (BLOB della conferenza) nello schema
-   Fornisce un wrapper COM per l'API di allocazione di indirizzi multicast (MADCAP)

## <a name="architecture"></a>Architettura

Le descrizioni e i diagrammi seguenti illustrano gli aspetti chiave dell'architettura del sistema.

-   Il client può modificare le conferenze archiviate in una directory dinamica ILS o nel server NTDS usando i controlli Rendezvous. Il protocollo LDAP (Lightweight Directory Access Protocol) viene utilizzato per comunicare con un server ILS.
-   I controlli Rendezvous forniscono interfacce COM doppie per lo script e la programmazione.
-   Un server SAP (Session annuncio Protocol) con accesso diretto a Internet è in ascolto degli annunci di conferenze su Internet e popola i server dinamici ILS con le informazioni sulla conferenza. Analogamente, annuncia anche le conferenze create localmente il cui ambito include Internet. Il server SAP non è pianificato per Microsoft Windows 2000.

![architettura del sistema Rendezvous](images/rend1.png)

 

 



