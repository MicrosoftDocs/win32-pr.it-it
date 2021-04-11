---
description: Specifica il nome visualizzato utilizzato per il collegamento creato sulla barra delle applicazioni quando l'utente sceglie di aggiungere un'applicazione alla barra delle applicazioni o di avviare una nuova istanza tramite la Jump List del relativo pulsante.
ms.assetid: a149838b-83b6-44ce-b705-e2804efb3d31
title: System. AppUserModel. RelaunchDisplayNameResource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79c22d0ccecb8bac86fe5ca3636ed10ed2ca50b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231602"
---
# <a name="systemappusermodelrelaunchdisplaynameresource"></a><span data-ttu-id="0c8d7-103">System. AppUserModel. RelaunchDisplayNameResource</span><span class="sxs-lookup"><span data-stu-id="0c8d7-103">System.AppUserModel.RelaunchDisplayNameResource</span></span>

<span data-ttu-id="0c8d7-104">Specifica il nome visualizzato utilizzato per il collegamento creato sulla barra delle applicazioni quando l'utente sceglie di aggiungere un'applicazione alla barra delle applicazioni o di avviare una nuova istanza tramite la Jump List del relativo pulsante.</span><span class="sxs-lookup"><span data-stu-id="0c8d7-104">Specifies the display name used for the shortcut created on the taskbar when the user chooses to pin an application to the taskbar or launch a new instance through its button's Jump List.</span></span> <span data-ttu-id="0c8d7-105">Il valore di questa proprietà deve essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c8d7-105">The value of this property must be one of the following:</span></span>

-   <span data-ttu-id="0c8d7-106">Stringa di risorsa indiretta, ad esempio "@% systemdir% \\ system32 \\shell32.dll,-19263".</span><span class="sxs-lookup"><span data-stu-id="0c8d7-106">An indirect resource string such as "@%systemdir%\\system32\\shell32.dll,-19263".</span></span> <span data-ttu-id="0c8d7-107">Si noti che il carattere ' @' è necessario per distinguere una stringa indiretta da una stringa di testo normale, descritta nel paragrafo successivo.</span><span class="sxs-lookup"><span data-stu-id="0c8d7-107">Note that the '@' character is required to distinguish an indirect string from a plain-text string (described in the next bulleted paragraph).</span></span> <span data-ttu-id="0c8d7-108">Questa stringa indiretta è costituita da un file binario e da un ID di risorsa della stringa contenuta nel file binario.</span><span class="sxs-lookup"><span data-stu-id="0c8d7-108">This indirect string consists of a binary file and a resource ID of the string contained in that binary.</span></span> <span data-ttu-id="0c8d7-109">Si consiglia vivamente di utilizzare questo formato stringa indiretto, che garantisce che il nome visualizzato venga modificato in modo appropriato quando la lingua di sistema viene modificata tramite l'interfaccia utente multilingue (MUI).</span><span class="sxs-lookup"><span data-stu-id="0c8d7-109">We strongly recommend that you use this indirect string form, which ensures that the display name changes appropriately when the system language is changed through the Multilingual User Interface (MUI).</span></span> <span data-ttu-id="0c8d7-110">Il carattere '-' prima dell'ID risorsa è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0c8d7-110">The '-' character before the resource ID is required.</span></span>
-   <span data-ttu-id="0c8d7-111">Una stringa di testo normale che non punta a una risorsa.</span><span class="sxs-lookup"><span data-stu-id="0c8d7-111">A plain-text string that does not point to a resource.</span></span> <span data-ttu-id="0c8d7-112">Questa operazione deve essere usata solo quando il nome visualizzato viene calcolato in modo dinamico o ottenuto da un'origine dati che non supporta MUI.</span><span class="sxs-lookup"><span data-stu-id="0c8d7-112">This should only be used when the display name is dynamically calculated or obtained from a data source that does not support MUI.</span></span> <span data-ttu-id="0c8d7-113">Ad esempio, la stringa può essere il nome di un dispositivo, ad esempio "Microsoft Zune", nei casi in cui l'applicazione viene visualizzata quando il dispositivo è collegato al computer.</span><span class="sxs-lookup"><span data-stu-id="0c8d7-113">For example, the string could be the name of a device, such as "Microsoft Zune", in cases where the application appears when that device is attached to the computer.</span></span>

> [!Note]  
> <span data-ttu-id="0c8d7-114">[System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md) e [System. AppUserModel. RelaunchDisplayNameResource]() devono essere impostati sempre insieme.</span><span class="sxs-lookup"><span data-stu-id="0c8d7-114">[System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md) and [System.AppUserModel.RelaunchDisplayNameResource]() must always be set together.</span></span> <span data-ttu-id="0c8d7-115">Se una di queste proprietà non è impostata, non viene usato nessuno dei due.</span><span class="sxs-lookup"><span data-stu-id="0c8d7-115">If one of those properties is not set, then neither is used.</span></span>

 

