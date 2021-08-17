---
title: Implementazione di CPluginWindow
description: Implementazione di CPluginWindow
ms.assetid: b22723ce-f373-43b1-a098-86a8dbcf485e
keywords:
- Windows Media Player plug-in, classe CPluginWindow
- plug-in, classe CPluginWindow
- plug-in dell'interfaccia utente, classe CPluginWindow
- Plug-in dell'interfaccia utente, classe CPluginWindow
- Classe CPluginWindow
- Guida per programmatori, plug-in dell'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6364d991fb219678d4f64b09ae4cd3df2526e77797093dcfff3a8dbce7f36101
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748136"
---
# <a name="implementing-cpluginwindow"></a>Implementazione di CPluginWindow

La classe CPluginWindow fornisce l'interfaccia utente al plug-in. Nel caso del plug-in dell'interfaccia utente di  ricerca, questa classe contiene il codice per il pulsante Cerca e il codice che avvia la pagina di ricerca quando si fa clic sul pulsante.

La procedura guidata fornisce un'implementazione di base di CPluginWindow nel file di intestazione CPluginWindow.h. Per semplicità, il plug-in dell'interfaccia utente di ricerca modificherà direttamente questo file, anche se in genere le aggiunte estese vengono inserite in un file CPluginWindow.cpp separato.

Le sezioni seguenti descrivono cosa è necessario fare per implementare CPluginWindow:

-   [Mappa messaggi](the-message-map.md)
-   [Costruttore](the-constructor.md)
-   [Metodo OnPaint](the-onpaint-method.md)
-   [Metodo OnCreate](the-oncreate-method.md)
-   [Metodo OnSearch](the-onsearch-method.md)
-   [Metodo LaunchPage](the-launchpage-method.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia utente di programmazione dei plug-in**](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




