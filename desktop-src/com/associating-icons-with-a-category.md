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
# <a name="associating-icons-with-a-category"></a><span data-ttu-id="59701-103">Associazione di icone a una categoria</span><span class="sxs-lookup"><span data-stu-id="59701-103">Associating Icons with a Category</span></span>

<span data-ttu-id="59701-104">La creazione di un'interfaccia utente che consente all'utente di selezionare le categorie di componenti all'interno di una categoria richiede la possibilità di visualizzare un'immagine significativa per una determinata categoria.</span><span class="sxs-lookup"><span data-stu-id="59701-104">Building a user interface that allows the user to select component categories within a category requires the ability to display a meaningful image for a particular category.</span></span> <span data-ttu-id="59701-105">Per associare un'icona a una categoria di componenti, creare una chiave per la categoria CATId e popolare la chiave con una sottochiave [DefaultIcon](defaulticon.md) .</span><span class="sxs-lookup"><span data-stu-id="59701-105">To associate an icon with a component category, create a key for the category's CATID and populate that key with a [DefaultIcon](defaulticon.md) subkey.</span></span> <span data-ttu-id="59701-106">La voce del registro di sistema è la seguente:</span><span class="sxs-lookup"><span data-stu-id="59701-106">The registry entry is as follows:</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\DefaultIcon = "c:\hello\icons.dll,1"
 
```

<span data-ttu-id="59701-107">Il nome file a cui fa riferimento la chiave DefaultIcon può essere un file EXE o DLL (DLL di sole risorse).</span><span class="sxs-lookup"><span data-stu-id="59701-107">The filename referenced by the DefaultIcon key can be either an EXE or a DLL file (resource-only DLL).</span></span>

<span data-ttu-id="59701-108">Per associare una piccola bitmap della casella degli strumenti 16x16 a una categoria di componenti, creare una chiave nel **\_ \_ \\ CLSID radice delle classi HKEY** per il CATID della categoria e popolare tale chiave con una sottochiave [ToolboxBitmap32](toolboxbitmap32.md) , come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="59701-108">To associate a small 16x16 "toolbox bitmap" with a component category, create a key in **HKEY\_CLASSES\_ROOT\\CLSID** for the category's CATID and populate that key with a [ToolBoxBitmap32](toolboxbitmap32.md) subkey, as shown in the following example:</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\ToolBoxBitmap32 = "c:\goodbye\mycomponent.dll,42"
 
```

<span data-ttu-id="59701-109">Il nome file a cui fa riferimento la chiave [ToolboxBitmap32](toolboxbitmap32.md) può essere anche un file exe o DLL (dll di sole risorse).</span><span class="sxs-lookup"><span data-stu-id="59701-109">The filename referenced by the [ToolBoxBitmap32](toolboxbitmap32.md) key can also be an EXE or DLL file (resource-only DLL).</span></span>

## <a name="related-topics"></a><span data-ttu-id="59701-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="59701-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59701-111">Categorizzazione in base alle funzionalità del componente</span><span class="sxs-lookup"><span data-stu-id="59701-111">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="59701-112">Categorizzazione in base alle funzionalità del contenitore</span><span class="sxs-lookup"><span data-stu-id="59701-112">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="59701-113">Classi e associazioni predefinite</span><span class="sxs-lookup"><span data-stu-id="59701-113">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="59701-114">Definizione delle categorie di componenti</span><span class="sxs-lookup"><span data-stu-id="59701-114">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="59701-115">**ICatInformation**</span><span class="sxs-lookup"><span data-stu-id="59701-115">**ICatInformation**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
</dt> <dt>

[<span data-ttu-id="59701-116">**ICatRegister**</span><span class="sxs-lookup"><span data-stu-id="59701-116">**ICatRegister**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatregister)
</dt> <dt>

[<span data-ttu-id="59701-117">Gestione categorie di componenti</span><span class="sxs-lookup"><span data-stu-id="59701-117">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




