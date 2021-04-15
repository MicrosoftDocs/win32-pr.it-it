---
description: Crea un oggetto enumeratore e passa di nuovo un puntatore alla relativa interfaccia IEnumWiaItem2 per le cartelle con elementi nell'albero IWiaItem2 di un dispositivo Windows Image Acquisition (WIA) 2,0.
ms.assetid: 0862bb6f-0464-491a-8cad-60b92d9609f1
title: 'Metodo IWiaItem2:: EnumChildItems (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumChildItems
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2de76d9bf43d10e08e5a85cd2a32d6b377680d18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485068"
---
# <a name="iwiaitem2enumchilditems-method"></a><span data-ttu-id="3f183-103">Metodo IWiaItem2:: EnumChildItems</span><span class="sxs-lookup"><span data-stu-id="3f183-103">IWiaItem2::EnumChildItems method</span></span>

<span data-ttu-id="3f183-104">Crea un oggetto enumeratore e passa di nuovo un puntatore alla relativa interfaccia [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) per le cartelle con elementi nell'albero [**IWiaItem2**](-wia-iwiaitem2.md) di un dispositivo Windows Image Acquisition (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="3f183-104">Creates an enumerator object and passes back a pointer to its [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface for folders with items in the [**IWiaItem2**](-wia-iwiaitem2.md) tree of a Windows Image Acquisition (WIA) 2.0 device.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f183-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f183-105">Syntax</span></span>


```C++
HRESULT EnumChildItems(
  [in]  const GUID          *pCategoryGUID,
  [out]       IEnumWiaItem2 **ppIEnumWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="3f183-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3f183-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f183-107">*pCategoryGUID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f183-107">*pCategoryGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f183-108">Tipo: \**const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="3f183-108">Type: \**const GUID\** _</span></span>

<span data-ttu-id="3f183-109">Specifica un puntatore a una categoria per cui vengono enumerati i nodi figlio.</span><span class="sxs-lookup"><span data-stu-id="3f183-109">Specifies a pointer to a category for which child nodes are enumerated.</span></span> <span data-ttu-id="3f183-110">Se _ \* NULL \* \*, vengono enumerati tutti i nodi figlio.</span><span class="sxs-lookup"><span data-stu-id="3f183-110">If _\*NULL\*\*, then all child nodes are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="3f183-111">*ppIEnumWiaItem2* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3f183-111">*ppIEnumWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f183-112">Tipo: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="3f183-112">Type: **[**IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span></span>

<span data-ttu-id="3f183-113">Riceve l'indirizzo di un puntatore all'interfaccia [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) creata da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="3f183-113">Receives the address of a pointer to the [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface that this method creates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f183-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3f183-114">Return value</span></span>

<span data-ttu-id="3f183-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3f183-115">Type: **HRESULT**</span></span>

<span data-ttu-id="3f183-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3f183-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3f183-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3f183-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f183-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f183-118">Remarks</span></span>

<span data-ttu-id="3f183-119">Il sistema di runtime WIA 2,0 rappresenta ogni dispositivo hardware WIA 2,0 come albero gerarchico di oggetti [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="3f183-119">The WIA 2.0 run-time system represents each WIA 2.0 hardware device as a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="3f183-120">Il metodo **IWiaItem2:: EnumChildItems** consente alle applicazioni di enumerare gli elementi figlio nell'elemento corrente.</span><span class="sxs-lookup"><span data-stu-id="3f183-120">The **IWiaItem2::EnumChildItems** method enables applications to enumerate child items in the current item.</span></span> <span data-ttu-id="3f183-121">Tuttavia, può essere applicato solo a elementi che sono cartelle.</span><span class="sxs-lookup"><span data-stu-id="3f183-121">However, it can only be applied to items that are folders.</span></span>

<span data-ttu-id="3f183-122">Se la cartella non è vuota, contiene un sottoalbero di oggetti [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="3f183-122">If the folder is not empty, it contains a subtree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="3f183-123">Il metodo **IWiaItem2:: EnumChildItems** enumera tutti gli elementi contenuti nella cartella.</span><span class="sxs-lookup"><span data-stu-id="3f183-123">The **IWiaItem2::EnumChildItems** method enumerates all of the items contained in the folder.</span></span> <span data-ttu-id="3f183-124">Archivia un puntatore a un enumeratore nel parametro *ppIEnumWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="3f183-124">It stores a pointer to an enumerator in the *ppIEnumWiaItem2* parameter.</span></span> <span data-ttu-id="3f183-125">Le applicazioni utilizzano il puntatore dell'enumeratore per eseguire l'enumerazione degli elementi figlio di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="3f183-125">Applications use the enumerator pointer to perform the enumeration of an object's child items.</span></span>

<span data-ttu-id="3f183-126">Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *ppIEnumWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="3f183-126">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnumWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f183-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f183-127">Requirements</span></span>



| <span data-ttu-id="3f183-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f183-128">Requirement</span></span> | <span data-ttu-id="3f183-129">Valore</span><span class="sxs-lookup"><span data-stu-id="3f183-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3f183-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f183-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3f183-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3f183-131">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3f183-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f183-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3f183-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3f183-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3f183-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3f183-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f183-135"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f183-135"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="3f183-136">IDL</span><span class="sxs-lookup"><span data-stu-id="3f183-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3f183-137"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3f183-137"><dt>Wia.idl</dt></span></span> </dl> |



 

 
