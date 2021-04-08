---
description: Il metodo TakePicture dell'oggetto Item fa in modo che un dispositivo della fotocamera digitale prenda un'immagine e restituisce un oggetto Item che rappresenta l'immagine risultante. Questo metodo si applica solo ai dispositivi della fotocamera digitale.
ms.assetid: d181048e-21ef-4fcc-a50a-5ba44bbde72e
title: Metodo Item. TakePicture (wiavideo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.TakePicture
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: fd07f7ccd4f2c65c2d911dabdd0ca829dc241765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967571"
---
# <a name="itemtakepicture-method"></a><span data-ttu-id="6f738-104">Item. TakePicture, metodo</span><span class="sxs-lookup"><span data-stu-id="6f738-104">Item.TakePicture method</span></span>

<span data-ttu-id="6f738-105">Il metodo **TakePicture** dell'oggetto [**Item**](-wia-item.md) fa in modo che un dispositivo della fotocamera digitale prenda un'immagine e restituisce un oggetto **Item** che rappresenta l'immagine risultante.</span><span class="sxs-lookup"><span data-stu-id="6f738-105">The **TakePicture** method of the [**Item**](-wia-item.md) object causes a digital camera device to take a picture and returns an **Item** object that represents the resulting image.</span></span> <span data-ttu-id="6f738-106">Questo metodo si applica solo ai dispositivi della fotocamera digitale.</span><span class="sxs-lookup"><span data-stu-id="6f738-106">This method applies only to digital camera devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f738-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f738-107">Syntax</span></span>


```JScript
retVal = Item.TakePicture()
```



## <a name="parameters"></a><span data-ttu-id="6f738-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6f738-108">Parameters</span></span>

<span data-ttu-id="6f738-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="6f738-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6f738-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6f738-110">Return value</span></span>

<span data-ttu-id="6f738-111">Tipo: **IWiaDispatchItem**</span><span class="sxs-lookup"><span data-stu-id="6f738-111">Type: **IWiaDispatchItem**</span></span>

<span data-ttu-id="6f738-112">Oggetto [**Item**](-wia-item.md) che rappresenta l'immagine creata da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="6f738-112">An [**Item**](-wia-item.md) object that represents the image that this method creates.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f738-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f738-113">Requirements</span></span>



| <span data-ttu-id="6f738-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f738-114">Requirement</span></span> | <span data-ttu-id="6f738-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6f738-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f738-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f738-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6f738-117">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6f738-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6f738-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f738-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6f738-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6f738-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6f738-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f738-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f738-121"><dt>Wiavideo. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f738-121"><dt>Wiavideo.h</dt></span></span> </dl>                         |
| <span data-ttu-id="6f738-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6f738-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f738-123"><dt>Wiascr.dll (versione 4,90 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="6f738-123"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




