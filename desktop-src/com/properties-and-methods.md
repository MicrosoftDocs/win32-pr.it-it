---
title: Proprietà e metodi
description: Come qualsiasi oggetto OLE, un controllo fornisce gran parte delle funzionalità tramite un set di interfacce in ingresso con proprietà e metodi.
ms.assetid: 5a0cdb5d-7e27-40e9-94db-cfda853879c6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52dae30453089f235a4e70d7896569ebefcdff9f7f2419b5fc54af88b8563d63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047889"
---
# <a name="properties-and-methods"></a>Proprietà e metodi

Come qualsiasi oggetto OLE, un controllo fornisce gran parte delle funzionalità tramite un set di interfacce in ingresso con proprietà e metodi.

Un controllo espone proprietà e metodi tramite l'automazione OLE in modo che i contenitori possano accedervi sotto il controllo di un linguaggio di programmazione fornito da contenitori.

Per supportare l'accesso alle proprietà tramite un'interfaccia utente, un controllo fornisce pagine delle proprietà, supporto per PROPRIETÀ OLEIVERB, esplorazione per proprietà e data binding tramite notfications di modifica \_ delle proprietà.

-   Tramite le pagine delle proprietà un controllo può visualizzare le relative proprietà, indipendentemente dal relativo contenitore, se necessario.
-   Supportando OLEIVERB \_ PROPERTIES, l'elemento Properties viene visualizzato nel menu del contenitore. L'utente finale può quindi selezionare **l'elemento Proprietà** per visualizzare le pagine delle proprietà del controllo e modificare le proprietà.
-   L'esplorazione per proprietà supporta un contenitore in grado di visualizzare le proprietà del controllo come parte di una finestra delle proprietà più grande che può includere proprietà di diversi controlli nel contenitore.
-   Tramite la notifica di modifica delle proprietà, un controllo può notificare a un client che le relative proprietà sono state modificate, consentendo al client di eseguire le azioni necessarie di conseguenza.

Per altre informazioni, vedere i seguenti argomenti:

-   [Proprietà del controllo](control-properties.md)
-   [Metodi di controllo](control-methods.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[ActiveX Controlli](activex-controls.md)
</dt> <dt>

[Pagine delle proprietà e finestre delle proprietà](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




