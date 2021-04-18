---
title: Creazione di un provider di Remote Desktop Protocol
description: Informazioni sulla creazione di un provider di Remote Desktop Protocol. Gestione protocolli viene implementato come server COM e registrato in un percorso in cui viene eseguita la ricerca all'avvio del servizio Servizi Desktop remoto.
ms.assetid: 9a3e6d5c-464f-4227-a06f-16eb8ed1079e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41265a350b4d5c559731a09abc21aa4c81b9b29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297632"
---
# <a name="creating-a-remote-desktop-protocol-provider"></a>Creazione di un provider di Remote Desktop Protocol

Le sezioni seguenti contengono informazioni sulla creazione di un provider di Remote Desktop Protocol. Gestione protocolli viene implementato come server COM e registrato in un percorso in cui viene eseguita la ricerca all'avvio del servizio Servizi Desktop remoto.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Registrazione di gestione protocolli](registering-the-custom-protocol.md)
</dt> <dd>

È necessario creare almeno una voce del valore del registro di sistema per gestione protocolli, in modo che il servizio Servizi Desktop remoto possa crearne un'istanza.

</dd> <dt>

[Sequenza di chiamate al metodo](method-call-sequence.md)
</dt> <dd>

Il servizio Servizi Desktop remoto e il provider di protocollo si chiamano reciprocamente in sequenze chiaramente definite.

</dd> </dl>

-   [Registrazione di gestione protocolli](registering-the-custom-protocol.md)
-   [Sequenza di chiamate al metodo](method-call-sequence.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API del provider Remote Desktop Protocol](custom-remote-desktop-protocols.md)
</dt> <dt>

[Utilizzo di Servizi Desktop remoto](using-terminal-services.md)
</dt> </dl>

 

 