<span data-ttu-id="0c8d7-116">Questa proprietà viene utilizzata solo se una finestra dispone di un ID modello utente applicazione esplicito (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), impostato tramite [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span><span class="sxs-lookup"><span data-stu-id="0c8d7-116">This property is used only if a window has an explicit Application User Model ID (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), set through [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span></span> <span data-ttu-id="0c8d7-117">Se la finestra non contiene un AppUserModelID esplicito, questa proprietà viene ignorata e la finestra viene raggruppata e bloccata come se facesse parte del processo a cui appartiene.</span><span class="sxs-lookup"><span data-stu-id="0c8d7-117">If the window does not have an explicit AppUserModelID, this property is ignored and the window is grouped and pinned as if it were part of the process that owns it.</span></span> <span data-ttu-id="0c8d7-118">Per ulteriori informazioni sull'applicazione di AppUserModelIDs espliciti e sul relativo effetto sul blocco della barra delle applicazioni, vedere [ID modello utente applicazione (AppUserModelIDs)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="0c8d7-118">For more information on the application of explicit AppUserModelIDs and their effect on taskbar pinning, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span> <span data-ttu-id="0c8d7-119">Questa proprietà deve essere usata da applicazioni o finestre che vogliono fornire informazioni di riavvio non predefinite.</span><span class="sxs-lookup"><span data-stu-id="0c8d7-119">This property is meant to be used by applications or windows that want to provide non-default relaunch information.</span></span> <span data-ttu-id="0c8d7-120">Per ulteriori informazioni, vedere [System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).</span><span class="sxs-lookup"><span data-stu-id="0c8d7-120">For more information, see [System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).</span></span>

> [!Note]  
> <span data-ttu-id="0c8d7-121">Questa proprietà viene ignorata se si imposta [System. AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) .</span><span class="sxs-lookup"><span data-stu-id="0c8d7-121">This property is ignored if [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) is set.</span></span> <span data-ttu-id="0c8d7-122">Questo consente a un'applicazione di controllare il raggruppamento delle relative finestre assegnando loro AppUserModelIDs espliciti ma impedendo l'aggiunta di tali finestre.</span><span class="sxs-lookup"><span data-stu-id="0c8d7-122">This enables an application to control the grouping of its windows by assigning them explicit AppUserModelIDs but preventing those windows from being pinned.</span></span>

 

<span data-ttu-id="0c8d7-123">Per impostare questa proprietà in una finestra, usare [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) per recuperare l'archivio delle proprietà della finestra e usare i metodi dell'oggetto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) recuperato per impostare la proprietà [System. AppUserModel. RelaunchDisplayNameResource]() di tale finestra.</span><span class="sxs-lookup"><span data-stu-id="0c8d7-123">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.RelaunchDisplayNameResource]() property of that window.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="0c8d7-124">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="0c8d7-124">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchDisplayNameResource
   shellPKey = PKEY_AppUserModel_RelaunchDisplayNameResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 4
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="0c8d7-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c8d7-125">Remarks</span></span>

<span data-ttu-id="0c8d7-126">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="0c8d7-126">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c8d7-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0c8d7-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c8d7-128">ID modello utente applicazione (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="0c8d7-128">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="0c8d7-129">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="0c8d7-129">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="0c8d7-130">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="0c8d7-130">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="0c8d7-131">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="0c8d7-131">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="0c8d7-132">searchInfo</span><span class="sxs-lookup"><span data-stu-id="0c8d7-132">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="0c8d7-133">labelInfo</span><span class="sxs-lookup"><span data-stu-id="0c8d7-133">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="0c8d7-134">typeInfo</span><span class="sxs-lookup"><span data-stu-id="0c8d7-134">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="0c8d7-135">displayInfo</span><span class="sxs-lookup"><span data-stu-id="0c8d7-135">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="0c8d7-136">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="0c8d7-136">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="0c8d7-137">stringFormat</span><span class="sxs-lookup"><span data-stu-id="0c8d7-137">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="0c8d7-138">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="0c8d7-138">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="0c8d7-139">numberFormat</span><span class="sxs-lookup"><span data-stu-id="0c8d7-139">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="0c8d7-140">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="0c8d7-140">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="0c8d7-141">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="0c8d7-141">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="0c8d7-142">enum</span><span class="sxs-lookup"><span data-stu-id="0c8d7-142">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="0c8d7-143">enumRange</span><span class="sxs-lookup"><span data-stu-id="0c8d7-143">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="0c8d7-144">image</span><span class="sxs-lookup"><span data-stu-id="0c8d7-144">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="0c8d7-145">drawControl</span><span class="sxs-lookup"><span data-stu-id="0c8d7-145">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="0c8d7-146">editControl</span><span class="sxs-lookup"><span data-stu-id="0c8d7-146">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="0c8d7-147">filterControl</span><span class="sxs-lookup"><span data-stu-id="0c8d7-147">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="0c8d7-148">queryControl</span><span class="sxs-lookup"><span data-stu-id="0c8d7-148">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="0c8d7-149">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="0c8d7-149">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="0c8d7-150">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="0c8d7-150">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
