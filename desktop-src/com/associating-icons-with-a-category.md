---
title: Associazione di icone a una categoria
description: Associazione di icone a una categoria
ms.assetid: 5e5c3c10-07cf-4a34-9822-97ec940b3117
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c7a662ab3aaf578f037ff246207d03e4fcd688
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044241"
---
# <a name="associating-icons-with-a-category"></a>Associazione di icone a una categoria

La creazione di un'interfaccia utente che consente all'utente di selezionare le categorie di componenti all'interno di una categoria richiede la possibilità di visualizzare un'immagine significativa per una determinata categoria. Per associare un'icona a una categoria di componenti, creare una chiave per la categoria CATId e popolare la chiave con una sottochiave [DefaultIcon](defaulticon.md) . La voce del registro di sistema è la seguente:

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\DefaultIcon = "c:\hello\icons.dll,1"
 
```

Il nome file a cui fa riferimento la chiave DefaultIcon può essere un file EXE o DLL (DLL di sole risorse).

Per associare una piccola bitmap della casella degli strumenti 16x16 a una categoria di componenti, creare una chiave nel **\_ \_ \\ CLSID radice delle classi HKEY** per il CATID della categoria e popolare tale chiave con una sottochiave [ToolboxBitmap32](toolboxbitmap32.md) , come illustrato nell'esempio seguente:

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\ToolBoxBitmap32 = "c:\goodbye\mycomponent.dll,42"
 
```

Il nome file a cui fa riferimento la chiave [ToolboxBitmap32](toolboxbitmap32.md) può essere anche un file exe o DLL (dll di sole risorse).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Categorizzazione in base alle funzionalità del componente](categorizing-by-component-capabilities.md)
</dt> <dt>

[Categorizzazione in base alle funzionalità del contenitore](categorizing-by-container-capabilities.md)
</dt> <dt>

[Classi e associazioni predefinite](default-classes-and-associations.md)
</dt> <dt>

[Definizione delle categorie di componenti](defining-component-categories.md)
</dt> <dt>

[**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
</dt> <dt>

[**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister)
</dt> <dt>

[Gestione categorie di componenti](the-component-categories-manager.md)
</dt> </dl>

 

 




