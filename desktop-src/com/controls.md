---
title: Controlli (COM)
description: Controlli
ms.assetid: 73947c81-6727-4112-9da0-efa60360f458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f440fff8f855f70c1a5ab3df78a6f6f6ed365ea
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104339993"
---
# <a name="controls-com"></a>Controlli (COM)

Un controllo ActiveX è in realtà un altro termine per l'oggetto OLE o più specificamente un oggetto COM. In altre parole, un controllo, almeno, è un oggetto COM che supporta l'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) ed è anche autoregistrato. Tramite [**IUnknown:: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) un contenitore può gestire la durata del controllo e individuare in modo dinamico l'entità completa della funzionalità di un controllo in base alle interfacce disponibili. Questo consente a un controllo di implementare il minor numero di funzionalità necessario, anziché supportare un numero elevato di interfacce che in realtà non eseguono alcuna operazione. In breve, questo requisito minimo per nient'altro che **IUnknown** consente a qualsiasi controllo di essere il più leggero possibile.

In breve, oltre a [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) e registrazione automatica, non sono previsti altri requisiti per un controllo. Esistono, tuttavia, le convenzioni che devono essere seguite per quanto riguarda il supporto di un'interfaccia in termini di funzionalità fornite al contenitore dal controllo. Questa sezione descrive quindi il significato di un controllo per supportare effettivamente un'interfaccia, oltre a metodi, proprietà ed eventi che un controllo deve fornire come linea di base se ha l'opportunità di supportare metodi, proprietà ed eventi.

Per altre informazioni, vedere i seguenti argomenti:

-   [Registrazione automatica per i controlli](self-registration-for-controls.md)
-   [Quale supporto per un'interfaccia significa](what-support-for-an-interface-means.md)
-   [Interfacce di persistenza](persistence-interfaces.md)
-   [Metodi facoltativi nelle interfacce di controllo](optional-methods-in-control-interfaces.md)
-   [Opzioni di class factory](class-factory-options.md)
-   [Esposizione di proprietà tramite IDispatch](properties.md)
-   [Esposizione di metodi tramite IDispatch](exposing-methods-through-idispatch.md)
-   [Eventi nei controlli](events-in-controls.md)
-   [Pagine delle proprietà](property-pages.md)
-   [Proprietà di ambiente per i controlli](ambient-properties-for-controls.md)
-   [Uso della funzionalità del contenitore](using-the-container-s-functionality.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Linee guida per il controllo ActiveX e il controllo del contenitore](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 




