---
title: Pattern di controllo ObjectModel
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IObjectModelProvider, incluse informazioni sui metodi. Il pattern di controllo ObjectModel viene usato per esporre un puntatore al modello a oggetti sottostante di un documento.
ms.assetid: 90A6937E-0E98-41EF-8EEB-E23CB71510E4
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo ObjectModel
- Automazione interfaccia utente, pattern di controllo ObjectModel
- Automazione interfaccia utente, IObjectModelProvider
- IObjectModelProvider
- implementazione del pattern di controllo ObjectModel di automazione interfaccia utente
- Pattern di controllo ObjectModel
- pattern di controllo, IObjectModelProvider
- pattern di controllo, implementazione dell'automazione interfaccia utente ObjectModel
- pattern di controllo, ObjectModel
- interfacce, IObjectModelProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ff115233faf19f93963153a0b2a0a1ff52c3f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338335"
---
# <a name="objectmodel-control-pattern"></a>Pattern di controllo ObjectModel

Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider), incluse informazioni sui metodi. Il pattern di controllo **ObjectModel** viene usato per esporre un puntatore al modello a oggetti sottostante di un documento.

Molte applicazioni implementano modelli a oggetti avanzati che aggiungono valore oltre a quello fornito da automazione interfaccia utente Microsoft. Questo pattern di controllo consente a un client di passare da un elemento di automazione interfaccia utente al modello a oggetti sottostante.

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **IObjectModelProvider**](#required-members-for-iobjectmodelprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **ObjectModel** , tenere presenti le linee guida e le convenzioni seguenti:

-   Il metodo [**IObjectModelProvider:: GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) deve restituire un puntatore all'oggetto che è il più vicino possibile all'elemento dell'interfaccia utente di origine. Ad esempio, in un Web browser, un provider di automazione interfaccia utente per un singolo elemento deve restituire un puntatore del modello a oggetti per l'elemento. La restituzione di un puntatore del modello a oggetti per la radice del documento sarebbe molto meno utile.
-   Il client del pattern di controllo **ObjectModel** dovrebbe avere l'IID per l'interfaccia cercata, motivo per cui è sufficiente restituire un semplice puntatore [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .
-   Poiché l'automazione interfaccia utente esegue il marshalling del puntatore al processo client, il provider deve prevedere che il client acceda al modello a oggetti utilizzando le procedure standard Component Object Model (COM).

## <a name="required-members-for-iobjectmodelprovider"></a>Membri obbligatori per **IObjectModelProvider**

Il metodo seguente è necessario per implementare l'interfaccia [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider) .



| Membri obbligatori                                                                             | Tipo di membro | Note                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) | Metodo      | Restituisce un puntatore COM al modello a oggetti sottostante. Si prevede che il client chiami il metodo [**IUnknown:: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per recuperare i puntatori specifici del modello a oggetti. |



 

Questo pattern di controllo non è associato a eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 