---
description: La proprietà DVDAdm. DisableScreenSaver attiva o disattiva la screen saver di sistema.
ms.assetid: 78a0512f-456a-45b6-8717-13593461a765
title: Proprietà DisableScreenSaver
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d651026f2bf09f872655a0ef58accb3a6173dcb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876034"
---
# <a name="disablescreensaver-property"></a><span data-ttu-id="b2963-103">Proprietà DisableScreenSaver</span><span class="sxs-lookup"><span data-stu-id="b2963-103">DisableScreenSaver Property</span></span>

> [!Note]  
> <span data-ttu-id="b2963-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b2963-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="b2963-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="b2963-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="b2963-106">La `DVDAdm.DisableScreenSaver` proprietà attiva o disattiva la screen saver di sistema.</span><span class="sxs-lookup"><span data-stu-id="b2963-106">The `DVDAdm.DisableScreenSaver` property turns the system screen saver on or off.</span></span>

``` syntax
[ bDisabled = ] DVD.DVDAdm.DisableScreenSaver
```

## <a name="return-value"></a><span data-ttu-id="b2963-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2963-107">Return Value</span></span>

<span data-ttu-id="b2963-108">Restituisce un valore booleano che indica se le impostazioni screen saver del sistema sono disabilitate per l'applicazione DVD Player; true indica che le impostazioni sono disabilitate.</span><span class="sxs-lookup"><span data-stu-id="b2963-108">Returns a Boolean value indicating whether the system's screen saver settings are disabled for the DVD player application; true means the settings are disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2963-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2963-109">Remarks</span></span>

<span data-ttu-id="b2963-110">Questa proprietà è di lettura/scrittura e il valore predefinito è true.</span><span class="sxs-lookup"><span data-stu-id="b2963-110">This property is read/write with a default value of true.</span></span> <span data-ttu-id="b2963-111">Quando si visualizza un disco DVD-Video, un utente in genere non utilizza il mouse o la tastiera per periodi di tempo prolungati.</span><span class="sxs-lookup"><span data-stu-id="b2963-111">When viewing a DVD-Video disc, a user typically does not use the mouse or keyboard for extended periods of time.</span></span> <span data-ttu-id="b2963-112">Il controllo® ActiveX MSWebDVD Disabilita quindi il screen saver di sistema per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b2963-112">The MSWebDVD ActiveX® control therefore disables the system screen saver by default.</span></span> <span data-ttu-id="b2963-113">Oggetto</span><span class="sxs-lookup"><span data-stu-id="b2963-113">Object</span></span>

## <a name="see-also"></a><span data-ttu-id="b2963-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2963-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2963-115">**RestoreScreenSaver**</span><span class="sxs-lookup"><span data-stu-id="b2963-115">**RestoreScreenSaver**</span></span>](restorescreensaver-method.md)
</dt> <dt>

[<span data-ttu-id="b2963-116">Oggetto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="b2963-116">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



