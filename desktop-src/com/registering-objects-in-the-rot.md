---
title: Registrazione di oggetti nella tabella ROT
description: Registrazione di oggetti nella tabella ROT
ms.assetid: f479c2d1-0c55-4281-8f15-2f957fa03b70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b452ead94a717791910ecceaa5082535bc1b233c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396082"
---
# <a name="registering-objects-in-the-rot"></a>Registrazione di oggetti nella tabella ROT

In genere, quando un client richiede a un server di creare un'istanza dell'oggetto, il server crea in genere un moniker per l'oggetto e lo registra nella tabella degli oggetti in esecuzione (ROT) tramite una chiamata a [**IRunningObjectTable:: Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register).

Quando il server chiama [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) per creare un moniker di file da registrare nella ROT, i server devono passare i nomi di file locali che sono basati su unità e non in formato UNC. In questo modo si garantisce che i dati di confronto del moniker generati dalla chiamata al registro ROT corrispondano a quelli utilizzati durante la ricerca di una ROT sulla parte di un client remoto. Questo perché quando il servizio COM distribuito riceve una richiesta di attivazione per un file locale al server da un client remoto, il file viene convertito in un percorso basato su unità locale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Installazione come applicazione di servizio](installing-as-a-service-application.md)
</dt> <dt>

[Registrazione di una classe durante l'installazione](registering-a-class-at-installation.md)
</dt> <dt>

[Registrazione di un server EXE in esecuzione](registering-a-running-exe-server.md)
</dt> <dt>

[Registrazione automatica](self-registration.md)
</dt> </dl>

 

 




