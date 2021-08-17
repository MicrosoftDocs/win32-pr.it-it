---
title: Creazione di un provider di Remote Desktop Protocol
description: Informazioni sulla creazione di un Remote Desktop Protocol provider. Il gestore di protocollo viene implementato come server COM e registrato in un percorso cercato all'avvio del Servizi Desktop remoto servizio.
ms.assetid: 9a3e6d5c-464f-4227-a06f-16eb8ed1079e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a7905bfcc623174aca9152f0807a867112aee1a0c54976db810b87f8b3408f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118856217"
---
# <a name="creating-a-remote-desktop-protocol-provider"></a>Creazione di un provider di Remote Desktop Protocol

Le sezioni seguenti contengono informazioni sulla creazione di un Remote Desktop Protocol provider. Il gestore di protocollo viene implementato come server COM e registrato in un percorso cercato all'avvio del Servizi Desktop remoto servizio.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Registrazione di Protocol Manager](registering-the-custom-protocol.md)
</dt> <dd>

È necessario creare almeno una voce del valore del Registro di sistema per il gestore di protocolli in modo che il Servizi Desktop remoto possa crearne un'istanza.

</dd> <dt>

[Sequenza di chiamate al metodo](method-call-sequence.md)
</dt> <dd>

Il Servizi Desktop remoto e il provider di protocolli si chiamano a vicenda in sequenze chiaramente definite.

</dd> </dl>

-   [Registrazione di Protocol Manager](registering-the-custom-protocol.md)
-   [Sequenza di chiamate al metodo](method-call-sequence.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Remote Desktop Protocol Provider API](custom-remote-desktop-protocols.md)
</dt> <dt>

[Uso di Servizi Desktop remoto](using-terminal-services.md)
</dt> </dl>

 

 




