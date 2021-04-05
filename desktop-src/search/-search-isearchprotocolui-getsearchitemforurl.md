---
description: Ottiene l'elemento di ricerca per i dati specificati. Questo metodo viene chiamato una volta per ogni URL elaborato dal gatherer e recupera un puntatore all'oggetto ISearchItem.
ms.assetid: 35893bc9-8327-44f9-a9fc-7855c5c063e3
title: 'Metodo ISearchProtocolUI:: GetSearchItemForUrl'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchProtocolUI.GetSearchItemForUrl
api_type:
- COM
api_location: ''
ms.openlocfilehash: f8a9bbe3459109946b7a4789d9b9f0fb7473ff05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750399"
---
# <a name="isearchprotocoluigetsearchitemforurl-method"></a><span data-ttu-id="62aca-104">Metodo ISearchProtocolUI:: GetSearchItemForUrl</span><span class="sxs-lookup"><span data-stu-id="62aca-104">ISearchProtocolUI::GetSearchItemForUrl method</span></span>

<span data-ttu-id="62aca-105">Ottiene l'elemento di ricerca per i dati specificati.</span><span class="sxs-lookup"><span data-stu-id="62aca-105">Gets the search item for the data specified.</span></span> <span data-ttu-id="62aca-106">Questo metodo viene chiamato una volta per ogni URL elaborato dal gatherer e recupera un puntatore all'oggetto [**ISearchItem**](-search-isearchitem.md) .</span><span class="sxs-lookup"><span data-stu-id="62aca-106">This method is called once for every URL processed by the gatherer, and retrieves a pointer to the [**ISearchItem**](-search-isearchitem.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="62aca-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62aca-107">Syntax</span></span>


```C++
HRESULT GetSearchItemForUrl(
  [in]          LPCOLESTR        pcwszURL,
  [in]          IItemPropertyBag *pPropertyBag,
  [out, retval] ISearchItem      **ppSearchItem
);
```



## <a name="parameters"></a><span data-ttu-id="62aca-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="62aca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62aca-109">*pcwszURL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62aca-109">*pcwszURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62aca-110">Tipo: **LPCOLESTR**</span><span class="sxs-lookup"><span data-stu-id="62aca-110">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="62aca-111">Puntatore a una stringa Unicode con terminazione di dati null contenente l'elemento di ricerca per l'URL a cui si accede.</span><span class="sxs-lookup"><span data-stu-id="62aca-111">Pointer to a null data terminated Unicode string containing the search item for the URL being accessed.</span></span>

</dd> <dt>

<span data-ttu-id="62aca-112">*pPropertyBag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62aca-112">*pPropertyBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62aca-113">Tipo: \**IItemPropertyBag \** _</span><span class="sxs-lookup"><span data-stu-id="62aca-113">Type: \**IItemPropertyBag\** _</span></span>

<span data-ttu-id="62aca-114">Puntatore a un oggetto [_ *IItemPropertyBag* \*](iitempropertybag.md) che contiene informazioni sull'elemento di ricerca, incluse le proprietà dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="62aca-114">Pointer to an [_ *IItemPropertyBag*\*](iitempropertybag.md) object that contains information about the search item, including the properties of the item.</span></span>

</dd> <dt>

<span data-ttu-id="62aca-115">*ppSearchItem* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="62aca-115">*ppSearchItem* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="62aca-116">Tipo: **[ **ISearchItem**](-search-isearchitem.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="62aca-116">Type: **[**ISearchItem**](-search-isearchitem.md)\*\***</span></span>

<span data-ttu-id="62aca-117">Riceve l'indirizzo di un puntatore all'oggetto [**ISearchItem**](-search-isearchitem.md) creato da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="62aca-117">Receives the address of a pointer to the [**ISearchItem**](-search-isearchitem.md) object created by this method.</span></span> <span data-ttu-id="62aca-118">Questo oggetto contiene informazioni sull'elemento di ricerca, ad esempio il nome del file dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="62aca-118">This object contains information about the search item, such as the item's file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62aca-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62aca-119">Return value</span></span>

<span data-ttu-id="62aca-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="62aca-120">Type: **HRESULT**</span></span>

<span data-ttu-id="62aca-121">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="62aca-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="62aca-122">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="62aca-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="62aca-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="62aca-123">Remarks</span></span>

<span data-ttu-id="62aca-124">Il metodo **ISearchProtocolUI:: GetSearchItemForUrl** è supportato solo in Windows XP e windows Server 2003 e non deve più essere usato.</span><span class="sxs-lookup"><span data-stu-id="62aca-124">The **ISearchProtocolUI::GetSearchItemForUrl** method is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="62aca-125">Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti in computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia [**ISearchProtocolUI**](-search-isearchprotocolui.md) e le API seguenti: le interfacce [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem**](-search-isearchitem.md) , la struttura [**LINKINFO**](-search-linkinfo.md) e l'enumerazione [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="62aca-125">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**ISearchProtocolUI**](-search-isearchprotocolui.md) interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="62aca-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62aca-126">Requirements</span></span>



| <span data-ttu-id="62aca-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="62aca-127">Requirement</span></span> | <span data-ttu-id="62aca-128">Valore</span><span class="sxs-lookup"><span data-stu-id="62aca-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="62aca-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62aca-129">Minimum supported client</span></span><br/> | <span data-ttu-id="62aca-130">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="62aca-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="62aca-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62aca-131">Minimum supported server</span></span><br/> | <span data-ttu-id="62aca-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="62aca-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="62aca-133">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="62aca-133">Redistributable</span></span><br/>          | <span data-ttu-id="62aca-134">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="62aca-134">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="62aca-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62aca-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62aca-136">**ISearchProtocolUI**</span><span class="sxs-lookup"><span data-stu-id="62aca-136">**ISearchProtocolUI**</span></span>](-search-isearchprotocolui.md)
</dt> </dl>

 

 




