---
description: Specifica un comando che può essere eseguito tramite ShellExecute per avviare un'applicazione quando viene bloccata sulla barra delle applicazioni o quando viene avviata una nuova istanza dell'applicazione tramite la Jump List dell'applicazione.
ms.assetid: 83aab060-0629-48e3-a2db-9ba96a8631e5
title: System. AppUserModel. RelaunchCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84049f605896ba5e99a98f33557e6ee4dea37df5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310101"
---
# <a name="systemappusermodelrelaunchcommand"></a><span data-ttu-id="db20e-103">System. AppUserModel. RelaunchCommand</span><span class="sxs-lookup"><span data-stu-id="db20e-103">System.AppUserModel.RelaunchCommand</span></span>

<span data-ttu-id="db20e-104">Specifica un comando che può essere eseguito tramite [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) per avviare un'applicazione quando viene bloccata sulla barra delle applicazioni o quando viene avviata una nuova istanza dell'applicazione tramite la Jump List dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="db20e-104">Specifies a command that can be executed through [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) to launch an application when it is pinned to the taskbar or when a new instance of the application is launched through the application's Jump List.</span></span>

<span data-ttu-id="db20e-105">Negli esempi vengono illustrati gli aspetti seguenti:</span><span class="sxs-lookup"><span data-stu-id="db20e-105">Examples include the following:</span></span>


```
shell:::{ED228FDF-9EA8-4870-83B1-96B02CFE0D52}

virtualhost.exe /virtualapp:12345

notepad.exe
```



<span data-ttu-id="db20e-106">Questa proprietà viene utilizzata solo se una finestra dispone di un ID modello utente applicazione esplicito (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), impostato tramite [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span><span class="sxs-lookup"><span data-stu-id="db20e-106">This property is used only if a window has an explicit Application User Model ID (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), set through [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span></span> <span data-ttu-id="db20e-107">Se la finestra non contiene un AppUserModelID esplicito, questa proprietà viene ignorata e la finestra viene raggruppata e bloccata come se facesse parte del processo a cui appartiene.</span><span class="sxs-lookup"><span data-stu-id="db20e-107">If the window does not have an explicit AppUserModelID, this property is ignored and the window is grouped and pinned as if it were part of the process that owns it.</span></span> <span data-ttu-id="db20e-108">Per ulteriori informazioni sull'applicazione di AppUserModelIDs espliciti e sul relativo effetto sul blocco della barra delle applicazioni, vedere [ID modello utente applicazione (AppUserModelIDs)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="db20e-108">For more information about the application of explicit AppUserModelIDs and their effect on taskbar pinning, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span>

<span data-ttu-id="db20e-109">Questa proprietà deve essere usata da applicazioni o finestre che vogliono fornire informazioni di riavvio non predefinite.</span><span class="sxs-lookup"><span data-stu-id="db20e-109">This property is meant to be used by applications or windows that want to provide non-default relaunch information.</span></span>

> [!Note]  
> <span data-ttu-id="db20e-110">[System. AppUserModel. RelaunchCommand]() e [System. AppUserModel. RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) devono essere impostati sempre insieme.</span><span class="sxs-lookup"><span data-stu-id="db20e-110">[System.AppUserModel.RelaunchCommand]() and [System.AppUserModel.RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) must always be set together.</span></span> <span data-ttu-id="db20e-111">Se una di queste proprietà non è impostata, non viene usato nessuno dei due.</span><span class="sxs-lookup"><span data-stu-id="db20e-111">If one of those properties is not set, then neither is used.</span></span>

 

<span data-ttu-id="db20e-112">Questa proprietà, insieme a [System. AppUserModel. RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) e [System. AppUserModel. RelaunchIconResource](./props-system-appusermodel-relaunchiconresource.md) , può essere usata per definire visivamente una finestra come applicazione per l'utente.</span><span class="sxs-lookup"><span data-stu-id="db20e-112">This property, together with [System.AppUserModel.RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) and [System.AppUserModel.RelaunchIconResource](./props-system-appusermodel-relaunchiconresource.md) can be used to visually define a window as an application to the user.</span></span> <span data-ttu-id="db20e-113">Questa operazione è utile per gli scenari di applicazioni host, in cui una singola istanza dell'host esegue più applicazioni figlio.</span><span class="sxs-lookup"><span data-stu-id="db20e-113">This is useful for host application scenarios, where a single host instance runs multiple child applications.</span></span> <span data-ttu-id="db20e-114">Ad esempio, una macchina virtuale che ospita diverse applicazioni virtualizzate potrebbe voler visualizzare le applicazioni virtualizzate come singole applicazioni per l'utente.</span><span class="sxs-lookup"><span data-stu-id="db20e-114">For example, a virtual machine that hosts several virtualized applications might want those virtualized applications to appear as individual applications to the user.</span></span> <span data-ttu-id="db20e-115">La macchina virtuale potrebbe etichettare ogni finestra con un AppUserModelID esplicito e le proprietà di rilancio appropriate per renderle visualizzate come applicazioni.</span><span class="sxs-lookup"><span data-stu-id="db20e-115">The virtual machine could label each window with an explicit AppUserModelID and the appropriate relaunch properties to make them appear as applications.</span></span> <span data-ttu-id="db20e-116">L'utente può quindi aggiungerli alla barra delle applicazioni e "riavviare" l'istanza bloccata.</span><span class="sxs-lookup"><span data-stu-id="db20e-116">The user could then pin them to the taskbar and "relaunch" the pinned instance.</span></span>

> [!Note]  
> <span data-ttu-id="db20e-117">Questa proprietà viene ignorata se si imposta [System. AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) .</span><span class="sxs-lookup"><span data-stu-id="db20e-117">This property is ignored if [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) is set.</span></span> <span data-ttu-id="db20e-118">Questo consente a un'applicazione di controllare il raggruppamento delle relative finestre assegnando loro AppUserModelIDs espliciti ma impedendo l'aggiunta di tali finestre.</span><span class="sxs-lookup"><span data-stu-id="db20e-118">This enables an application to control the grouping of its windows by assigning them explicit AppUserModelIDs but preventing those windows from being pinned.</span></span>

 

<span data-ttu-id="db20e-119">Per impostare questa proprietà in una finestra, usare [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) per recuperare l'archivio delle proprietà della finestra e usare i metodi dell'oggetto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) recuperato per impostare la proprietà [System. AppUserModel. RelaunchCommand]() di tale finestra.</span><span class="sxs-lookup"><span data-stu-id="db20e-119">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.RelaunchCommand]() property of that window.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="db20e-120">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="db20e-120">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchCommand
   shellPKey = PKEY_AppUserModel_RelaunchCommand
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="db20e-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="db20e-121">Remarks</span></span>

