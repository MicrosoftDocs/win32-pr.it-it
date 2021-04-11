---
description: Ottiene il componente Windows Image Acquisition (WIA) 2,0 Preview.
ms.assetid: 0b773c4c-f080-41fa-8902-4243a80fc67c
title: 'Metodo IWiaItem2:: GetPreviewComponent (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetPreviewComponent
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2e0881f68044c30731322c89d6cc2f19ce7277a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129422"
---
# <a name="iwiaitem2getpreviewcomponent-method"></a><span data-ttu-id="66dde-103">Metodo IWiaItem2:: GetPreviewComponent</span><span class="sxs-lookup"><span data-stu-id="66dde-103">IWiaItem2::GetPreviewComponent method</span></span>

<span data-ttu-id="66dde-104">Ottiene il componente Windows Image Acquisition (WIA) 2,0 Preview.</span><span class="sxs-lookup"><span data-stu-id="66dde-104">Gets the Windows Image Acquisition (WIA) 2.0 preview component.</span></span>

## <a name="syntax"></a><span data-ttu-id="66dde-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66dde-105">Syntax</span></span>


```C++
HRESULT GetPreviewComponent(
  [in]  LONG        lFlags,
  [out] IWiaPreview **ppWiaPreview
);
```



## <a name="parameters"></a><span data-ttu-id="66dde-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="66dde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66dde-107">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66dde-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66dde-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="66dde-108">Type: **LONG**</span></span>

<span data-ttu-id="66dde-109">Non usato.</span><span class="sxs-lookup"><span data-stu-id="66dde-109">Not used.</span></span> <span data-ttu-id="66dde-110">Impostare su 0.</span><span class="sxs-lookup"><span data-stu-id="66dde-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="66dde-111">*ppWiaPreview* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="66dde-111">*ppWiaPreview* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66dde-112">Tipo: **[ **IWiaPreview**](-wia-iwiapreview.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="66dde-112">Type: **[**IWiaPreview**](-wia-iwiapreview.md)\*\***</span></span>

<span data-ttu-id="66dde-113">Restituisce l'indirizzo di un puntatore all'interfaccia [**IWiaPreview**](-wia-iwiapreview.md) del componente di anteprima.</span><span class="sxs-lookup"><span data-stu-id="66dde-113">Returns the address of a pointer to the [**IWiaPreview**](-wia-iwiapreview.md) interface of the preview component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66dde-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="66dde-114">Return value</span></span>

<span data-ttu-id="66dde-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="66dde-115">Type: **HRESULT**</span></span>

<span data-ttu-id="66dde-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="66dde-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="66dde-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="66dde-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="66dde-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="66dde-118">Remarks</span></span>

<span data-ttu-id="66dde-119">Usare questa funzione per restituire un puntatore all'indirizzo del componente WIA 2,0 Preview per qualsiasi oggetto [**IWiaItem2**](-wia-iwiaitem2.md) nell'albero degli oggetti di un dispositivo hardware WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="66dde-119">Use this function to return a pointer to the address of the WIA 2.0 preview component for any [**IWiaItem2**](-wia-iwiaitem2.md) object in the object tree of a WIA 2.0 hardware device.</span></span>

<span data-ttu-id="66dde-120">Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *ppWiaPreview* .</span><span class="sxs-lookup"><span data-stu-id="66dde-120">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers that they receive through the *ppWiaPreview* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="66dde-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66dde-121">Requirements</span></span>



| <span data-ttu-id="66dde-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="66dde-122">Requirement</span></span> | <span data-ttu-id="66dde-123">Valore</span><span class="sxs-lookup"><span data-stu-id="66dde-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="66dde-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66dde-124">Minimum supported client</span></span><br/> | <span data-ttu-id="66dde-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="66dde-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="66dde-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66dde-126">Minimum supported server</span></span><br/> | <span data-ttu-id="66dde-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="66dde-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="66dde-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="66dde-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="66dde-129"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="66dde-129"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="66dde-130">IDL</span><span class="sxs-lookup"><span data-stu-id="66dde-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="66dde-131"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="66dde-131"><dt>Wia.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66dde-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66dde-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66dde-133">**IWiaItem2**</span><span class="sxs-lookup"><span data-stu-id="66dde-133">**IWiaItem2**</span></span>](-wia-iwiaitem2.md)
</dt> <dt>

[<span data-ttu-id="66dde-134">**IWiaPreview**</span><span class="sxs-lookup"><span data-stu-id="66dde-134">**IWiaPreview**</span></span>](-wia-iwiapreview.md)
</dt> </dl>

 

 
