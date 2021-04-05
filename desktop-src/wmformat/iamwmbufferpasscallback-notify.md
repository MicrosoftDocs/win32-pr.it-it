---
title: Metodo di notifica IAMWMBufferPassCallback
description: Il metodo Notify viene chiamato dal pin per ogni buffer recapitato durante il flusso.
ms.assetid: 3f252754-c784-4ffd-bcfc-fab73fa02b9a
keywords:
- Notifica metodo Windows Media Format
- Metodo di notifica Windows Media Format, interfaccia IAMWMBufferPassCallback
- Interfaccia IAMWMBufferPassCallback-formato Windows Media, metodo Notify
topic_type:
- apiref
api_name:
- IAMWMBufferPassCallback.Notify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8f362262b36dee0bfc9a18e57010d102b2fa2cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118254"
---
# <a name="iamwmbufferpasscallbacknotify-method"></a><span data-ttu-id="40d67-106">Metodo IAMWMBufferPassCallback:: Notify</span><span class="sxs-lookup"><span data-stu-id="40d67-106">IAMWMBufferPassCallback::Notify method</span></span>

<span data-ttu-id="40d67-107">Il metodo **Notify** viene chiamato dal pin per ogni buffer recapitato durante il flusso.</span><span class="sxs-lookup"><span data-stu-id="40d67-107">The **Notify** method is called by the pin for each buffer that is delivered during streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="40d67-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40d67-108">Syntax</span></span>


```C++
HRESULT Notify(
  [in] INSSBuffer3    *pNSSBuffer3,
  [in] IPin           *pPin,
  [in] REFERENCE_TIME *prtStart,
  [in] REFERENCE_TIME *prtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="40d67-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="40d67-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40d67-110">*pNSSBuffer3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40d67-110">*pNSSBuffer3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40d67-111">Puntatore all'interfaccia [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) esposta nell'esempio multimediale.</span><span class="sxs-lookup"><span data-stu-id="40d67-111">Pointer to the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface exposed on the media sample.</span></span>

</dd> <dt>

<span data-ttu-id="40d67-112">*pPin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40d67-112">*pPin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40d67-113">Puntatore al pin associato al flusso multimediale a cui appartiene l'esempio.</span><span class="sxs-lookup"><span data-stu-id="40d67-113">Pointer to the pin associated with the media stream that the sample belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="40d67-114">*prtStart* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40d67-114">*prtStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40d67-115">Ora di inizio dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="40d67-115">Start time of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="40d67-116">*prtEnd* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40d67-116">*prtEnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40d67-117">Ora di fine dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="40d67-117">End time of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40d67-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="40d67-118">Return value</span></span>

<span data-ttu-id="40d67-119">Non viene specificato alcun valore restituito specifico.</span><span class="sxs-lookup"><span data-stu-id="40d67-119">No particular return value is specified.</span></span> <span data-ttu-id="40d67-120">Il pin chiamante ignora **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="40d67-120">The calling pin ignores the **HRESULT**.</span></span>

## <a name="remarks"></a><span data-ttu-id="40d67-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="40d67-121">Remarks</span></span>

<span data-ttu-id="40d67-122">Questo metodo consente a un'applicazione di esaminare e agire sulle informazioni nel buffer multimediale prima che il contenuto del buffer venga elaborato.</span><span class="sxs-lookup"><span data-stu-id="40d67-122">This method enables an application to examine and act on information in the media buffer before the buffer contents are processed.</span></span> <span data-ttu-id="40d67-123">L'applicazione è responsabile della conoscenza del tipo di supporto sul pin.</span><span class="sxs-lookup"><span data-stu-id="40d67-123">The application is responsible for knowing the media type on the pin.</span></span> <span data-ttu-id="40d67-124">Queste informazioni possono essere ottenute ottenendo prima le informazioni sul flusso dal profilo e quindi chiamando il metodo [**IConfigAsfWriter2:: StreamNumFromPin**](iconfigasfwriter2-streamnumfrompin.md) per determinare quale pin è associato a ogni flusso.</span><span class="sxs-lookup"><span data-stu-id="40d67-124">This information can be obtained by first getting the stream information from the profile and then calling [**IConfigAsfWriter2::StreamNumFromPin**](iconfigasfwriter2-streamnumfrompin.md) method to determine which pin is associated with each stream.</span></span>

## <a name="see-also"></a><span data-ttu-id="40d67-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40d67-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40d67-126">**Informazioni di riferimento su DirectShow QASF**</span><span class="sxs-lookup"><span data-stu-id="40d67-126">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="40d67-127">**Interfaccia IAMWMBufferPassCallback**</span><span class="sxs-lookup"><span data-stu-id="40d67-127">**IAMWMBufferPassCallback Interface**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback)
</dt> <dt>

[<span data-ttu-id="40d67-128">**Interfaccia INSSBuffer3**</span><span class="sxs-lookup"><span data-stu-id="40d67-128">**INSSBuffer3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)
</dt> </dl>

 

 