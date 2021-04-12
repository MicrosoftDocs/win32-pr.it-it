---
description: ID del modello utente dell'applicazione (AppUserModelID) esplicito utilizzato per associare processi, file e finestre a una particolare applicazione.
ms.assetid: 07858b3c-e601-40ec-a87a-d66612d5473a
title: System.AppUserModel.ID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c636b2c946f1138f4a25c3129a7a3b44d31558
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344781"
---
# <a name="systemappusermodelid"></a><span data-ttu-id="eaed3-103">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="eaed3-103">System.AppUserModel.ID</span></span>

<span data-ttu-id="eaed3-104">ID del modello utente dell'applicazione (AppUserModelID) esplicito utilizzato per associare processi, file e finestre a una particolare applicazione.</span><span class="sxs-lookup"><span data-stu-id="eaed3-104">An explicit Application User Model ID (AppUserModelID) used to associate processes, files, and windows with a particular application.</span></span> <span data-ttu-id="eaed3-105">In alcuni casi, è sufficiente basarsi sul AppUserModelID interno assegnato a un processo dal sistema.</span><span class="sxs-lookup"><span data-stu-id="eaed3-105">In some cases, it is sufficient to rely on the internal AppUserModelID assigned to a process by the system.</span></span> <span data-ttu-id="eaed3-106">Tuttavia, un'applicazione che possiede più processi o un'applicazione in esecuzione in un processo host potrebbe dover identificarsi in modo esplicito tramite questa proprietà, in modo che possa raggruppare le finestre altrimenti diverse in un unico pulsante della barra delle applicazioni e controllare il contenuto della Jump List dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="eaed3-106">However, an application that owns multiple processes or an application that is running in a host process might need to explicitly identify itself through this property so that it can group its otherwise disparate windows under a single taskbar button and control the contents of that application's Jump List.</span></span>

<span data-ttu-id="eaed3-107">Per impostare questa proprietà in una finestra, usare [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) per recuperare l'archivio delle proprietà della finestra e usare i metodi dell'oggetto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) recuperato per impostare la proprietà [System.AppUserModel.ID]() di tale finestra.</span><span class="sxs-lookup"><span data-stu-id="eaed3-107">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.ID]() property of that window.</span></span>

<span data-ttu-id="eaed3-108">Per ulteriori informazioni, vedere [ID modello utente applicazione (AppUserModelIDs)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="eaed3-108">For more information, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span>

<span data-ttu-id="eaed3-109">Al momento dell'impostazione della proprietà [System.AppUserModel.ID]() , alla barra delle applicazioni viene inviata una notifica per aggiornare le informazioni nella finestra o nel collegamento, dato che AppUserModelID.</span><span class="sxs-lookup"><span data-stu-id="eaed3-109">At the time the [System.AppUserModel.ID]() property is set, the taskbar is notified to refresh its information on the window or shortcut given that AppUserModelID.</span></span>

<span data-ttu-id="eaed3-110">Altre proprietà finestra e collegamento possono essere usate insieme a un AppUserModelID esplicito per controllare ulteriormente il raggruppamento e il blocco associato a una finestra, il nome visualizzato e l'icona usati nella barra delle applicazioni e il comando per avviare un'applicazione aggiunta alla barra delle applicazioni o una nuova istanza dell'applicazione tramite la Jump List dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="eaed3-110">Other window and shortcut properties can be used in conjunction with an explicit AppUserModelID to further control the grouping and pinning associated with a window, the display name and icon used for it in the taskbar, and the command to launch either an application pinned to the taskbar or a new instance of the application through that application's Jump List.</span></span> <span data-ttu-id="eaed3-111">Queste proprietà devono essere impostate prima di impostare la proprietà [System.AppUserModel.ID]() .</span><span class="sxs-lookup"><span data-stu-id="eaed3-111">These properties should be set before setting the [System.AppUserModel.ID]() property.</span></span> <span data-ttu-id="eaed3-112">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="eaed3-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="eaed3-113">System. AppUserModel. PreventPinning</span><span class="sxs-lookup"><span data-stu-id="eaed3-113">System.AppUserModel.PreventPinning</span></span>](./props-system-appusermodel-preventpinning.md)
-   [<span data-ttu-id="eaed3-114">System. AppUserModel. RelaunchCommand</span><span class="sxs-lookup"><span data-stu-id="eaed3-114">System.AppUserModel.RelaunchCommand</span></span>](./props-system-appusermodel-relaunchcommand.md)
-   [<span data-ttu-id="eaed3-115">System. AppUserModel. RelaunchDisplayNameResource</span><span class="sxs-lookup"><span data-stu-id="eaed3-115">System.AppUserModel.RelaunchDisplayNameResource</span></span>](./props-system-appusermodel-relaunchdisplaynameresource.md)
-   [<span data-ttu-id="eaed3-116">System. AppUserModel. RelaunchIconResource</span><span class="sxs-lookup"><span data-stu-id="eaed3-116">System.AppUserModel.RelaunchIconResource</span></span>](./props-system-appusermodel-relaunchiconresource.md)

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="eaed3-117">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="eaed3-117">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.ID
   shellPKey = PKEY_AppUserModel_ID
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 5
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="eaed3-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="eaed3-118">Remarks</span></span>

<span data-ttu-id="eaed3-119">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="eaed3-119">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eaed3-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eaed3-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eaed3-121">ID modello utente applicazione (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="eaed3-121">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="eaed3-122">**SHGetPropertyStoreForWindow**</span><span class="sxs-lookup"><span data-stu-id="eaed3-122">**SHGetPropertyStoreForWindow**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> <dt>

[<span data-ttu-id="eaed3-123">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="eaed3-123">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="eaed3-124">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="eaed3-124">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="eaed3-125">searchInfo</span><span class="sxs-lookup"><span data-stu-id="eaed3-125">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="eaed3-126">labelInfo</span><span class="sxs-lookup"><span data-stu-id="eaed3-126">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="eaed3-127">typeInfo</span><span class="sxs-lookup"><span data-stu-id="eaed3-127">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="eaed3-128">displayInfo</span><span class="sxs-lookup"><span data-stu-id="eaed3-128">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="eaed3-129">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="eaed3-129">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="eaed3-130">stringFormat</span><span class="sxs-lookup"><span data-stu-id="eaed3-130">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="eaed3-131">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="eaed3-131">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="eaed3-132">numberFormat</span><span class="sxs-lookup"><span data-stu-id="eaed3-132">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="eaed3-133">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="eaed3-133">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="eaed3-134">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="eaed3-134">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="eaed3-135">enum</span><span class="sxs-lookup"><span data-stu-id="eaed3-135">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="eaed3-136">enumRange</span><span class="sxs-lookup"><span data-stu-id="eaed3-136">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="eaed3-137">image</span><span class="sxs-lookup"><span data-stu-id="eaed3-137">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="eaed3-138">drawControl</span><span class="sxs-lookup"><span data-stu-id="eaed3-138">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="eaed3-139">editControl</span><span class="sxs-lookup"><span data-stu-id="eaed3-139">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="eaed3-140">filterControl</span><span class="sxs-lookup"><span data-stu-id="eaed3-140">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="eaed3-141">queryControl</span><span class="sxs-lookup"><span data-stu-id="eaed3-141">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="eaed3-142">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="eaed3-142">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="eaed3-143">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="eaed3-143">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
