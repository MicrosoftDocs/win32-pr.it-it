---
description: L'interfaccia ITablet3 consente l'esecuzione di query multitouch per l'input.
ms.assetid: 949f2d83-7761-4d60-b8fe-5a9ac7567238
title: Interfaccia ITablet3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f37d70888ccedf0fe941f0387c064aba37dc287e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317929"
---
# <a name="itablet3-interface"></a><span data-ttu-id="28fb7-103">Interfaccia ITablet3</span><span class="sxs-lookup"><span data-stu-id="28fb7-103">ITablet3 interface</span></span>

<span data-ttu-id="28fb7-104">L'interfaccia ITablet3 consente l'esecuzione di query multitouch per l'input.</span><span class="sxs-lookup"><span data-stu-id="28fb7-104">The ITablet3 interface enables multitouch querying for input.</span></span>

## <a name="members"></a><span data-ttu-id="28fb7-105">Membri</span><span class="sxs-lookup"><span data-stu-id="28fb7-105">Members</span></span>

<span data-ttu-id="28fb7-106">L'interfaccia **ITablet3** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="28fb7-106">The **ITablet3** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="28fb7-107">**ITablet3** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="28fb7-107">**ITablet3** also has these types of members:</span></span>

-   [<span data-ttu-id="28fb7-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="28fb7-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="28fb7-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="28fb7-109">Methods</span></span>

<span data-ttu-id="28fb7-110">L'interfaccia **ITablet3** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="28fb7-110">The **ITablet3** interface has these methods.</span></span>



| <span data-ttu-id="28fb7-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="28fb7-111">Method</span></span>                                                  | <span data-ttu-id="28fb7-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28fb7-112">Description</span></span>                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="28fb7-113">**GetMaximumCursors**</span><span class="sxs-lookup"><span data-stu-id="28fb7-113">**GetMaximumCursors**</span></span>](itablet3-getmaximumcursors.md) | <span data-ttu-id="28fb7-114">Recupera il numero massimo di input supportati.</span><span class="sxs-lookup"><span data-stu-id="28fb7-114">Retrieves the maximum number of inputs supported.</span></span><br/>        |
| [<span data-ttu-id="28fb7-115">**MultiTouch**</span><span class="sxs-lookup"><span data-stu-id="28fb7-115">**isMultiTouch**</span></span>](itablet3-ismultitouch.md)           | <span data-ttu-id="28fb7-116">Indica se il multitouch è abilitato per questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="28fb7-116">Indicates whether multitouch is enabled for this object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="28fb7-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="28fb7-117">Remarks</span></span>

<span data-ttu-id="28fb7-118">Gli sviluppatori non devono usare questa interfaccia</span><span class="sxs-lookup"><span data-stu-id="28fb7-118">Developers should not use this interface</span></span>

<span data-ttu-id="28fb7-119">Il codice seguente descrive il modo in cui viene definita l'interfaccia **ITablet3** .</span><span class="sxs-lookup"><span data-stu-id="28fb7-119">The following code describes how the **ITablet3** interface is defined.</span></span>

``` syntax
[
  object,
  uuid(AC0E3951-0A2F-448E-88D0-49DA0C453460)
  pointer_default(unique)
]
interface ITablet3 : IUnknown
{
    HRESULT IsMultiTouch([out] BOOL *pIsMultiTouch);

    HRESULT GetMaximumCursors([out] ULONG *pMaximumCursors);
};
  
```

## <a name="requirements"></a><span data-ttu-id="28fb7-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28fb7-120">Requirements</span></span>



| <span data-ttu-id="28fb7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="28fb7-121">Requirement</span></span> | <span data-ttu-id="28fb7-122">Valore</span><span class="sxs-lookup"><span data-stu-id="28fb7-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28fb7-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28fb7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="28fb7-124">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="28fb7-124">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="28fb7-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28fb7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="28fb7-126">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="28fb7-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="28fb7-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="28fb7-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="28fb7-128"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="28fb7-128"><dt>Wisptis.exe</dt></span></span> </dl> |



 

