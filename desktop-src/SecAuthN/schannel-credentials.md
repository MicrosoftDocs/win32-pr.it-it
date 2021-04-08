---
description: I protocolli Schannel richiedono credenziali per autenticare i server e, facoltativamente, i client.
ms.assetid: 8295b1bd-6ae1-4f7e-926d-a9da7ec6a524
title: Credenziali Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f91556a7e3bfca67aa386f0264e78ae67052f02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967388"
---
# <a name="schannel-credentials"></a>Credenziali Schannel

I protocolli Schannel richiedono credenziali per autenticare i server e, facoltativamente, i client. L'autenticazione server, in cui il server fornisce la prova dell'identità al client, è richiesta dai [*protocolli di sicurezza*](../secgloss/s-gly.md)Schannel. L'autenticazione client può essere richiesta dal server in qualsiasi momento.

Le credenziali Schannel sono certificati [*X. 509*](../secgloss/x-gly.md) . Le informazioni sulle chiavi [*pubbliche*](../secgloss/p-gly.md) e [*private*](../secgloss/p-gly.md) dei certificati vengono usate per autenticare il server e, facoltativamente, il client. Queste chiavi vengono usate anche per fornire l' [*integrità*](../secgloss/i-gly.md) dei messaggi, mentre client e server scambiano le informazioni necessarie per generare e scambiare le [*chiavi della sessione*](../secgloss/s-gly.md).

Per informazioni sulla programmazione, vedere [ottenere le credenziali Schannel](obtaining-schannel-credentials.md).

 

 
