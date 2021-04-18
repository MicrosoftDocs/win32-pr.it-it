---
description: Consente al filtro di elaborazione delle immagini di scrivere di nuovo le proprietà sul driver (e sul dispositivo).
ms.assetid: b9bb8d81-2945-46ba-a0a2-7009000574aa
title: 'Metodo IWiaImageFilter:: ApplyProperties (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.ApplyProperties
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3c20527ee587b975adea34e7c480349836620015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312397"
---
# <a name="iwiaimagefilterapplyproperties-method"></a><span data-ttu-id="1a962-103">Metodo IWiaImageFilter:: ApplyProperties</span><span class="sxs-lookup"><span data-stu-id="1a962-103">IWiaImageFilter::ApplyProperties method</span></span>

<span data-ttu-id="1a962-104">Consente al filtro di elaborazione delle immagini di scrivere di nuovo le proprietà sul driver (e sul dispositivo).</span><span class="sxs-lookup"><span data-stu-id="1a962-104">Enables the image processing filter to write properties back to the driver (and device).</span></span>

## <a name="syntax"></a><span data-ttu-id="1a962-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-105">Syntax</span></span>


```C++
HRESULT ApplyProperties(
  [in] IWiaPropertyStorage *pWiaPropertyStorage
);
```



## <a name="parameters"></a><span data-ttu-id="1a962-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a962-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a962-107">*pWiaPropertyStorage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a962-107">*pWiaPropertyStorage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a962-108">Tipo: \**[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) \** _</span><span class="sxs-lookup"><span data-stu-id="1a962-108">Type: \**[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)\** _</span></span>

<span data-ttu-id="1a962-109">Specifica un puntatore a [_ *IWiaPropertyStorage* \*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) per le proprietà da applicare.</span><span class="sxs-lookup"><span data-stu-id="1a962-109">Specifies a pointer to the [_ *IWiaPropertyStorage*\*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) for the properties to be applied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a962-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1a962-110">Return value</span></span>

<span data-ttu-id="1a962-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1a962-111">Type: **HRESULT**</span></span>

<span data-ttu-id="1a962-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1a962-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1a962-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1a962-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a962-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a962-114">Remarks</span></span>

<span data-ttu-id="1a962-115">Non chiamare questo metodo direttamente dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1a962-115">Do not call this method directly from your application.</span></span> <span data-ttu-id="1a962-116">Viene chiamato da Windows Image Acquisition (WIA) 2,0 dopo che il filtro di elaborazione delle immagini ha elaborato i dati non elaborati.</span><span class="sxs-lookup"><span data-stu-id="1a962-116">It is called by Windows Image Acquisition (WIA) 2.0 after the image processing filter has processed the raw data.</span></span>

<span data-ttu-id="1a962-117">*pWiaPropertyStorage* è l'interfaccia [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) in cui il filtro di elaborazione delle immagini deve scrivere le proprietà.</span><span class="sxs-lookup"><span data-stu-id="1a962-117">*pWiaPropertyStorage* is the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface into which the image processing filter should write properties.</span></span> <span data-ttu-id="1a962-118">Un filtro di elaborazione immagini deve usare solo il metodo [IPropertyStorage:: WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) per scrivere le proprietà.</span><span class="sxs-lookup"><span data-stu-id="1a962-118">An image processing filter should use only the [IPropertyStorage::WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) method to write properties.</span></span>

<span data-ttu-id="1a962-119">Questo metodo consente al filtro di elaborazione delle immagini di scrivere di nuovo le proprietà nel driver (e nel dispositivo).</span><span class="sxs-lookup"><span data-stu-id="1a962-119">This method allows the image processing filter to write properties back to the driver (and device).</span></span> <span data-ttu-id="1a962-120">Questa operazione può essere necessaria per i filtri che implementano funzionalità come l'esposizione automatica durante l'analisi dei film.</span><span class="sxs-lookup"><span data-stu-id="1a962-120">This may be necessary for filters that implement features such as auto-exposure during film scanning.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a962-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a962-121">Requirements</span></span>



| <span data-ttu-id="1a962-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a962-122">Requirement</span></span> | <span data-ttu-id="1a962-123">Valore</span><span class="sxs-lookup"><span data-stu-id="1a962-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1a962-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a962-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1a962-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1a962-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1a962-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a962-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1a962-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1a962-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1a962-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1a962-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a962-129"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a962-129"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="1a962-130">IDL</span><span class="sxs-lookup"><span data-stu-id="1a962-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1a962-131"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1a962-131"><dt>Wia.idl</dt></span></span> </dl> |



 

 
