---
description: Impostare questa proprietà su un collegamento a (1) impedire che un'applicazione venga bloccata automaticamente alla schermata Start durante l'installazione; o (2) indica che un elemento viene aggiunto a livello di codice all'utilità di avvio tramite un'azione dell'utente (che implica automaticamente il pin per l'avvio e l'eliminazione in Rimuovi).
ms.assetid: 247ad0a6-ce65-45f1-a0d5-51ad135000aa
title: System. AppUserModel. StartPinOption
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43cdef82a90488ce87bbf182323b00d62a5cdfea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880546"
---
# <a name="systemappusermodelstartpinoption"></a><span data-ttu-id="39862-103">System. AppUserModel. StartPinOption</span><span class="sxs-lookup"><span data-stu-id="39862-103">System.AppUserModel.StartPinOption</span></span>

<span data-ttu-id="39862-104">Impostare questa proprietà su un collegamento a (1) impedire che un'applicazione venga bloccata automaticamente alla schermata Start durante l'installazione; o (2) indica che un elemento viene aggiunto a livello di codice all'utilità di avvio tramite un'azione dell'utente (che implica automaticamente il pin per l'avvio e l'eliminazione in Rimuovi).</span><span class="sxs-lookup"><span data-stu-id="39862-104">Set this property on a shortcut to (1) prevent an application from being automatically pinned to Start screen upon installation; or(2) indicate that an item is programmatically added to launcher via user action (which implies automatically pin to Start and delete on unpin).</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="39862-105">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="39862-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.AppUserModel.StartPinOption
   shellPKey = PKEY_AppUserModel_StartPinOption
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 12
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = false
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Default
            value = 0
            text = Default
            defineToken = APPUSERMODEL_STARTPINOPTION_DEFAULT
         enum
            name = NoPinOnInstall
            value = 1
            text = NoPinOnInstall
            defineToken = APPUSERMODEL_STARTPINOPTION_NOPINONINSTALL
         enum
            name = UserPinned
            value = 2
            text = UserPinned
            defineToken = APPUSERMODEL_STARTPINOPTION_USERPINNED
```

## <a name="remarks"></a><span data-ttu-id="39862-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="39862-106">Remarks</span></span>

<span data-ttu-id="39862-107">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="39862-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39862-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="39862-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39862-109">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="39862-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="39862-110">searchInfo</span><span class="sxs-lookup"><span data-stu-id="39862-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="39862-111">labelInfo</span><span class="sxs-lookup"><span data-stu-id="39862-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="39862-112">typeInfo</span><span class="sxs-lookup"><span data-stu-id="39862-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="39862-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="39862-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="39862-114">stringFormat</span><span class="sxs-lookup"><span data-stu-id="39862-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="39862-115">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="39862-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="39862-116">numberFormat</span><span class="sxs-lookup"><span data-stu-id="39862-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="39862-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="39862-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="39862-118">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="39862-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="39862-119">drawControl</span><span class="sxs-lookup"><span data-stu-id="39862-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="39862-120">editControl</span><span class="sxs-lookup"><span data-stu-id="39862-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="39862-121">filterControl</span><span class="sxs-lookup"><span data-stu-id="39862-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="39862-122">queryControl</span><span class="sxs-lookup"><span data-stu-id="39862-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
