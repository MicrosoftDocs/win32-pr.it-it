---
title: Gestione categorie di componenti
description: Gestione categorie di componenti
ms.assetid: bd43ef98-2299-4c8a-9f35-bf9aceb074ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fdf301e1b344bbc2403fd656dd90447ccffc357
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471219"
---
# <a name="the-component-categories-manager"></a>Gestione categorie di componenti

Per facilitare la gestione delle categorie di componenti e garantire la coerenza del registro di sistema, il sistema fornisce il componente Gestione categorie di componenti, un oggetto COM con CLSID \_ StdComponentCategoriesMgr. Questo oggetto COM fornisce le interfacce seguenti:

-   [**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
-   [**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister)

[**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) fornisce metodi per ottenere informazioni sulle categorie implementate o richieste da una determinata classe e fornisce informazioni sulle categorie registrate in un determinato computer.

[**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) fornisce metodi per la registrazione e l'annullamento della registrazione delle informazioni sulle categorie di componenti nel registro di sistema. Sono inclusi i nomi leggibili delle categorie e le categorie implementate o richieste da un determinato componente o classe.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Associazione di icone a una categoria](associating-icons-with-a-category.md)
</dt> <dt>

[Categorizzazione in base alle funzionalità del componente](categorizing-by-component-capabilities.md)
</dt> <dt>

[Categorizzazione in base alle funzionalità del contenitore](categorizing-by-container-capabilities.md)
</dt> <dt>

[Classi e associazioni predefinite](default-classes-and-associations.md)
</dt> <dt>

[Definizione delle categorie di componenti](defining-component-categories.md)
</dt> </dl>

 

 