<span data-ttu-id="db20e-122">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="db20e-122">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db20e-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="db20e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db20e-124">ID modello utente applicazione (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="db20e-124">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="db20e-125">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="db20e-125">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="db20e-126">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="db20e-126">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="db20e-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="db20e-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="db20e-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="db20e-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="db20e-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="db20e-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="db20e-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="db20e-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="db20e-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="db20e-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="db20e-132">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="db20e-132">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="db20e-133">stringFormat</span><span class="sxs-lookup"><span data-stu-id="db20e-133">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="db20e-134">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="db20e-134">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="db20e-135">numberFormat</span><span class="sxs-lookup"><span data-stu-id="db20e-135">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="db20e-136">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="db20e-136">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="db20e-137">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="db20e-137">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="db20e-138">enum</span><span class="sxs-lookup"><span data-stu-id="db20e-138">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="db20e-139">enumRange</span><span class="sxs-lookup"><span data-stu-id="db20e-139">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="db20e-140">image</span><span class="sxs-lookup"><span data-stu-id="db20e-140">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="db20e-141">drawControl</span><span class="sxs-lookup"><span data-stu-id="db20e-141">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="db20e-142">editControl</span><span class="sxs-lookup"><span data-stu-id="db20e-142">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="db20e-143">filterControl</span><span class="sxs-lookup"><span data-stu-id="db20e-143">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="db20e-144">queryControl</span><span class="sxs-lookup"><span data-stu-id="db20e-144">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="db20e-145">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="db20e-145">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="db20e-146">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="db20e-146">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
