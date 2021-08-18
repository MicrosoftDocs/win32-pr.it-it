---
description: Le credenziali utente sono richieste da Microsoft Digest; Sia il client che il server devono presentare credenziali valide prima di poter stabilire un contesto di sicurezza per lo scambio di messaggi. Gli handle di credenziali vengono usati per ottenere e presentare le credenziali.
ms.assetid: f97bdaf6-40a8-414e-a561-d3cb953d0bab
title: Recupero delle Microsoft Digest SSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ea17889331453f009d0d19b7b834e9a4b1301636ec41ef73e6557f79419b461
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921280"
---
# <a name="obtaining-microsoft-digest-ssp-credentials"></a>Recupero delle Microsoft Digest SSP

Le [*credenziali utente*](../secgloss/c-gly.md) sono richieste da Microsoft Digest; Sia il client che il server devono presentare credenziali valide prima di poter stabilire un [*contesto di sicurezza per*](../secgloss/s-gly.md) lo scambio di messaggi. Gli handle di credenziali vengono usati per ottenere e presentare le credenziali.

Poiché l'handle delle credenziali viene usato per archiviare le informazioni di configurazione, lo stesso handle non può essere usato sia per le operazioni sul lato client che sul lato server. Ciò significa che le applicazioni che supportano connessioni client e server devono ottenere almeno due handle di credenziali.

Per ottenere un handle per le credenziali richieste da Microsoft Digest, chiamare la [**funzione AcquireCredentialsHandle.**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)

Gli esempi di linguaggio C seguenti illustrano come ottenere le credenziali.

-   [Recupero delle credenziali digest predefinite](obtaining-default-digest-credentials.md)
-   [Recupero di credenziali digest alternative](obtaining-alternate-digest-credentials.md)

 

 
