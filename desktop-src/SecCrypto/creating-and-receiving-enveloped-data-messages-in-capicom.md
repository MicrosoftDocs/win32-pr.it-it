---
description: Il messaggio in busta è costituito dal messaggio crittografato, dai certificati dei destinatari previsti e dal set di chiavi crittografate, una per ogni destinatario. Il messaggio generato è in formato PKCS \# 7/CMS.
ms.assetid: 2acd0b58-1028-478d-bfa1-b02fa457d7e3
title: Creazione e ricezione di messaggi di dati in buste in CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4024516333b7dd416f788f181f2ac36e5e0f4e015953cdab26d08b48da16c49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876540"
---
# <a name="creating-and-receiving-enveloped-data-messages-in-capicom"></a>Creazione e ricezione di messaggi di dati in buste in CAPICOM

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [Alternative all'uso di CAPICOM.](alternatives-to-using-capicom.md)\]

Un messaggio in busta è un messaggio crittografato per un set di destinatari. Nel processo di envelopment viene generata una chiave di crittografia della sessione e il messaggio viene crittografato con tale chiave. La chiave di crittografia stessa viene quindi crittografata separatamente per ogni destinatario usando le chiavi pubbliche del certificato di ogni destinatario previsto. Il messaggio in busta è costituito dal messaggio crittografato, dai certificati dei destinatari previsti e dal set di chiavi crittografate, una per ogni destinatario. Il messaggio generato è in formato PKCS \# 7/CMS.

Le sezioni seguenti illustrano procedure ed esempi per le attività dei messaggi in busta:

-   [Invio di un messaggio di dati in busta](sending-an-enveloped-data-message.md)
-   [Ricezione di un messaggio di dati in busta](receiving-an-enveloped-data-message.md)

 

 



