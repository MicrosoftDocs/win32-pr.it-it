---
title: Personalizzazione del plug-in dell'interfaccia utente
description: Personalizzazione del plug-in dell'interfaccia utente
ms.assetid: d961ed18-ba14-45af-90d3-b1e38dc53180
keywords:
- Plug-in di Windows Media Player, personalizzazione
- plug-in, personalizzazione
- plug-in dell'interfaccia utente, personalizzazione
- Plug-in dell'interfaccia utente, personalizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4572c4ce5102443c3100ddd20719fe17fe62ffc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045123"
---
# <a name="customizing-the-ui-plug-in"></a>Personalizzazione del plug-in dell'interfaccia utente

A questo punto, il progetto è pronto per la personalizzazione. È possibile modificare l'implementazione generata dalla procedura guidata dell'interfaccia **IWMPPluginUI** , è possibile aggiungere un'interfaccia utente alla classe **CPluginWindow** ed è possibile implementare una pagina delle proprietà nella classe **CPropertyDialog** . Se il plug-in è configurato per l'ascolto di eventi di Windows Media Player, la procedura guidata avrà generato implementazioni predefinite o vuote di tutti i gestori eventi necessari, che è possibile modificare o creare.

Il tipo di plug-in e le funzionalità supportate sono indicati da un valore archiviato nel registro di sistema di Windows. La procedura guidata genera un file con estensione rgs che contiene le informazioni per la registrazione del plug-in. Il valore "Capabilities" in questo file è l'equivalente decimale di un valore booleano o delle costanti del tipo di plug-in e dei flag di plug-in definiti in wmpplug. h. Sebbene questo valore sia determinato dalle opzioni selezionate nella procedura guidata, è necessario modificarlo se si desidera creare un plug-in con più set di impostazioni o uno a cui è possibile inviare elementi multimediali o playlist.

Quando si modifica ed estende il codice del plug-in, è possibile compilare e registrare la DLL in modo che sia possibile testare il plug-in in Windows Media Player.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un plug-in dell'interfaccia utente**](building-a-ui-plug-in.md)
</dt> </dl>

 

 




