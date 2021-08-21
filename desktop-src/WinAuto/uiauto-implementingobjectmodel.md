---
title: Pattern di controllo ObjectModel
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IObjectModelProvider, incluse le informazioni sui metodi. Il pattern di controllo ObjectModel viene usato per esporre un puntatore al modello a oggetti sottostante di un documento.
ms.assetid: 90A6937E-0E98-41EF-8EEB-E23CB71510E4
keywords:
- Automazione interfaccia utente,implementazione del pattern di controllo ObjectModel
- Automazione interfaccia utente,Pattern di controllo ObjectModel
- Automazione interfaccia utente,IObjectModelProvider
- IObjectModelProvider
- implementazione Automazione interfaccia utente pattern di controllo ObjectModel
- Pattern di controllo ObjectModel
- pattern di controllo, IObjectModelProvider
- pattern di controllo, implementazione Automazione interfaccia utente ObjectModel
- pattern di controllo, ObjectModel
- interfacce, IObjectModelProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62081f8fb841e7827f589fd2441c7b6411810f9a71c1c1962a0dfcf8b0e37180
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114994"
---
# <a name="objectmodel-control-pattern"></a>Pattern di controllo ObjectModel

Vengono descritte le linee guida e le convenzioni per [**l'implementazione di IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider), incluse le informazioni sui metodi. Il **pattern di controllo ObjectModel** viene usato per esporre un puntatore al modello a oggetti sottostante di un documento.

Molte applicazioni implementano modelli a oggetti complessi che aggiungono valore oltre a quanto Automazione interfaccia utente Microsoft. Questo pattern di controllo consente a un client di spostarsi da un Automazione interfaccia utente elemento nel modello a oggetti sottostante.

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **IObjectModelProvider**](#required-members-for-iobjectmodelprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern **di controllo ObjectModel,** tenere presente le linee guida e le convenzioni seguenti:

-   Il [**metodo IObjectModelProvider::GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) deve restituire un puntatore all'oggetto il più vicino possibile all'elemento dell'interfaccia utente di origine. In un Web browser, ad esempio, un provider Automazione interfaccia utente per un singolo elemento deve restituire un puntatore del modello a oggetti per l'elemento. La restituzione di un puntatore del modello a oggetti per la radice del documento sarebbe molto meno utile.
-   È previsto che il client del pattern di controllo **ObjectModel** abbia l'IID per l'interfaccia che sta cercando, motivo per cui è sufficiente restituire un semplice [**puntatore IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)
-   Poiché Automazione interfaccia utente esegue il marshalling del puntatore al processo client, il provider deve aspettarsi che il client accedono al modello a oggetti usando procedure COM (Standard Component Object Model).

## <a name="required-members-for-iobjectmodelprovider"></a>Membri obbligatori per **IObjectModelProvider**

Il metodo seguente è necessario per implementare [**l'interfaccia IObjectModelProvider.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider)



| Membri obbligatori                                                                             | Tipo di membro | Note                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) | Metodo      | Restituisce un puntatore COM al modello a oggetti sottostante. È previsto che il client chiami il [**metodo IUnknown::QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per recuperare puntatori specifici del modello a oggetti. |



 

Questo pattern di controllo non è associato a eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 