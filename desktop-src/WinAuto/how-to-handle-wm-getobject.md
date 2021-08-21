---
title: Come gestire i WM_GETOBJECT
description: Quando riceve un messaggio WM GETOBJECT che contiene OBJID CLIENT, il server deve restituire un puntatore all'oggetto \_ \_ che implementa IAccessible.
ms.assetid: 455398b7-f748-4ab0-8953-3f74439e44f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f066ee42ffaeee2d585ac5480e5af31acf14c87ba9994d3d338b65e6cf427a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052727"
---
# <a name="how-to-handle-wm_getobject"></a>Come gestire WM \_ GETOBJECT

Quando riceve un messaggio [**WM \_ GETOBJECT**](wm-getobject.md) che contiene [**OBJID \_ CLIENT,**](object-identifiers.md)il server deve restituire un puntatore all'oggetto che implementa [**IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Questo puntatore è un LRESULT ottenuto chiamando [**LresultFromObject.**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) Microsoft Active Accessibility, in combinazione con la libreria Component Object Model (COM), esegue il marshalling appropriato e passa il puntatore di interfaccia **IAccessible** dal server al client.

I server devono gestire correttamente il conteggio dei riferimenti sull'oggetto accessibile. Tenere presente che quando si crea un oggetto COM, il conteggio dei riferimenti è 1. [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) incrementa ulteriormente il conteggio dei riferimenti più volte. Tutti i riferimenti creati da **LresultFromObject** vengono rilasciati automaticamente quando l'oggetto non è più necessario, ma il server è responsabile del rilascio del riferimento iniziale e, a meno che non lo faccia, l'oggetto non verrà mai eliminato. Gli esempi nelle sezioni seguenti illustrano come rilasciare riferimenti a oggetti accessibili.

I server gestiscono [**in genere WM \_ GETOBJECT**](wm-getobject.md) in uno dei modi seguenti:

-   [Creare nuovi oggetti accessibili](create-new-accessible-objects.md)
-   [Riutilizzare i puntatori esistenti agli oggetti](reuse-existing-pointers-to-objects.md)
-   [Creare nuove interfacce per lo stesso oggetto](create-new-interfaces-to-the-same-object.md)

> [!Note]  
> In questa sezione come nel resto della documentazione, quando viene illustrato un puntatore a un'interfaccia [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) questo puntatore può essere effettivamente un puntatore a un oggetto proxy che esegue il wrapping **dell'interfaccia IAccessible.** Per altre informazioni sugli oggetti proxy, vedere [Creazione di oggetti proxy.](creating-proxy-objects.md)

 

Per una panoramica di [**WM \_ GETOBJECT,**](wm-getobject.md)vedere [Funzionamento di WM \_ GETOBJECT.](how-wm-getobject-works.md)

 

 




