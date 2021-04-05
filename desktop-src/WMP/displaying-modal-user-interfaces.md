---
title: Visualizzazione di interfacce utente modali
description: Visualizzazione di interfacce utente modali
ms.assetid: 748a8db7-159d-4043-beac-e0516327bcef
keywords:
- Plug-in di Windows Media Player, visualizzazione di finestre di dialogo e finestre di messaggio
- plug-in, visualizzazione di finestre di dialogo e finestre di messaggio
- plug-in dell'interfaccia utente, visualizzazione di finestre di dialogo e finestre di messaggio
- Plug-in dell'interfaccia utente, visualizzazione di finestre di dialogo e finestre di messaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d96387ca46864064c7b6ff7b9cd3dba8187eed0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714527"
---
# <a name="displaying-modal-user-interfaces"></a>Visualizzazione di interfacce utente modali

I plug-in dell'interfaccia utente non devono visualizzare le finestre di dialogo o le finestre di messaggio modali in risposta alle chiamate al metodo da Windows Media Player. Ad esempio, non visualizzare una finestra di messaggio dall'implementazione di **IWMPPluginUI:: create**.

Se è necessario visualizzare una finestra di dialogo o una finestra di messaggio da un'implementazione del metodo del plug-in dell'interfaccia utente chiamata dal lettore, è necessario attenersi alla procedura seguente:

1.  Registrare un nuovo messaggio della finestra usando **RegisterWindowMessage**.
2.  Inviare il messaggio della finestra registrato nella finestra del plug-in dell'interfaccia utente usando **PostMessage**.
3.  Visualizza la finestra di dialogo o la finestra di messaggio dal gestore di messaggi per il nuovo messaggio della finestra.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica del plug-in dell'interfaccia utente**](ui-plug-in-overview.md)
</dt> </dl>

 

 




