---
title: Metodo OnStatus IDRMStatusCallback
description: Il metodo OnStatus riceve i messaggi di stato dai processi DRM asincroni.
ms.assetid: 2a128088-0924-4c54-b08d-a1c7ea91e541
keywords:
- OnStatus metodo Windows Media Format
- Metodo OnStatus Windows Media Format, interfaccia IDRMStatusCallback
- Interfaccia IDRMStatusCallback Windows Media Format, metodo OnStatus
topic_type:
- apiref
api_name:
- IDRMStatusCallback.OnStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 754d59d74fb0365f423243e92565ac17b46628a5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045600"
---
# <a name="idrmstatuscallbackonstatus-method"></a><span data-ttu-id="7f38b-106">Metodo IDRMStatusCallback:: OnStatus</span><span class="sxs-lookup"><span data-stu-id="7f38b-106">IDRMStatusCallback::OnStatus method</span></span>

<span data-ttu-id="7f38b-107">Il metodo **OnStatus** riceve i messaggi di stato dai processi DRM asincroni.</span><span class="sxs-lookup"><span data-stu-id="7f38b-107">The **OnStatus** method receives status messages from asynchronous DRM processes.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f38b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f38b-108">Syntax</span></span>


```C++
HRESULT OnStatus(
  [in] MSDRM_STATUS      Status,
  [in] HRESULT           hr,
  [in] DRM_ATTR_DATATYPE dwType,
  [in] BYTE              *pValue,
  [in] void              *pvContext
);
```



## <a name="parameters"></a><span data-ttu-id="7f38b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7f38b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f38b-110">*Stato* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="7f38b-110">*Status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f38b-111">Codice di stato.</span><span class="sxs-lookup"><span data-stu-id="7f38b-111">Status code.</span></span> <span data-ttu-id="7f38b-112">I codici di messaggio sono definiti nel tipo di enumerazione **\_ dello stato MSDRM** .</span><span class="sxs-lookup"><span data-stu-id="7f38b-112">Message codes are defined in the **MSDRM\_STATUS** enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="7f38b-113">*risorse umane* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f38b-113">*hr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f38b-114">Codice restituito che supporta il messaggio di stato.</span><span class="sxs-lookup"><span data-stu-id="7f38b-114">Return code that supports the status message.</span></span>

</dd> <dt>

<span data-ttu-id="7f38b-115">*dwType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f38b-115">*dwType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f38b-116">Tipo di dati a cui punta *pValue*.</span><span class="sxs-lookup"><span data-stu-id="7f38b-116">Type of the data pointed to by *pValue*.</span></span> <span data-ttu-id="7f38b-117">Impostare su uno dei valori dell'enumerazione di [**\_ \_ tipo di dati DRM attr**](drm-attr-datatype.md) .</span><span class="sxs-lookup"><span data-stu-id="7f38b-117">Set to one of the values of the [**DRM\_ATTR\_DATATYPE**](drm-attr-datatype.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="7f38b-118">*pValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f38b-118">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f38b-119">Puntatore ai dati correlati al messaggio di stato.</span><span class="sxs-lookup"><span data-stu-id="7f38b-119">Pointer to data related to the status message.</span></span> <span data-ttu-id="7f38b-120">Il tipo di dati è determinato dal valore del parametro *dwType* .</span><span class="sxs-lookup"><span data-stu-id="7f38b-120">The type of data is determined by the value of the *dwType* parameter.</span></span> <span data-ttu-id="7f38b-121">Per ulteriori informazioni, vedere l'enumerazione del tipo di dati di [**DRM \_ attr \_**](drm-attr-datatype.md) .</span><span class="sxs-lookup"><span data-stu-id="7f38b-121">For more information, see the [**DRM\_ATTR\_DATATYPE**](drm-attr-datatype.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="7f38b-122">*pvContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f38b-122">*pvContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f38b-123">Parametro facoltativo che può essere usato per identificare l'oggetto che ha inviato il messaggio.</span><span class="sxs-lookup"><span data-stu-id="7f38b-123">Optional parameter that can be used to identify the object that sent the message.</span></span> <span data-ttu-id="7f38b-124">Impostando *pvContext* quando si registra questo callback, è possibile utilizzare lo stesso callback per gestire più processi asincroni.</span><span class="sxs-lookup"><span data-stu-id="7f38b-124">By setting *pvContext* when you register this callback, you can use the same callback to handle multiple asynchronous processes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f38b-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7f38b-125">Return value</span></span>

<span data-ttu-id="7f38b-126">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7f38b-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7f38b-127">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="7f38b-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7f38b-128">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7f38b-128">Return code</span></span>                                                                          | <span data-ttu-id="7f38b-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f38b-129">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="7f38b-130"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7f38b-130"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="7f38b-131">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="7f38b-131">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7f38b-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f38b-132">Remarks</span></span>

<span data-ttu-id="7f38b-133">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="7f38b-133">None.</span></span>

## <a name="see-also"></a><span data-ttu-id="7f38b-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f38b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f38b-135">**tipo di dati attr di DRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7f38b-135">**DRM\_ATTR\_DATATYPE**</span></span>](drm-attr-datatype.md)
</dt> <dt>

[<span data-ttu-id="7f38b-136">**Interfaccia IDRMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="7f38b-136">**IDRMStatusCallback Interface**</span></span>](idrmstatuscallback.md)
</dt> </dl>

 

 





