---
description: Disabilita la possibilità di aggiungere un collegamento o una finestra alla barra delle applicazioni o al menu Start. Questa proprietà rende anche l'elemento non idoneo per l'inclusione nell'elenco dei menu Start (MFU) usato più di frequente.
ms.assetid: 86239BF8-BCFC-4e76-BF94-5ABA4639562C
title: System. AppUserModel. PreventPinning
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7804c615bcb35909610b06622bd25fe3dccdd0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882209"
---
# <a name="systemappusermodelpreventpinning"></a><span data-ttu-id="afa58-104">System. AppUserModel. PreventPinning</span><span class="sxs-lookup"><span data-stu-id="afa58-104">System.AppUserModel.PreventPinning</span></span>

<span data-ttu-id="afa58-105">Disabilita la possibilità di aggiungere un collegamento o una finestra alla barra delle applicazioni o al menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="afa58-105">Disables the ability of a shortcut or window to be pinned to the taskbar or the **Start** menu.</span></span> <span data-ttu-id="afa58-106">Questa proprietà rende anche l'elemento non idoneo per l'inclusione nell'elenco dei menu **Start** (MFU) usato più di frequente.</span><span class="sxs-lookup"><span data-stu-id="afa58-106">This property also makes the item ineligible for inclusion in the **Start** menu's Most Frequently Used (MFU) list.</span></span>

<span data-ttu-id="afa58-107">Questa proprietà deve essere impostata su una finestra prima della [proprietà \_ \_ ID AppUserModel pkey](./props-system-appusermodel-id.md) .</span><span class="sxs-lookup"><span data-stu-id="afa58-107">This property must be set on a window before the [PKEY\_AppUserModel\_ID](./props-system-appusermodel-id.md) property.</span></span> <span data-ttu-id="afa58-108">Una volta \_ impostata la proprietà pkey AppUserModel \_ ID, le modifiche apportate a [pkey \_ AppUserModel \_ PreventPinning]() vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="afa58-108">After the PKEY\_AppUserModel\_ID property is set, changes to [PKEY\_AppUserModel\_PreventPinning]() are ignored.</span></span>

<span data-ttu-id="afa58-109">Per ulteriori informazioni sugli ID del modello utente dell'applicazione (AppUserModelIDs) e altri metodi di esclusione di un elemento da aggiungere alla barra delle applicazioni e dall'inclusione MFU, vedere [ID modello utente applicazione (AppUserModelIDs)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="afa58-109">For more information about Application User Model IDs (AppUserModelIDs) and other methods of excluding an item from being pinned to the taskbar and from MFU inclusion, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span>

<span data-ttu-id="afa58-110">Per impostare questa proprietà in una finestra, usare [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) per recuperare l'archivio delle proprietà della finestra e usare i metodi dell'oggetto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) recuperato per impostare la proprietà [System. AppUserModel. PreventPinning]() di tale finestra.</span><span class="sxs-lookup"><span data-stu-id="afa58-110">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.PreventPinning]() property of that window.</span></span>

<span data-ttu-id="afa58-111">Se si imposta questa proprietà, le proprietà seguenti verranno ignorate:</span><span class="sxs-lookup"><span data-stu-id="afa58-111">Setting this property causes the following properties to be ignored:</span></span>

-   [<span data-ttu-id="afa58-112">System. AppUserModel. RelaunchCommand</span><span class="sxs-lookup"><span data-stu-id="afa58-112">System.AppUserModel.RelaunchCommand</span></span>](./props-system-appusermodel-relaunchcommand.md)
-   [<span data-ttu-id="afa58-113">System. AppUserModel. RelaunchDisplayNameResource</span><span class="sxs-lookup"><span data-stu-id="afa58-113">System.AppUserModel.RelaunchDisplayNameResource</span></span>](./props-system-appusermodel-relaunchdisplaynameresource.md)
-   [<span data-ttu-id="afa58-114">System. AppUserModel. RelaunchIconResource</span><span class="sxs-lookup"><span data-stu-id="afa58-114">System.AppUserModel.RelaunchIconResource</span></span>](./props-system-appusermodel-relaunchiconresource.md)

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="afa58-115">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="afa58-115">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.PreventPinning
   shellPKey = PKEY_AppUserModel_PreventPinning
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="afa58-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="afa58-116">Remarks</span></span>

<span data-ttu-id="afa58-117">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="afa58-117">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="afa58-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="afa58-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afa58-119">ID modello utente applicazione (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="afa58-119">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="afa58-120">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="afa58-120">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="afa58-121">**SHGetPropertyStoreForWindow**</span><span class="sxs-lookup"><span data-stu-id="afa58-121">**SHGetPropertyStoreForWindow**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> <dt>

[<span data-ttu-id="afa58-122">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="afa58-122">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="afa58-123">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="afa58-123">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="afa58-124">searchInfo</span><span class="sxs-lookup"><span data-stu-id="afa58-124">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="afa58-125">labelInfo</span><span class="sxs-lookup"><span data-stu-id="afa58-125">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="afa58-126">typeInfo</span><span class="sxs-lookup"><span data-stu-id="afa58-126">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="afa58-127">displayInfo</span><span class="sxs-lookup"><span data-stu-id="afa58-127">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="afa58-128">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="afa58-128">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="afa58-129">stringFormat</span><span class="sxs-lookup"><span data-stu-id="afa58-129">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="afa58-130">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="afa58-130">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="afa58-131">numberFormat</span><span class="sxs-lookup"><span data-stu-id="afa58-131">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="afa58-132">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="afa58-132">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="afa58-133">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="afa58-133">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="afa58-134">enum</span><span class="sxs-lookup"><span data-stu-id="afa58-134">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="afa58-135">enumRange</span><span class="sxs-lookup"><span data-stu-id="afa58-135">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="afa58-136">image</span><span class="sxs-lookup"><span data-stu-id="afa58-136">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="afa58-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="afa58-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="afa58-138">editControl</span><span class="sxs-lookup"><span data-stu-id="afa58-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="afa58-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="afa58-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="afa58-140">queryControl</span><span class="sxs-lookup"><span data-stu-id="afa58-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="afa58-141">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="afa58-141">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="afa58-142">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="afa58-142">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
