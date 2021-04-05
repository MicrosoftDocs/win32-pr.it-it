---
description: Ottiene l'elemento radice di un albero di oggetti elemento utilizzato per rappresentare un dispositivo hardware Windows Image Acquisition (WIA) 2,0.
ms.assetid: bc31ad4a-0851-4510-a038-83646ffd5c98
title: 'Metodo IWiaItem2:: GetRootItem (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetRootItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: c8d4f004cc9c7cabaf4898f5e8c838a0399dc106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751778"
---
# <a name="iwiaitem2getrootitem-method"></a><span data-ttu-id="dc5fc-103">Metodo IWiaItem2:: GetRootItem</span><span class="sxs-lookup"><span data-stu-id="dc5fc-103">IWiaItem2::GetRootItem method</span></span>

<span data-ttu-id="dc5fc-104">Ottiene l'elemento radice di un albero di oggetti elemento utilizzato per rappresentare un dispositivo hardware Windows Image Acquisition (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="dc5fc-104">Gets the root item of a tree of item objects used to represent a Windows Image Acquisition (WIA) 2.0 hardware device.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc5fc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc5fc-105">Syntax</span></span>


```C++
HRESULT GetRootItem(
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="dc5fc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dc5fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc5fc-107">*ppIWiaItem2* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dc5fc-107">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc5fc-108">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="dc5fc-108">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="dc5fc-109">Riceve l'indirizzo di un puntatore all'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) dell'elemento radice.</span><span class="sxs-lookup"><span data-stu-id="dc5fc-109">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the root item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc5fc-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dc5fc-110">Return value</span></span>

<span data-ttu-id="dc5fc-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="dc5fc-111">Type: **HRESULT**</span></span>

<span data-ttu-id="dc5fc-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dc5fc-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dc5fc-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dc5fc-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc5fc-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc5fc-114">Remarks</span></span>

<span data-ttu-id="dc5fc-115">Dato qualsiasi oggetto [**IWiaItem2**](-wia-iwiaitem2.md) nell'albero degli oggetti di un dispositivo hardware WIA 2,0, l'applicazione recupera un puntatore all'elemento radice chiamando questa funzione.</span><span class="sxs-lookup"><span data-stu-id="dc5fc-115">Given any [**IWiaItem2**](-wia-iwiaitem2.md) object in the object tree of a WIA 2.0 hardware device, the application retrieves a pointer to the root item by calling this function.</span></span>

<span data-ttu-id="dc5fc-116">Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="dc5fc-116">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc5fc-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc5fc-117">Requirements</span></span>



| <span data-ttu-id="dc5fc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc5fc-118">Requirement</span></span> | <span data-ttu-id="dc5fc-119">Valore</span><span class="sxs-lookup"><span data-stu-id="dc5fc-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dc5fc-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc5fc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dc5fc-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dc5fc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="dc5fc-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc5fc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dc5fc-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dc5fc-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dc5fc-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dc5fc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc5fc-125"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc5fc-125"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="dc5fc-126">IDL</span><span class="sxs-lookup"><span data-stu-id="dc5fc-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dc5fc-127"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dc5fc-127"><dt>Wia.idl</dt></span></span> </dl> |



 

 
