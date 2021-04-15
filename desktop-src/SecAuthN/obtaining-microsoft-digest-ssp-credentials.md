---
description: Le credenziali utente sono necessarie per Microsoft Digest; sia il client che il server devono presentare credenziali valide prima di poter stabilire un contesto di sicurezza per lo scambio di messaggi. Gli handle delle credenziali vengono utilizzati per ottenere e presentare le credenziali.
ms.assetid: f97bdaf6-40a8-414e-a561-d3cb953d0bab
title: Acquisizione di Microsoft Digest credenziali SSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c61895ecc8e49713665af4542689729bc491d9e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484709"
---
# <a name="obtaining-microsoft-digest-ssp-credentials"></a>Acquisizione di Microsoft Digest credenziali SSP

Le [*credenziali*](../secgloss/c-gly.md) utente sono necessarie per Microsoft Digest; sia il client che il server devono presentare credenziali valide prima di poter stabilire un [*contesto di sicurezza*](../secgloss/s-gly.md) per lo scambio di messaggi. Gli handle delle credenziali vengono utilizzati per ottenere e presentare le credenziali.

Poiché l'handle delle credenziali viene utilizzato per archiviare le informazioni di configurazione, non è possibile utilizzare lo stesso handle sia per le operazioni sul lato client che sul lato server. Ciò significa che le applicazioni che supportano le connessioni client e server devono ottenere almeno due handle di credenziali.

Per ottenere un handle per le credenziali richieste da Microsoft Digest, chiamare la funzione [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) .

Negli esempi di linguaggio C seguenti viene illustrato come ottenere le credenziali.

-   [Recupero delle credenziali del digest predefinite](obtaining-default-digest-credentials.md)
-   [Acquisizione di credenziali del digest alternative](obtaining-alternate-digest-credentials.md)

 

 
