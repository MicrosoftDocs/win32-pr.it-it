---
description: La proprietà DVDAdm. DefaultMenuLCID imposta o recupera l'impostazione del registro di sistema per l'LCID predefinito specificato dall'utente per i menu.
ms.assetid: 49e64b89-5914-4797-8aa6-2e3f253e494a
title: Proprietà DefaultMenuLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907fbef0d04306b5ddc4f9a59749c96573d05bb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125175"
---
# <a name="defaultmenulcid-property"></a><span data-ttu-id="c163a-103">Proprietà DefaultMenuLCID</span><span class="sxs-lookup"><span data-stu-id="c163a-103">DefaultMenuLCID Property</span></span>

> [!Note]  
> <span data-ttu-id="c163a-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c163a-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="c163a-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="c163a-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="c163a-106">La `DVDAdm.DefaultMenuLCID` proprietà imposta o recupera l'impostazione del registro di sistema per l'LCID predefinito specificato dall'utente per i menu.</span><span class="sxs-lookup"><span data-stu-id="c163a-106">The `DVDAdm.DefaultMenuLCID` property sets or retrieves the registry setting for the user-specified default LCID for menus.</span></span>

``` syntax
[ iMenuLCID = ] DVD.DVDAdm.DefaultMenuLCID
```

## <a name="return-value"></a><span data-ttu-id="c163a-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c163a-107">Return Value</span></span>

<span data-ttu-id="c163a-108">Restituisce un valore intero che rappresenta l'LCID come archiviato nelle impostazioni del registro di sistema per l'applicazione DVD.</span><span class="sxs-lookup"><span data-stu-id="c163a-108">Returns an Integer value representing the LCID as stored in the registry settings for the DVD application.</span></span> <span data-ttu-id="c163a-109">Questo valore non è necessariamente uguale alla lingua di menu predefinita creata sul DVD.</span><span class="sxs-lookup"><span data-stu-id="c163a-109">This value is not necessarily the same as the default menu language as authored on the DVD.</span></span> <span data-ttu-id="c163a-110">Per l'intervallo degli LCID validi, vedere la documentazione di Win32 in Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="c163a-110">For the range of valid LCIDs, see the Win32 documentation in the Platform SDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c163a-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c163a-111">Remarks</span></span>

<span data-ttu-id="c163a-112">Questa proprietà è di lettura/scrittura e non prevede alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="c163a-112">This property is read/write with no default value.</span></span> <span data-ttu-id="c163a-113">Se non viene specificato alcun LCID di menu predefinito, l'oggetto MSDVDAdm utilizzerà la lingua contrassegnata come lingua di menu predefinita sul disco.</span><span class="sxs-lookup"><span data-stu-id="c163a-113">If no default menu LCID is specified, the MSDVDAdm object will use the language that is marked as the default menu language on the disc.</span></span>

## <a name="see-also"></a><span data-ttu-id="c163a-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c163a-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c163a-115">Oggetto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="c163a-115">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



