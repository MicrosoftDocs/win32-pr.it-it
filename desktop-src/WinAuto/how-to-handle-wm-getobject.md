---
title: Come gestire WM_GETOBJECT
description: Quando riceve un messaggio WM \_ GetObject che contiene il \_ client ObjID, il server deve restituire un puntatore all'oggetto che implementa IAccessible.
ms.assetid: 455398b7-f748-4ab0-8953-3f74439e44f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6223d75339f537ccf1939f9c9af46a42aa47bfdb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711716"
---
# <a name="how-to-handle-wm_getobject"></a>Come gestire WM \_ GETobject

Quando riceve un messaggio [**WM \_ GetObject**](wm-getobject.md) che contiene il [**\_ client ObjID**](object-identifiers.md), il server deve restituire un puntatore all'oggetto che implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). Questo puntatore è un LRESULT ottenuto chiamando [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject). Microsoft Active Accessibility, insieme alla libreria di Component Object Model (COM), esegue il marshalling appropriato e passa il puntatore all'interfaccia **IAccessible** dal server al client.

I server devono gestire correttamente il conteggio dei riferimenti per l'oggetto accessibile. Tenere presente che quando si crea un oggetto COM, il conteggio dei riferimenti è 1. [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) incrementa il conteggio dei riferimenti più volte. Tutti i riferimenti creati da **LresultFromObject** vengono rilasciati automaticamente quando l'oggetto non è più necessario, ma il server è responsabile del rilascio del riferimento iniziale e, a meno che non lo faccia, l'oggetto non verrà mai eliminato definitivamente. Negli esempi nelle sezioni seguenti viene illustrato come rilasciare i riferimenti agli oggetti accessibili.

I server in genere gestiscono [**WM \_ GetObject**](wm-getobject.md) in uno dei modi seguenti:

-   [Creare nuovi oggetti accessibili](create-new-accessible-objects.md)
-   [Riutilizza puntatori esistenti a oggetti](reuse-existing-pointers-to-objects.md)
-   [Crea nuove interfacce per lo stesso oggetto](create-new-interfaces-to-the-same-object.md)

> [!Note]  
> In questa sezione, come nel resto della documentazione, quando viene discusso un puntatore a un'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , questo puntatore può essere effettivamente un puntatore a un oggetto proxy che esegue il wrapping dell'interfaccia **IAccessible** . Per ulteriori informazioni sugli oggetti proxy, vedere [creazione di oggetti proxy](creating-proxy-objects.md).

 

Per una panoramica di [**WM \_ GetObject**](wm-getobject.md), vedere funzionamento di [WM \_ GetObject](how-wm-getobject-works.md).

 

 




