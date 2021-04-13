---
description: Il messaggio in busta digitale è costituito dal messaggio crittografato, dai certificati dei destinatari desiderati e dal set di chiavi crittografate, uno per ogni destinatario. Il messaggio generato è in \# formato PKCS 7/cms.
ms.assetid: 2acd0b58-1028-478d-bfa1-b02fa457d7e3
title: Creazione e ricezione di messaggi di dati in busta digitale in CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672d56383ac635a295847777c0e557bbe7c40b69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343151"
---
# <a name="creating-and-receiving-enveloped-data-messages-in-capicom"></a>Creazione e ricezione di messaggi di dati in busta digitale in CAPICOM

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [alternative all'uso di CAPICOM](alternatives-to-using-capicom.md).\]

Un messaggio in busta digitale è un messaggio crittografato per un set di destinatari. Nel processo di inviluppo viene generata una chiave di crittografia della sessione e il messaggio viene crittografato con tale chiave. La chiave di crittografia stessa viene quindi crittografata separatamente per ogni destinatario utilizzando le chiavi pubbliche di ogni certificato del destinatario previsto. Il messaggio in busta digitale è costituito dal messaggio crittografato, dai certificati dei destinatari desiderati e dal set di chiavi crittografate, uno per ogni destinatario. Il messaggio generato è in \# formato PKCS 7/cms.

Le sezioni seguenti illustrano le procedure e gli esempi per le attività dei messaggi in busta:

-   [Invio di un messaggio di dati in busta](sending-an-enveloped-data-message.md)
-   [Ricezione di un messaggio di dati in busta](receiving-an-enveloped-data-message.md)

 

 



