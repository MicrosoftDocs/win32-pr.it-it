---
description: Specifica il metodo usato per codificare le informazioni sul vettore di movimento.
ms.assetid: 22ffdb77-9266-42e5-be41-fc7457141bba
title: Proprietà MFPKEY_DELTAMVRANGEINDEX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c72d923659e64c9a0dcab40811e31d7752924700
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528675"
---
# <a name="mfpkey_deltamvrangeindex-property"></a><span data-ttu-id="0ab83-103">\_Proprietà DELTAMVRANGEINDEX di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="0ab83-103">MFPKEY\_DELTAMVRANGEINDEX Property</span></span>

<span data-ttu-id="0ab83-104">Specifica il metodo usato per codificare le informazioni sul vettore di movimento.</span><span class="sxs-lookup"><span data-stu-id="0ab83-104">Specifies the method used to encode the motion vector information.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="0ab83-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="0ab83-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="0ab83-106">g \_ wszWMVCDeltaMVRangeIndex</span><span class="sxs-lookup"><span data-stu-id="0ab83-106">g\_wszWMVCDeltaMVRangeIndex</span></span>

## <a name="data-type"></a><span data-ttu-id="0ab83-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0ab83-107">Data Type</span></span>

<span data-ttu-id="0ab83-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="0ab83-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="0ab83-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="0ab83-109">Default Value</span></span>

<span data-ttu-id="0ab83-110">0</span><span class="sxs-lookup"><span data-stu-id="0ab83-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="0ab83-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ab83-111">Remarks</span></span>

<span data-ttu-id="0ab83-112">Se questa proprietà è impostata, il codificatore aumenta l'intervallo di vettori di movimento Delta nei campi.</span><span class="sxs-lookup"><span data-stu-id="0ab83-112">If this property is set, the encoder increases the delta motion vector range in fields.</span></span> <span data-ttu-id="0ab83-113">Le informazioni sul vettore di movimento sono valide solo per i campi interlacciati.</span><span class="sxs-lookup"><span data-stu-id="0ab83-113">Motion vector information is valid only for interlaced fields.</span></span>

<span data-ttu-id="0ab83-114">Questa proprietà può essere impostata su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="0ab83-114">This property may be set to one of the following values:</span></span>



| <span data-ttu-id="0ab83-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0ab83-115">Value</span></span> | <span data-ttu-id="0ab83-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ab83-116">Description</span></span>                                                                          |
|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0ab83-117">0</span><span class="sxs-lookup"><span data-stu-id="0ab83-117">0</span></span>     | <span data-ttu-id="0ab83-118">Usare l'intervallo di vettori di movimento Delta esistente.</span><span class="sxs-lookup"><span data-stu-id="0ab83-118">Use the existing delta motion vector range.</span></span>                                          |
| <span data-ttu-id="0ab83-119">1</span><span class="sxs-lookup"><span data-stu-id="0ab83-119">1</span></span>     | <span data-ttu-id="0ab83-120">Raddoppiare l'intervallo del vettore di movimento Delta nella direzione orizzontale.</span><span class="sxs-lookup"><span data-stu-id="0ab83-120">Double the delta motion vector range in the horizontal direction.</span></span>                    |
| <span data-ttu-id="0ab83-121">2</span><span class="sxs-lookup"><span data-stu-id="0ab83-121">2</span></span>     | <span data-ttu-id="0ab83-122">Raddoppiare l'intervallo del vettore di movimento Delta nella direzione verticale.</span><span class="sxs-lookup"><span data-stu-id="0ab83-122">Double the delta motion vector range in the vertical direction.</span></span>                      |
| <span data-ttu-id="0ab83-123">3</span><span class="sxs-lookup"><span data-stu-id="0ab83-123">3</span></span>     | <span data-ttu-id="0ab83-124">Raddoppiare l'intervallo del vettore di movimento Delta nelle direzioni orizzontale e verticale.</span><span class="sxs-lookup"><span data-stu-id="0ab83-124">Double the delta motion vector range in both the horizontal and vertical directions.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="0ab83-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ab83-125">Requirements</span></span>



| <span data-ttu-id="0ab83-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ab83-126">Requirement</span></span> | <span data-ttu-id="0ab83-127">Valore</span><span class="sxs-lookup"><span data-stu-id="0ab83-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ab83-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ab83-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0ab83-129">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0ab83-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0ab83-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ab83-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0ab83-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0ab83-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0ab83-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ab83-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ab83-133"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ab83-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ab83-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ab83-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ab83-135">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0ab83-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




