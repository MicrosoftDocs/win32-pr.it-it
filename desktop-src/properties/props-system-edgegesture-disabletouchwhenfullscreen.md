---
description: Impedisce comportamenti dei movimenti di bordo quando una finestra dell'applicazione è attiva e in modalità schermo intero (oppure è attiva una finestra di proprietà).
ms.assetid: F4242C05-181B-44FC-BE6C-8ABB76079981
title: System. EdgeGesture. DisableTouchWhenFullscreen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 208962f11b96420a8e0ef771ada846a3f802e815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317993"
---
# <a name="systemedgegesturedisabletouchwhenfullscreen"></a><span data-ttu-id="d2781-103">System. EdgeGesture. DisableTouchWhenFullscreen</span><span class="sxs-lookup"><span data-stu-id="d2781-103">System.EdgeGesture.DisableTouchWhenFullscreen</span></span>

<span data-ttu-id="d2781-104">Impedisce comportamenti dei movimenti di bordo quando una finestra dell'applicazione è attiva e in modalità schermo intero (oppure è attiva una finestra di proprietà).</span><span class="sxs-lookup"><span data-stu-id="d2781-104">Prevents edge gesture behaviors when an application window is active and in full-screen mode (or an owned window is active).</span></span>

> [!Note]  
> <span data-ttu-id="d2781-105">In modalità schermo intero, le dimensioni della finestra dell'applicazione corrispondono alla risoluzione dello schermo.</span><span class="sxs-lookup"><span data-stu-id="d2781-105">In full-screen mode, the size of the application window matches the screen resolution.</span></span>

 

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="d2781-106">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="d2781-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.EdgeGesture.DisableTouchWhenFullscreen
   shellPKey = PKEY_EdgeGesture_DisableTouchWhenFullscreen
   formatID = 32CE38B2-2C9A-41B1-9BC5-B3784394AA44
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a><span data-ttu-id="d2781-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2781-107">Remarks</span></span>

<span data-ttu-id="d2781-108">In Windows 8 le interazioni utente con i bordi dello schermo visualizzano l'interfaccia utente del sistema, ad esempio le barre dell'app, gli accessi e le app in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d2781-108">In Windows 8, user interactions with the edges of the screen display system UI such as app bars, charms, and running apps.</span></span>

<span data-ttu-id="d2781-109">Per le applicazioni remote a schermo intero, questo comportamento dell'interfaccia utente nel computer locale potrebbe sostituire e interferire con l'interfaccia utente della sessione remota.</span><span class="sxs-lookup"><span data-stu-id="d2781-109">For full-screen, remote applications, this UI behavior on the local machine might override and interfere with the UI of the remote session.</span></span> <span data-ttu-id="d2781-110">Questa proprietà consente a un'applicazione di disabilitare l'interfaccia utente perimetrale nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="d2781-110">This property enables an application to disable the edge UI on the local machine.</span></span>

<span data-ttu-id="d2781-111">Per disabilitare l'interfaccia utente di Edge, impostare questa proprietà su VARIANT \_ true.</span><span class="sxs-lookup"><span data-stu-id="d2781-111">To disable edge UI, set this property to VARIANT\_TRUE.</span></span> <span data-ttu-id="d2781-112">Il valore predefinito è VARIANT \_ false.</span><span class="sxs-lookup"><span data-stu-id="d2781-112">The default value is VARIANT\_FALSE.</span></span>

<span data-ttu-id="d2781-113">Questa proprietà non ha alcun effetto sulle app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="d2781-113">This property has no effect on Windows Store apps.</span></span>

<span data-ttu-id="d2781-114">Nell'esempio seguente viene illustrato come impostare i comportamenti dell'interfaccia utente di Edge.</span><span class="sxs-lookup"><span data-stu-id="d2781-114">The following example shows how to set edge UI behaviors.</span></span>


```
HRESULT SetTouchDisableProperty(HWND hwnd, BOOL fDisableTouch)
{
    IPropertyStore* pPropStore;
    HRESULT hrReturnValue = SHGetPropertyStoreForWindow(hwnd, IID_PPV_ARGS(&pPropStore));
    if (SUCCEEDED(hrReturnValue))
    {
        PROPVARIANT var;
        var.vt = VT_BOOL;
        var.boolVal = fDisableTouch ? VARIANT_TRUE : VARIANT_FALSE;
        hrReturnValue = pPropStore->SetValue(PKEY_EdgeGesture_DisableTouchWhenFullscreen, var);
        pPropStore->Release();
    }
    return hrReturnValue;
}
```



## <a name="related-topics"></a><span data-ttu-id="d2781-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d2781-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2781-116">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="d2781-116">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="d2781-117">searchInfo</span><span class="sxs-lookup"><span data-stu-id="d2781-117">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="d2781-118">typeInfo</span><span class="sxs-lookup"><span data-stu-id="d2781-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> </dl>

 

 
