---
description: Ottiene l'elemento padre nell'albero che rappresenta un dispositivo hardware Windows Image Acquisition (WIA) 2,0.
ms.assetid: c6fdaf1d-9875-4852-893c-813894d89f6c
title: 'Metodo IWiaItem2:: GetParentItem (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetParentItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 055625b98807103c3b79109216f6081d00564b15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343666"
---
# <a name="iwiaitem2getparentitem-method"></a><span data-ttu-id="c0047-103">Metodo IWiaItem2:: GetParentItem</span><span class="sxs-lookup"><span data-stu-id="c0047-103">IWiaItem2::GetParentItem method</span></span>

<span data-ttu-id="c0047-104">Ottiene l'elemento padre nell'albero che rappresenta un dispositivo hardware Windows Image Acquisition (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="c0047-104">Gets the parent item in the tree that represents a Windows Image Acquisition (WIA) 2.0 hardware device.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0047-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0047-105">Syntax</span></span>


```C++
HRESULT GetParentItem(
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="c0047-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c0047-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0047-107">*ppIWiaItem2* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c0047-107">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0047-108">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c0047-108">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="c0047-109">Riceve l'indirizzo di un puntatore all'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) del padre dell'elemento nell'albero degli oggetti elemento.</span><span class="sxs-lookup"><span data-stu-id="c0047-109">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the parent of the item in the tree of item objects.</span></span> <span data-ttu-id="c0047-110">Se questo metodo viene chiamato sulla radice della struttura ad albero, l'indirizzo restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="c0047-110">If this method is called on the root of the tree, then the returned address is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0047-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c0047-111">Return value</span></span>

<span data-ttu-id="c0047-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c0047-112">Type: **HRESULT**</span></span>

<span data-ttu-id="c0047-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c0047-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c0047-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c0047-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0047-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="c0047-115">Remarks</span></span>

<span data-ttu-id="c0047-116">Dato qualsiasi oggetto [**IWiaItem2**](-wia-iwiaitem2.md) nell'albero degli oggetti di un dispositivo hardware WIA 2,0, l'applicazione recupera un puntatore all'elemento padre chiamando questa funzione.</span><span class="sxs-lookup"><span data-stu-id="c0047-116">Given any [**IWiaItem2**](-wia-iwiaitem2.md) object in the object tree of a WIA 2.0 hardware device, the application retrieves a pointer to the parent item by calling this function.</span></span>

<span data-ttu-id="c0047-117">Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *ppIWiaItem2* se questi puntatori non sono **null**.</span><span class="sxs-lookup"><span data-stu-id="c0047-117">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter if these pointers are not **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0047-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0047-118">Requirements</span></span>



| <span data-ttu-id="c0047-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0047-119">Requirement</span></span> | <span data-ttu-id="c0047-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c0047-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c0047-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0047-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c0047-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c0047-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c0047-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0047-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c0047-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c0047-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c0047-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c0047-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0047-126"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0047-126"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0047-127">IDL</span><span class="sxs-lookup"><span data-stu-id="c0047-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c0047-128"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c0047-128"><dt>Wia.idl</dt></span></span> </dl> |



 

 
