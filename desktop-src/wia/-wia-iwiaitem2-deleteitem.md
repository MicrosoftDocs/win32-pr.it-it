---
description: Rimuove l'oggetto IWiaItem2 corrente dalla struttura ad albero di oggetti del dispositivo.
ms.assetid: 247eb36f-3e5c-4030-8334-1a4028b3eb44
title: Metodo IWiaItem2::D eleteItem (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeleteItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: ef6a4204b591f06811f0941ca0ceed72b76151db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307367"
---
# <a name="iwiaitem2deleteitem-method"></a><span data-ttu-id="2a439-103">IWiaItem2::D Metodo eleteItem</span><span class="sxs-lookup"><span data-stu-id="2a439-103">IWiaItem2::DeleteItem method</span></span>

<span data-ttu-id="2a439-104">Rimuove l'oggetto [**IWiaItem2**](-wia-iwiaitem2.md) corrente dalla struttura ad albero di oggetti del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2a439-104">Removes the current [**IWiaItem2**](-wia-iwiaitem2.md) object from the device's object tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a439-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2a439-105">Syntax</span></span>


```C++
HRESULT DeleteItem(
  [in] LONG lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="2a439-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2a439-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a439-107">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2a439-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a439-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="2a439-108">Type: **LONG**</span></span>

<span data-ttu-id="2a439-109">Attualmente non usato.</span><span class="sxs-lookup"><span data-stu-id="2a439-109">Currently unused.</span></span> <span data-ttu-id="2a439-110">Deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="2a439-110">Should be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a439-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2a439-111">Return value</span></span>

<span data-ttu-id="2a439-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2a439-112">Type: **HRESULT**</span></span>

<span data-ttu-id="2a439-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2a439-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2a439-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2a439-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a439-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a439-115">Remarks</span></span>

<span data-ttu-id="2a439-116">Il sistema di runtime Windows Image Acquisition (WIA) 2,0 rappresenta ogni dispositivo hardware WIA 2,0 connesso al computer dell'utente come albero gerarchico di oggetti [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="2a439-116">The Windows Image Acquisition (WIA) 2.0 run-time system represents each WIA 2.0 hardware device connected to the user's computer as a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="2a439-117">Un dispositivo WIA 2,0 specificato può o meno consentire alle applicazioni di eliminare oggetti **IWiaItem2** dal relativo albero.</span><span class="sxs-lookup"><span data-stu-id="2a439-117">A given WIA 2.0 device may or may not allow applications to delete **IWiaItem2** objects from its tree.</span></span> <span data-ttu-id="2a439-118">Gli elementi con elementi figlio non possono essere eliminati.</span><span class="sxs-lookup"><span data-stu-id="2a439-118">Items that have children cannot be deleted.</span></span> <span data-ttu-id="2a439-119">Per eseguire una query sul dispositivo per la funzionalità di eliminazione degli elementi, è necessario usare l'interfaccia [**IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) .</span><span class="sxs-lookup"><span data-stu-id="2a439-119">The [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface must be used to query the device for item deletion capability.</span></span>

<span data-ttu-id="2a439-120">Se il dispositivo supporta l'eliminazione di elementi nella struttura ad albero di [**IWiaItem2**](-wia-iwiaitem2.md) , chiamare il metodo **IWiaItem2::D eleteitem** per rimuovere l'oggetto **IWiaItem2** .</span><span class="sxs-lookup"><span data-stu-id="2a439-120">If the device supports item deletion in its [**IWiaItem2**](-wia-iwiaitem2.md) tree, call the **IWiaItem2::DeleteItem** method to remove the **IWiaItem2** object.</span></span> <span data-ttu-id="2a439-121">Si noti che questo metodo elimina un oggetto solo dopo che tutti i riferimenti all'oggetto sono stati rilasciati.</span><span class="sxs-lookup"><span data-stu-id="2a439-121">Note that this method only deletes an object after all references to the object have been released.</span></span> <span data-ttu-id="2a439-122">Se l'eliminazione di un elemento non è riuscita, \_ viene restituito E DeleteItem.</span><span class="sxs-lookup"><span data-stu-id="2a439-122">If the deletion of an item has failed, E\_DELETEITEM is returned.</span></span> <span data-ttu-id="2a439-123">Il valore numerico per questo errore non è ancora definito.</span><span class="sxs-lookup"><span data-stu-id="2a439-123">The numeric value for this error is not yet defined.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a439-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a439-124">Requirements</span></span>



| <span data-ttu-id="2a439-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a439-125">Requirement</span></span> | <span data-ttu-id="2a439-126">Valore</span><span class="sxs-lookup"><span data-stu-id="2a439-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2a439-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a439-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2a439-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2a439-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2a439-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a439-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2a439-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2a439-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2a439-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a439-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a439-132"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a439-132"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="2a439-133">IDL</span><span class="sxs-lookup"><span data-stu-id="2a439-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2a439-134"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2a439-134"><dt>Wia.idl</dt></span></span> </dl> |



 

 




