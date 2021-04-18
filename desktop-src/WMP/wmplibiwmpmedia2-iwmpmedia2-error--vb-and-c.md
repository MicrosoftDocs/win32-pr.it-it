---
title: Proprietà errore IWMPMedia2
description: La proprietà Error ottiene un'interfaccia IWMPErrorItem se l'elemento multimediale presenta una condizione di errore.
ms.assetid: 57dc8aef-5f22-43da-87bc-fdc0c8ebe49b
keywords:
- Finestra Proprietà errore Media Player
- Proprietà Error Media Player Windows, interfaccia IWMPMedia2
- Interfaccia IWMPMedia2 Windows Media Player, proprietà Error
topic_type:
- apiref
api_name:
- IWMPMedia2.Error
- IWMPMedia2.get_Error
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2179b4604efd03574c78261575ce02311cd18a0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324376"
---
# <a name="iwmpmedia2error-property"></a><span data-ttu-id="1aba9-106">Proprietà IWMPMedia2:: Error</span><span class="sxs-lookup"><span data-stu-id="1aba9-106">IWMPMedia2::Error property</span></span>

<span data-ttu-id="1aba9-107">La proprietà **Error** ottiene un'interfaccia **IWMPErrorItem** se l'elemento multimediale presenta una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="1aba9-107">The **Error** property gets an **IWMPErrorItem** interface if the media item has an error condition.</span></span>

<span data-ttu-id="1aba9-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="1aba9-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1aba9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1aba9-109">Syntax</span></span>


```CSharp
public IWMPErrorItem Error {get;}
```


```VB

Public ReadOnly Property Error As IWMPErrorItem
```





## <a name="property-value"></a><span data-ttu-id="1aba9-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="1aba9-110">Property value</span></span>

<span data-ttu-id="1aba9-111">Interfaccia **wmplib. IWMPErrorItem** che consente di accedere alle informazioni sulla condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="1aba9-111">A **WMPLib.IWMPErrorItem** interface that provides access to information about the error condition.</span></span>

## <a name="remarks"></a><span data-ttu-id="1aba9-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="1aba9-112">Remarks</span></span>

<span data-ttu-id="1aba9-113">Se non è possibile riprodurre l'elemento multimediale, questa proprietà ottiene un'interfaccia **IWMPErrorItem** contenente informazioni sul problema riscontrato.</span><span class="sxs-lookup"><span data-stu-id="1aba9-113">If the media item cannot be played, this property gets an **IWMPErrorItem** interface that contains information about the problem encountered.</span></span>

## <a name="requirements"></a><span data-ttu-id="1aba9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1aba9-114">Requirements</span></span>



| <span data-ttu-id="1aba9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1aba9-115">Requirement</span></span> | <span data-ttu-id="1aba9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="1aba9-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1aba9-117">Versione</span><span class="sxs-lookup"><span data-stu-id="1aba9-117">Version</span></span><br/>   | <span data-ttu-id="1aba9-118">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="1aba9-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="1aba9-119">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1aba9-119">Namespace</span></span><br/> | <span data-ttu-id="1aba9-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="1aba9-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1aba9-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="1aba9-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1aba9-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1aba9-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1aba9-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1aba9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aba9-124">**IWMPErrorItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1aba9-124">**IWMPErrorItem (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1aba9-125">**Interfaccia IWMPMedia2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1aba9-125">**IWMPMedia2 Interface (VB and C#)**</span></span>](iwmpmedia2--vb-and-c.md)
</dt> </dl>

 

 





