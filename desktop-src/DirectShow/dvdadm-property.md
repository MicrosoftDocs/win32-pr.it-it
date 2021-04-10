---
description: La proprietà DVDAdm fornisce l'accesso all'oggetto MSDVDAdm che contiene i metodi e le proprietà per il salvataggio delle informazioni sull'applicazione e sull'utente.
ms.assetid: eb73a851-7118-42f3-be99-1cf356d2e37a
title: Proprietà DVDAdm
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c3d81742fc6e643d6ee805a76c14d07d45d1924
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124584"
---
# <a name="dvdadm-property"></a><span data-ttu-id="d84c3-103">Proprietà DVDAdm</span><span class="sxs-lookup"><span data-stu-id="d84c3-103">DVDAdm Property</span></span>

> [!Note]  
> <span data-ttu-id="d84c3-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d84c3-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="d84c3-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="d84c3-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="d84c3-106">La `DVDAdm` proprietà fornisce l'accesso all'oggetto [MSDVDAdm](msdvdadm-object.md) che contiene i metodi e le proprietà per il salvataggio delle informazioni sull'applicazione e sull'utente.</span><span class="sxs-lookup"><span data-stu-id="d84c3-106">The `DVDAdm` property provides access to the [MSDVDAdm](msdvdadm-object.md) object that contains methods and properties for saving application and user information.</span></span>

``` syntax
        MSWebDVD.DVDAdm
```

## <a name="remarks"></a><span data-ttu-id="d84c3-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="d84c3-107">Remarks</span></span>

<span data-ttu-id="d84c3-108">Questa proprietà è di sola lettura e non prevede alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="d84c3-108">This property is read-only with no default value.</span></span> <span data-ttu-id="d84c3-109">Non è necessario creare un riferimento separato all'oggetto **MSDVDAdm** .</span><span class="sxs-lookup"><span data-stu-id="d84c3-109">There is no need to create a separate reference to the **MSDVDAdm** object.</span></span> <span data-ttu-id="d84c3-110">Per accedere ai metodi e alle proprietà dell'oggetto, usare la `DVDAdm` proprietà come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="d84c3-110">To access the methods and properties of the object, use the `DVDAdm` property as shown in the following example.</span></span>

## <a name="examples"></a><span data-ttu-id="d84c3-111">Esempi</span><span class="sxs-lookup"><span data-stu-id="d84c3-111">Examples</span></span>


```VB
DVD.DVDAdm.DisableScreenSaver = true
```



 

 



