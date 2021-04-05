---
title: Implementazione di CPluginWindow
description: Implementazione di CPluginWindow
ms.assetid: b22723ce-f373-43b1-a098-86a8dbcf485e
keywords:
- Plug-in di Windows Media Player, classe CPluginWindow
- plug-in, classe CPluginWindow
- plug-in dell'interfaccia utente, classe CPluginWindow
- Plug-in dell'interfaccia utente, classe CPluginWindow
- Classe CPluginWindow
- Guida per programmatori, plug-in dell'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe282b0c6cefbcac8fbce76ca53f8e0efaf64874
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709073"
---
# <a name="implementing-cpluginwindow"></a>Implementazione di CPluginWindow

La classe CPluginWindow fornisce l'interfaccia utente per il plug-in. Nel caso del plug-in di ricerca dell'interfaccia utente, questa classe contiene il codice per il pulsante **Cerca** e il codice che avvia la pagina di ricerca quando si fa clic sul pulsante.

La procedura guidata fornisce un'implementazione di base di CPluginWindow nel file di intestazione CPluginWindow. h. Per semplificare le operazioni, il plug-in di ricerca dell'interfaccia utente modificherà direttamente il file, anche se le aggiunte estese verrebbero normalmente inserite in un file CPluginWindow. cpp separato.

Nelle sezioni seguenti vengono descritte le operazioni necessarie per implementare CPluginWindow:

-   [Mappa messaggi](the-message-map.md)
-   [Costruttore](the-constructor.md)
-   [Metodo OnPaint](the-onpaint-method.md)
-   [Metodo OnCreate](the-oncreate-method.md)
-   [Metodo OnSearch](the-onsearch-method.md)
-   [Metodo LaunchPage](the-launchpage-method.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida alla programmazione di plug-in dell'interfaccia utente**](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




