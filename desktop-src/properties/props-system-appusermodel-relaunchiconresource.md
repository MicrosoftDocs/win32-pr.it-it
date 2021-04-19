---
description: Specifica l'icona utilizzata per il collegamento creato sulla barra delle applicazioni quando l'utente sceglie di aggiungere un'applicazione alla barra delle applicazioni o di avviare una nuova istanza tramite la Jump List del relativo pulsante.
ms.assetid: 3559d1f5-988c-41d9-ba9a-dfa4ba643ee2
title: System. AppUserModel. RelaunchIconResource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc79c246fef7be5641c6488dcc34169cd5bbf98b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310100"
---
# <a name="systemappusermodelrelaunchiconresource"></a><span data-ttu-id="e7a41-103">System. AppUserModel. RelaunchIconResource</span><span class="sxs-lookup"><span data-stu-id="e7a41-103">System.AppUserModel.RelaunchIconResource</span></span>

<span data-ttu-id="e7a41-104">Specifica l'icona utilizzata per il collegamento creato sulla barra delle applicazioni quando l'utente sceglie di aggiungere un'applicazione alla barra delle applicazioni o di avviare una nuova istanza tramite la Jump List del relativo pulsante.</span><span class="sxs-lookup"><span data-stu-id="e7a41-104">Specifies the icon used for the shortcut created on the taskbar when the user chooses to pin an application to the taskbar or launch a new instance through its button's Jump List.</span></span> <span data-ttu-id="e7a41-105">Si tratta dell'icona utilizzata per il gruppo della barra delle applicazioni e viene visualizzata per un'applicazione bloccata, indipendentemente dal fatto che l'applicazione sia in esecuzione o meno.</span><span class="sxs-lookup"><span data-stu-id="e7a41-105">This is the icon used for the taskbar group and is shown for a pinned application whether that application is running or not.</span></span> <span data-ttu-id="e7a41-106">Questa operazione deve essere specificata in uno dei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="e7a41-106">This should be specified in one of the following formats:</span></span>

-   <span data-ttu-id="e7a41-107">Formato di risorsa standard, ad esempio "% systemdir% \\ system32 \\shell32.dll,-128".</span><span class="sxs-lookup"><span data-stu-id="e7a41-107">Standard resource format, such as "%systemdir%\\system32\\shell32.dll,-128".</span></span> <span data-ttu-id="e7a41-108">Il carattere '-' prima dell'ID risorsa è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e7a41-108">The '-' character before the resource ID is required.</span></span> <span data-ttu-id="e7a41-109">Non usare il carattere ' @' all'inizio della stringa di percorso.</span><span class="sxs-lookup"><span data-stu-id="e7a41-109">Do not use the '@' character at the front of the path string.</span></span>
-   <span data-ttu-id="e7a41-110">Percorso diretto di un file di icona, ad esempio "% ProgramFiles% \\ Microsoft \\ notepad \\ notepad. ico,0".</span><span class="sxs-lookup"><span data-stu-id="e7a41-110">Direct path to an icon file, such as "%programfiles%\\Microsoft\\Notepad\\Notepad.ico,0".</span></span> <span data-ttu-id="e7a41-111">Si noti che poiché i file con estensione ICO possono contenere più risorse icona, nella stringa è necessario un ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="e7a41-111">Note that because .ico files can contain multiple icon resources, a resource ID is required in the string.</span></span> <span data-ttu-id="e7a41-112">Se il file con estensione ico è una singola immagine, usare "0" (senza il carattere '-') come ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="e7a41-112">If the .ico file is a single image, use "0" (without the '-' character) as the resource ID.</span></span>

<span data-ttu-id="e7a41-113">[System. AppUserModel. RelaunchIconResource]() è una proprietà facoltativa.</span><span class="sxs-lookup"><span data-stu-id="e7a41-113">[System.AppUserModel.RelaunchIconResource]() is an optional property.</span></span> <span data-ttu-id="e7a41-114">Se non è impostata, viene utilizzata l'icona della destinazione del comando di rilancio ([System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)).</span><span class="sxs-lookup"><span data-stu-id="e7a41-114">If it is not set, the icon of the target of the relaunch command ([System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)) is used.</span></span> <span data-ttu-id="e7a41-115">Tuttavia, poiché ciò può portare a risultati indesiderati, si consiglia vivamente di fornire un'icona in modo esplicito tramite questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="e7a41-115">However, because that can lead to undesired results, we strongly encourage you to provide an icon explicitly through this property.</span></span>

