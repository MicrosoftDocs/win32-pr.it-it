---
title: Metodo IDWriteFont2 IsColorFont
description: Consente di determinare se un percorso di rendering del colore è potenzialmente necessario.
ms.assetid: E21BB773-923E-461B-B966-A186ACD0164A
keywords:
- Scrittura diretta metodo IsColorFont
- Metodo IsColorFont scrittura diretta, interfaccia IDWriteFont2
- IDWriteFont2 Interface Direct Write, metodo IsColorFont
topic_type:
- apiref
api_name:
- IDWriteFont2.IsColorFont
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 353499c5e1c00ae37e585ecc6be47e5a2033d795
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400756"
---
# <a name="idwritefont2iscolorfont-method"></a><span data-ttu-id="6050e-106">Metodo IDWriteFont2:: IsColorFont</span><span class="sxs-lookup"><span data-stu-id="6050e-106">IDWriteFont2::IsColorFont method</span></span>

<span data-ttu-id="6050e-107">Consente di determinare se un percorso di rendering del colore è potenzialmente necessario.</span><span class="sxs-lookup"><span data-stu-id="6050e-107">Enables determining if a color rendering path is potentially necessary.</span></span>

## <a name="syntax"></a><span data-ttu-id="6050e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6050e-108">Syntax</span></span>


```C++
BOOL IsColorFont();
```



## <a name="parameters"></a><span data-ttu-id="6050e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6050e-109">Parameters</span></span>

<span data-ttu-id="6050e-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="6050e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6050e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6050e-111">Return value</span></span>

<span data-ttu-id="6050e-112">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="6050e-112">Type: **BOOL**</span></span>

<span data-ttu-id="6050e-113">Restituisce **true** se il tipo di carattere contiene informazioni sui colori (tabelle colr e CPAL); in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="6050e-113">Returns **TRUE** if the font has color information (COLR and CPAL tables); otherwise **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6050e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6050e-114">Requirements</span></span>



| <span data-ttu-id="6050e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6050e-115">Requirement</span></span> | <span data-ttu-id="6050e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6050e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6050e-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6050e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6050e-118">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6050e-118">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="6050e-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6050e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6050e-120">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6050e-120">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="6050e-121">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6050e-121">Minimum supported phone</span></span><br/>  | <span data-ttu-id="6050e-122">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="6050e-122">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="6050e-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="6050e-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="6050e-124"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6050e-124"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="6050e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6050e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6050e-126"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6050e-126"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6050e-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6050e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6050e-128">**IDWriteFont2**</span><span class="sxs-lookup"><span data-stu-id="6050e-128">**IDWriteFont2**</span></span>](idwritefont2.md)
</dt> </dl>

 

 





