---
description: Le interfacce del documento forniscono l'accesso ai componenti del pacchetto XPS che determinano la struttura di un documento in un OM XPS.
ms.assetid: 3302d164-81ad-4198-a116-f967e7a14147
title: Interfacce del documento XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc191c4c0b8ec5571331022321a8ae829587022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310148"
---
# <a name="xps-om-document-interfaces"></a>Interfacce del documento XPS OM

Le interfacce del documento forniscono l'accesso ai componenti del pacchetto XPS che determinano la struttura di un documento in un OM XPS. Nella tabella seguente sono elencate le interfacce del documento.



| Nome interfaccia                                                      | Interfacce figlio logiche                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> | [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>           | Rappresenta un set di documenti associati in un elenco ordinato.<br/> Le interfacce figlio vengono raccolte in un'interfaccia [**IXpsOMDocumentCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection) .<br/>                                                                                                                                                                                                  |
| [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                 | [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> | Rappresenta una singola parte di FixedDocument e associa la raccolta di riferimenti di pagina delle pagine in un documento.<br/> Le interfacce figlio vengono raccolte in un'interfaccia [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) .<br/> La struttura del documento è esposta in un'interfaccia [**IXpsOMDocumentStructureResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource) .<br/> |
| [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/>       | [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/>                   | Versione virtualizzata ridotta di una pagina nel documento. Un riferimento alla pagina descrive le caratteristiche principali della pagina, ad esempio le dimensioni, ma non include il contenuto della pagina.<br/>                                                                                                                                                                                             |
| [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)<br/>     | nessuno<br/>                                               | Raccolta di oggetti della pagina che sono destinazioni di collegamento ipertestuale.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**IXpsOMPartResources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/>       | nessuno<br/>                                               | Raccolta delle risorse della parte associate a una pagina.<br/>                                                                                                                                                                                                                                                                                                                                |



 

## <a name="contents"></a>Contenuto

-   L'utilizzo delle [interfacce IXpsOMDocumentSequence](working-with-xpsomdocumentsequence-interfaces.md) contiene informazioni sull'utilizzo delle interfacce seguenti:
    -   [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
    -   [**IXpsOMDocumentCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)
-   L'utilizzo delle [interfacce IXpsOMDocument](working-with-xpsomdocument-interfaces.md) contiene informazioni sull'utilizzo delle interfacce seguenti:
    -   [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
    -   [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)
    -   [**IXpsOMDocumentStructureResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)
-   L'utilizzo delle [interfacce IXpsOMPageReference](working-with-xpsompagereference-interfaces.md) contiene informazioni sull'utilizzo delle interfacce seguenti:
    -   [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
    -   [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
    -   [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)
    -   [**IXpsOMPartResources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)

 

 




