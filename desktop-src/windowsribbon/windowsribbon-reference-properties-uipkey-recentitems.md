---
title: UI_PKEY_RecentItems
description: Identifica la proprietà RecentItems dell'interfaccia utente \_ pkey \_ .
ms.assetid: 54e7ad1f-86b3-45e0-a0f4-5ee0d08e9d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a07410d3152fb49b55460ec15c6914c53f3b6850
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299970"
---
# <a name="ui_pkey_recentitems"></a><span data-ttu-id="fb1b5-103">Interfaccia utente \_ pkey \_ RecentItems</span><span class="sxs-lookup"><span data-stu-id="fb1b5-103">UI\_PKEY\_RecentItems</span></span>

<span data-ttu-id="fb1b5-104">Identifica la proprietà RecentItems dell'interfaccia utente \_ pkey \_ .</span><span class="sxs-lookup"><span data-stu-id="fb1b5-104">Identifies the UI\_PKEY\_RecentItems property.</span></span>

```
propertyDescription
   name = UI_PKEY_RecentItems
   shellPKey = UI_PKEY_RecentItems
   formatID = 00000350-7363-696e-8441798acf5aebb7
   propID = 350
   typeInfo
      type = VT_ARRAY | VT_UNKNOWN
```

## <a name="remarks"></a><span data-ttu-id="fb1b5-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb1b5-105">Remarks</span></span>

<span data-ttu-id="fb1b5-106">[Interfaccia utente \_ PKEY \_ aggiunto](windowsribbon-reference-properties-uipkey-pinned.md) viene usato da un'applicazione per eseguire una query sulla matrice di elementi della raccolta di elementi usati di recente (MRU) del [menu dell'applicazione](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="fb1b5-106">[UI\_PKEY\_Pinned](windowsribbon-reference-properties-uipkey-pinned.md) is used by an application to query the array of items in the most recently used (MRU) items collection of the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span> <span data-ttu-id="fb1b5-107">Le informazioni per ogni elemento MRU sono incapsulate in un oggetto [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) e includono le tre chiavi di proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="fb1b5-107">The information for each MRU item is encapsulated in an [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object and includes the following three property keys:</span></span>

-   [<span data-ttu-id="fb1b5-108">\_Etichetta pkey dell'interfaccia utente \_</span><span class="sxs-lookup"><span data-stu-id="fb1b5-108">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)
-   [<span data-ttu-id="fb1b5-109">Interfaccia utente \_ pkey \_ LabelDescription</span><span class="sxs-lookup"><span data-stu-id="fb1b5-109">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)
-   [<span data-ttu-id="fb1b5-110">Interfaccia utente \_ pkey \_ bloccata</span><span class="sxs-lookup"><span data-stu-id="fb1b5-110">UI\_PKEY\_Pinned</span></span>](windowsribbon-reference-properties-uipkey-pinned.md)

<span data-ttu-id="fb1b5-111">L'elenco di elementi MRU viene passato all'applicazione host della barra multifunzione come **SAFEARRAY** di puntatori [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) alle rispettive implementazioni nell'applicazione host.</span><span class="sxs-lookup"><span data-stu-id="fb1b5-111">The list of MRU items is passed to the Ribbon host application as a **SAFEARRAY** of [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) pointers to respective implementations in the host application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb1b5-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fb1b5-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb1b5-113">Proprietà stato</span><span class="sxs-lookup"><span data-stu-id="fb1b5-113">State Properties</span></span>](windowsribbon-reference-properties-state.md)
</dt> </dl>

 

 