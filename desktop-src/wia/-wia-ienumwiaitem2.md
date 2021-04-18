---
description: Utilizzato dalle applicazioni per enumerare gli oggetti IWiaItem2 nella cartella corrente dell'albero degli elementi.
ms.assetid: a82298e0-fbe7-4ef5-99c5-18ff60538e03
title: Interfaccia IEnumWiaItem2 (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: f6e41b3172793f696a9ea3c2d319bdee6ca3d691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308268"
---
# <a name="ienumwiaitem2-interface"></a><span data-ttu-id="1c363-103">Interfaccia IEnumWiaItem2</span><span class="sxs-lookup"><span data-stu-id="1c363-103">IEnumWiaItem2 interface</span></span>

<span data-ttu-id="1c363-104">Utilizzato dalle applicazioni per enumerare gli oggetti [**IWiaItem2**](-wia-iwiaitem2.md) nella cartella corrente dell'albero degli elementi.</span><span class="sxs-lookup"><span data-stu-id="1c363-104">Used by applications to enumerate [**IWiaItem2**](-wia-iwiaitem2.md) objects in the item tree's current folder.</span></span>

## <a name="members"></a><span data-ttu-id="1c363-105">Membri</span><span class="sxs-lookup"><span data-stu-id="1c363-105">Members</span></span>

<span data-ttu-id="1c363-106">L'interfaccia **IEnumWiaItem2** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1c363-106">The **IEnumWiaItem2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1c363-107">**IEnumWiaItem2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1c363-107">**IEnumWiaItem2** also has these types of members:</span></span>

-   [<span data-ttu-id="1c363-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="1c363-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1c363-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="1c363-109">Methods</span></span>

<span data-ttu-id="1c363-110">L'interfaccia **IEnumWiaItem2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="1c363-110">The **IEnumWiaItem2** interface has these methods.</span></span>



| <span data-ttu-id="1c363-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="1c363-111">Method</span></span>                                          | <span data-ttu-id="1c363-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c363-112">Description</span></span>                                                                                                                    |
|:------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c363-113">**Clone**</span><span class="sxs-lookup"><span data-stu-id="1c363-113">**Clone**</span></span>](-wia-ienumwiaitem2-clone.md)       | <span data-ttu-id="1c363-114">Crea un'istanza aggiuntiva dell'interfaccia **IEnumWiaItem2** e restituisce un puntatore.</span><span class="sxs-lookup"><span data-stu-id="1c363-114">Creates an additional instance of the **IEnumWiaItem2** interface and sends back a pointer to it.</span></span> <br/>                  |
| [<span data-ttu-id="1c363-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="1c363-115">**GetCount**</span></span>](-wia-ienumwiaitem2-getcount.md) | <span data-ttu-id="1c363-116">Restituisce il numero di elementi archiviati da questo enumeratore.</span><span class="sxs-lookup"><span data-stu-id="1c363-116">Returns the number of elements stored by this enumerator.</span></span> <br/>                                                          |
| [<span data-ttu-id="1c363-117">**Avanti**</span><span class="sxs-lookup"><span data-stu-id="1c363-117">**Next**</span></span>](-wia-ienumwiaitem2-next.md)         | <span data-ttu-id="1c363-118">Riempie una matrice di puntatori alle interfacce [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="1c363-118">Fills an array of pointers to [**IWiaItem2**](-wia-iwiaitem2.md) interfaces.</span></span><br/>                                       |
| [<span data-ttu-id="1c363-119">**Reset**</span><span class="sxs-lookup"><span data-stu-id="1c363-119">**Reset**</span></span>](-wia-ienumwiaitem2-reset.md)       | <span data-ttu-id="1c363-120">Reimposta il riferimento di enumerazione sul primo oggetto [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="1c363-120">Resets the enumeration reference to the first [**IWiaItem2**](-wia-iwiaitem2.md) object.</span></span> <br/>                          |
| [<span data-ttu-id="1c363-121">**Ignora**</span><span class="sxs-lookup"><span data-stu-id="1c363-121">**Skip**</span></span>](-wia-ienumwiaitem2-skip.md)         | <span data-ttu-id="1c363-122">Ignora il numero specificato di elementi durante un'enumerazione degli oggetti [**IWiaItem2**](-wia-iwiaitem2.md) disponibili.</span><span class="sxs-lookup"><span data-stu-id="1c363-122">Skips the specified number of items during an enumeration of available [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1c363-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c363-123">Requirements</span></span>



| <span data-ttu-id="1c363-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c363-124">Requirement</span></span> | <span data-ttu-id="1c363-125">Valore</span><span class="sxs-lookup"><span data-stu-id="1c363-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1c363-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c363-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1c363-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1c363-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1c363-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c363-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1c363-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1c363-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1c363-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1c363-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c363-131"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c363-131"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="1c363-132">IDL</span><span class="sxs-lookup"><span data-stu-id="1c363-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1c363-133"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1c363-133"><dt>Wia.idl</dt></span></span> </dl> |



 

 
