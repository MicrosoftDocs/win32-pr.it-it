---
description: Cerca nell'albero degli elementi secondari di un elemento usando il nome come chiave di ricerca.
ms.assetid: e4ce0bfb-9793-4928-b454-66ae1455b7b5
title: 'Metodo IWiaItem2:: FindItemByName (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.FindItemByName
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 821be7e4abd8d1396befa886093aa197bcdea7f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307363"
---
# <a name="iwiaitem2finditembyname-method"></a><span data-ttu-id="96d61-103">Metodo IWiaItem2:: FindItemByName</span><span class="sxs-lookup"><span data-stu-id="96d61-103">IWiaItem2::FindItemByName method</span></span>

<span data-ttu-id="96d61-104">Cerca nell'albero degli elementi secondari di un elemento usando il nome come chiave di ricerca.</span><span class="sxs-lookup"><span data-stu-id="96d61-104">Searches an item's tree of subitems using the name as the search key.</span></span>

## <a name="syntax"></a><span data-ttu-id="96d61-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96d61-105">Syntax</span></span>


```C++
HRESULT FindItemByName(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrFullItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="96d61-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="96d61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96d61-107">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96d61-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96d61-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="96d61-108">Type: **LONG**</span></span>

<span data-ttu-id="96d61-109">Attualmente non usato.</span><span class="sxs-lookup"><span data-stu-id="96d61-109">Currently unused.</span></span> <span data-ttu-id="96d61-110">Deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="96d61-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="96d61-111">*bstrFullItemName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96d61-111">*bstrFullItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96d61-112">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="96d61-112">Type: **BSTR**</span></span>

<span data-ttu-id="96d61-113">Specifica il nome dell'elemento da cercare.</span><span class="sxs-lookup"><span data-stu-id="96d61-113">Specifies the name fo the item to search for.</span></span>

</dd> <dt>

<span data-ttu-id="96d61-114">*ppIWiaItem2* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="96d61-114">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96d61-115">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="96d61-115">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="96d61-116">Riceve l'indirizzo di un puntatore all'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) dell'elemento trovato.</span><span class="sxs-lookup"><span data-stu-id="96d61-116">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the item found.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96d61-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96d61-117">Return value</span></span>

<span data-ttu-id="96d61-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="96d61-118">Type: **HRESULT**</span></span>

<span data-ttu-id="96d61-119">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="96d61-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="96d61-120">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="96d61-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="96d61-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="96d61-121">Remarks</span></span>

<span data-ttu-id="96d61-122">Questo metodo esegue la ricerca nell'albero degli elementi secondari dell'elemento corrente usando il nome come chiave di ricerca.</span><span class="sxs-lookup"><span data-stu-id="96d61-122">This method searches the current item's tree of sub-items using the name as the search key.</span></span> <span data-ttu-id="96d61-123">Se **IWiaItem2:: FindItemByName** trova l'elemento specificato da *bstrFullItemName*, archivia l'indirizzo di un puntatore nell'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) dell'elemento nel parametro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="96d61-123">If **IWiaItem2::FindItemByName** finds the item specified by *bstrFullItemName*, it stores the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the item in the *ppIWiaItem2* parameter.</span></span>

<span data-ttu-id="96d61-124">Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="96d61-124">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="96d61-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96d61-125">Requirements</span></span>



| <span data-ttu-id="96d61-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="96d61-126">Requirement</span></span> | <span data-ttu-id="96d61-127">Valore</span><span class="sxs-lookup"><span data-stu-id="96d61-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="96d61-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96d61-128">Minimum supported client</span></span><br/> | <span data-ttu-id="96d61-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="96d61-129">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="96d61-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96d61-130">Minimum supported server</span></span><br/> | <span data-ttu-id="96d61-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="96d61-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="96d61-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96d61-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="96d61-133"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="96d61-133"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="96d61-134">IDL</span><span class="sxs-lookup"><span data-stu-id="96d61-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="96d61-135"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="96d61-135"><dt>Wia.idl</dt></span></span> </dl> |



 

 
