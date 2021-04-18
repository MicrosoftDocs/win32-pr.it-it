---
description: Questo argomento descrive come usare le interfacce a livello di pagina che consentono di accedere al contenuto di una pagina in un OM XPS.
ms.assetid: 7127ee28-eca9-4e0e-a27a-9051eb105b27
title: Utilizzo di interfacce di pagine XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8350409f2f436cc4ec2293e735c3f020b49bea68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313997"
---
# <a name="working-with-xps-om-page-interfaces"></a>Utilizzo di interfacce di pagine XPS OM

Questo argomento descrive come usare le interfacce a livello di pagina che consentono di accedere al contenuto di una pagina in un OM XPS.



| Nome interfaccia                                                                                                                                                                              | Interfacce figlio logiche                                                                                                                                                                                            | Descrizione                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/>                                                                                                                                                 | [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/>                                                                         | Oggetto radice del contenuto della pagina.<br/> Questo oggetto rappresenta una parte del documento.<br/>                                                |
| [**IXpsOMShareable**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable)<br/>                                                                                                                                       | [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> [**IXpsOMMatrixTransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)<br/> [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)<br/> [**IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush)<br/> | Le interfacce che derivano dall'interfaccia [**IXpsOMShareable**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable) possono essere archiviate in un dizionario risorse e condivise.<br/> |
| [**IXpsOMRemoteDictionaryResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource)<br/> [**IXpsOMRemoteDictionaryResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)<br/> | [**IXpsOMDictionary**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)<br/>                                                                                                                                                             | Contiene un dizionario risorse.<br/>                                                                                                         |
| [**IXpsOMDictionary**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)<br/>                                                                                                                                     | nessuno<br/>                                                                                                                                                                                                     | Fa riferimento alle risorse condivise da altri oggetti.<br/>                                                                              |
| [**IXpsOMStoryFragmentsResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource)<br/>                                                                                                             | nessuno<br/>                                                                                                                                                                                                     | Consente di accedere al contenuto del flusso di risorse della parte StoryFragments del documento.<br/>                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IXpsOMDictionary**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)
</dt> <dt>

[**IXpsOMDocumentStructureResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)
</dt> <dt>

[**Interfaccia IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**Interfaccia IXpsOMRemoteDictionaryResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource)
</dt> <dt>

[**Interfaccia IXpsOMRemoteDictionaryResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)
</dt> <dt>

[**Interfaccia IXpsOMStoryFragmentsResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource)
</dt> </dl>

 

 




