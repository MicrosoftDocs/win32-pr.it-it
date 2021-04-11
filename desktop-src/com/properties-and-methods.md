---
title: Proprietà e metodi
description: Analogamente a qualsiasi oggetto OLE, un controllo offre la maggior parte delle funzionalità tramite un set di interfacce in ingresso con proprietà e metodi.
ms.assetid: 5a0cdb5d-7e27-40e9-94db-cfda853879c6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 701b100be635fdb8db9cb51f258dc722edd23eca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044381"
---
# <a name="properties-and-methods"></a>Proprietà e metodi

Analogamente a qualsiasi oggetto OLE, un controllo offre la maggior parte delle funzionalità tramite un set di interfacce in ingresso con proprietà e metodi.

Un controllo espone proprietà e metodi tramite l'automazione OLE, in modo che i contenitori possano accedervi sotto il controllo di un linguaggio di programmazione fornito dal contenitore.

Per supportare l'accesso alle proprietà tramite un'interfaccia utente, un controllo fornisce pagine di proprietà, il supporto per \_ le proprietà OLEIVERB, l'esplorazione delle proprietà e la data binding tramite la modifica della proprietà notifica.

-   Tramite le pagine delle proprietà, un controllo può visualizzarne le proprietà, indipendentemente dal relativo contenitore, se necessario.
-   Grazie al supporto \_ delle proprietà OLEIVERB, l'elemento Properties viene visualizzato nel menu del contenitore. Quindi, l'utente finale può selezionare l'elemento **Properties** per visualizzare le pagine delle proprietà del controllo e modificare le proprietà.
-   Per esplorazione di proprietà è supportato un contenitore in grado di visualizzare le proprietà del controllo come parte di una finestra delle proprietà più ampia che può includere proprietà di diversi controlli nel contenitore.
-   Tramite la notifica delle modifiche alle proprietà, un controllo può notificare a un client che le relative proprietà sono state modificate, consentendo al client di eseguire le azioni necessarie di conseguenza.

Per altre informazioni, vedere i seguenti argomenti:

-   [Proprietà del controllo](control-properties.md)
-   [Metodi di controllo](control-methods.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controlli ActiveX](activex-controls.md)
</dt> <dt>

[Pagine delle proprietà e finestre delle proprietà](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




