---
description: Il metodo DVDAdm. RestoreScreenSaver Ripristina le impostazioni di screen saver di sistema.
ms.assetid: 606ab850-95bf-4c60-b7cf-e3a94ceee7a7
title: Metodo RestoreScreenSaver
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b747aa21815bb37cc7db2296347c9890a06914
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303911"
---
# <a name="restorescreensaver-method"></a><span data-ttu-id="c97b8-103">Metodo RestoreScreenSaver</span><span class="sxs-lookup"><span data-stu-id="c97b8-103">RestoreScreenSaver Method</span></span>

> [!Note]  
> <span data-ttu-id="c97b8-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c97b8-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="c97b8-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="c97b8-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="c97b8-106">Il `DVDAdm.RestoreScreenSaver` metodo ripristina le impostazioni del screen saver di sistema.</span><span class="sxs-lookup"><span data-stu-id="c97b8-106">The `DVDAdm.RestoreScreenSaver` method restores the system screen saver settings.</span></span>

``` syntax
DVD.DVDAdm.RestoreScreenSaver()
```

## <a name="return-value"></a><span data-ttu-id="c97b8-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c97b8-107">Return Value</span></span>

<span data-ttu-id="c97b8-108">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="c97b8-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c97b8-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="c97b8-109">Remarks</span></span>

<span data-ttu-id="c97b8-110">In genere, un'applicazione DVD Disabilita la screen saver di sistema all'avvio impostando la proprietà [**DisableScreenSaver**](disablescreensaver-property.md) su true e riabilitando nuovamente l'screen saver quando l'applicazione DVD viene chiusa chiamando `RestoreScreenSaver` .</span><span class="sxs-lookup"><span data-stu-id="c97b8-110">Generally, a DVD application will disable the system's screen saver on startup by setting the [**DisableScreenSaver**](disablescreensaver-property.md) property to true, and then re-enable the screen saver again when the DVD application is closed by calling `RestoreScreenSaver`.</span></span> <span data-ttu-id="c97b8-111">Se un'applicazione non utilizza le impostazioni screen saver del sistema, non è necessario chiamare questo metodo o impostare la proprietà **DisableScreenSaver** .</span><span class="sxs-lookup"><span data-stu-id="c97b8-111">If an application does not use the system's screen saver settings, it does not have to call this method or set the **DisableScreenSaver** property.</span></span>

## <a name="see-also"></a><span data-ttu-id="c97b8-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c97b8-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c97b8-113">Oggetto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="c97b8-113">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