<span data-ttu-id="e7a41-116">Questa proprietà viene utilizzata solo se una finestra dispone di un ID modello utente applicazione esplicito (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), impostato tramite [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span><span class="sxs-lookup"><span data-stu-id="e7a41-116">This property is used only if a window has an explicit Application User Model ID (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), set through [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span></span> <span data-ttu-id="e7a41-117">Se la finestra non dispone di un AppUserModelID esplicito (System.AppUserModel.ID), questa proprietà viene ignorata e la finestra viene raggruppata e bloccata come se facesse parte del processo proprietario.</span><span class="sxs-lookup"><span data-stu-id="e7a41-117">If the window does not have an explicit AppUserModelID (System.AppUserModel.ID), this property is ignored and the window is grouped and pinned as if it were part of its owning process.</span></span> <span data-ttu-id="e7a41-118">Per ulteriori informazioni sull'applicazione di AppUserModelIDs espliciti e sul relativo effetto sul blocco della barra delle applicazioni, vedere [ID modello utente applicazione (AppUserModelIDs)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="e7a41-118">For more information on the application of explicit AppUserModelIDs and their effect on taskbar pinning, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span> <span data-ttu-id="e7a41-119">Questa proprietà deve essere usata da applicazioni o finestre che vogliono fornire informazioni di riavvio non predefinite.</span><span class="sxs-lookup"><span data-stu-id="e7a41-119">This property is meant to be used by applications or windows that want to provide non-default relaunch information.</span></span> <span data-ttu-id="e7a41-120">Per ulteriori informazioni, vedere [System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).</span><span class="sxs-lookup"><span data-stu-id="e7a41-120">For more information, see [System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).</span></span>

<span data-ttu-id="e7a41-121">Se nella finestra è impostato un AppUserModelID esplicito, ma questa proprietà non è impostata, il sistema tenta di trovare un collegamento con lo stesso AppUserModelID e il collegamento alla barra delle applicazioni per rappresentare la finestra.</span><span class="sxs-lookup"><span data-stu-id="e7a41-121">If an explicit AppUserModelID is set on the window, but this property is not set, the system attempts to find a shortcut with the same AppUserModelID, and pins that shortcut to the taskbar to represent the window.</span></span> <span data-ttu-id="e7a41-122">Se non è possibile trovare tale collegamento, viene usato l'eseguibile sottostante del processo a cui è proprietario.</span><span class="sxs-lookup"><span data-stu-id="e7a41-122">If no such shortcut can be located, then the backing executable of the process that owns it is used.</span></span>

> [!Note]  
> <span data-ttu-id="e7a41-123">Questa proprietà viene ignorata se si imposta [System. AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) .</span><span class="sxs-lookup"><span data-stu-id="e7a41-123">This property is ignored if [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) is set.</span></span> <span data-ttu-id="e7a41-124">Questo consente a un'applicazione di controllare il raggruppamento delle relative finestre assegnando loro AppUserModelIDs espliciti ma impedendo l'aggiunta di tali finestre.</span><span class="sxs-lookup"><span data-stu-id="e7a41-124">This enables an application to control the grouping of its windows by assigning them explicit AppUserModelIDs but preventing those windows from being pinned.</span></span>

 

<span data-ttu-id="e7a41-125">Per impostare questa proprietà in una finestra, usare [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) per recuperare l'archivio delle proprietà della finestra e usare i metodi dell'oggetto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) recuperato per impostare la proprietà [System. AppUserModel. RelaunchIconResource]() di tale finestra.</span><span class="sxs-lookup"><span data-stu-id="e7a41-125">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.RelaunchIconResource]() property of that window.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a><span data-ttu-id="e7a41-126">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e7a41-126">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = false
```

## <a name="windows-8-windows-7"></a><span data-ttu-id="e7a41-127">Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="e7a41-127">Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="related-topics"></a><span data-ttu-id="e7a41-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e7a41-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7a41-129">ID modello utente applicazione (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="e7a41-129">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="e7a41-130">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="e7a41-130">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="e7a41-131">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="e7a41-131">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="e7a41-132">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="e7a41-132">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="e7a41-133">searchInfo</span><span class="sxs-lookup"><span data-stu-id="e7a41-133">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="e7a41-134">labelInfo</span><span class="sxs-lookup"><span data-stu-id="e7a41-134">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="e7a41-135">typeInfo</span><span class="sxs-lookup"><span data-stu-id="e7a41-135">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="e7a41-136">displayInfo</span><span class="sxs-lookup"><span data-stu-id="e7a41-136">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="e7a41-137">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="e7a41-137">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="e7a41-138">stringFormat</span><span class="sxs-lookup"><span data-stu-id="e7a41-138">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="e7a41-139">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="e7a41-139">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="e7a41-140">numberFormat</span><span class="sxs-lookup"><span data-stu-id="e7a41-140">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="e7a41-141">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="e7a41-141">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="e7a41-142">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="e7a41-142">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="e7a41-143">enum</span><span class="sxs-lookup"><span data-stu-id="e7a41-143">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="e7a41-144">enumRange</span><span class="sxs-lookup"><span data-stu-id="e7a41-144">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="e7a41-145">image</span><span class="sxs-lookup"><span data-stu-id="e7a41-145">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="e7a41-146">drawControl</span><span class="sxs-lookup"><span data-stu-id="e7a41-146">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="e7a41-147">editControl</span><span class="sxs-lookup"><span data-stu-id="e7a41-147">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="e7a41-148">filterControl</span><span class="sxs-lookup"><span data-stu-id="e7a41-148">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="e7a41-149">queryControl</span><span class="sxs-lookup"><span data-stu-id="e7a41-149">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="e7a41-150">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="e7a41-150">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="e7a41-151">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="e7a41-151">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
