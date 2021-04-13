---
title: Interfaccia IDWriteFont2
description: Rappresenta un tipo di carattere fisico in una raccolta di tipi di carattere.
ms.assetid: 4E3069AE-5882-4A26-A36D-BE7D7EE1B0C3
keywords:
- Scrittura diretta dell'interfaccia IDWriteFont2
- Scrittura diretta dell'interfaccia IDWriteFont2, descritta
topic_type:
- apiref
api_name:
- IDWriteFont2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82a47e56915747b0e118a6f63484b9dd3dcdbd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340842"
---
# <a name="idwritefont2-interface"></a><span data-ttu-id="2a787-105">Interfaccia IDWriteFont2</span><span class="sxs-lookup"><span data-stu-id="2a787-105">IDWriteFont2 interface</span></span>

<span data-ttu-id="2a787-106">Rappresenta un tipo di carattere fisico in una raccolta di tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="2a787-106">Represents a physical font in a font collection.</span></span>

<span data-ttu-id="2a787-107">Questa interfaccia consente di controllare se un percorso di rendering del colore è potenzialmente necessario.</span><span class="sxs-lookup"><span data-stu-id="2a787-107">This interface adds the ability to check if a color rendering path is potentially necessary.</span></span>

## <a name="members"></a><span data-ttu-id="2a787-108">Membri</span><span class="sxs-lookup"><span data-stu-id="2a787-108">Members</span></span>

<span data-ttu-id="2a787-109">L'interfaccia **IDWriteFont2** eredita da [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1).</span><span class="sxs-lookup"><span data-stu-id="2a787-109">The **IDWriteFont2** interface inherits from [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1).</span></span> <span data-ttu-id="2a787-110">**IDWriteFont2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2a787-110">**IDWriteFont2** also has these types of members:</span></span>

-   [<span data-ttu-id="2a787-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="2a787-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2a787-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="2a787-112">Methods</span></span>

<span data-ttu-id="2a787-113">L'interfaccia **IDWriteFont2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2a787-113">The **IDWriteFont2** interface has these methods.</span></span>



| <span data-ttu-id="2a787-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="2a787-114">Method</span></span>                                          | <span data-ttu-id="2a787-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a787-115">Description</span></span>                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="2a787-116">**IsColorFont**</span><span class="sxs-lookup"><span data-stu-id="2a787-116">**IsColorFont**</span></span>](idwritefont2-iscolorfont.md) | <span data-ttu-id="2a787-117">Consente di determinare se un percorso di rendering del colore è potenzialmente necessario.</span><span class="sxs-lookup"><span data-stu-id="2a787-117">Enables determining if a color rendering path is potentially necessary.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2a787-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a787-118">Requirements</span></span>



| <span data-ttu-id="2a787-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a787-119">Requirement</span></span> | <span data-ttu-id="2a787-120">Valore</span><span class="sxs-lookup"><span data-stu-id="2a787-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a787-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a787-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2a787-122">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2a787-122">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="2a787-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a787-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2a787-124">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2a787-124">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="2a787-125">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a787-125">Minimum supported phone</span></span><br/>  | <span data-ttu-id="2a787-126">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="2a787-126">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="2a787-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="2a787-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="2a787-128"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a787-128"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2a787-129">DLL</span><span class="sxs-lookup"><span data-stu-id="2a787-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a787-130"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a787-130"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2a787-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a787-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a787-132">**IDWriteFont1**</span><span class="sxs-lookup"><span data-stu-id="2a787-132">**IDWriteFont1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1)
</dt> </dl>

 

