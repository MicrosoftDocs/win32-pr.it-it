---
description: Metodo virtuale pure che esegue l'override delle classi derivate.
ms.assetid: 05c73f6b-27f4-4930-b4d5-1688b6bf1791
title: Metodo CBaseControlVideo. GetStaticImage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetStaticImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13b0515e20202373954050b6fa18f10a20a76a6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328950"
---
# <a name="cbasecontrolvideogetstaticimage-method"></a><span data-ttu-id="3d8e0-103">CBaseControlVideo. GetStaticImage, metodo</span><span class="sxs-lookup"><span data-stu-id="3d8e0-103">CBaseControlVideo.GetStaticImage method</span></span>

<span data-ttu-id="3d8e0-104">Metodo virtuale pure che esegue l'override delle classi derivate.</span><span class="sxs-lookup"><span data-stu-id="3d8e0-104">Pure virtual method that derived classes override.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d8e0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d8e0-105">Syntax</span></span>


```C++
virtual HRESULT GetStaticImage(
   long *pBufferSize,
   long *pDIBImage
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="3d8e0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d8e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d8e0-107">*pBufferSize*</span><span class="sxs-lookup"><span data-stu-id="3d8e0-107">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="3d8e0-108">Puntatore alla dimensione del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="3d8e0-108">Pointer to the size of the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3d8e0-109">*pDIBImage*</span><span class="sxs-lookup"><span data-stu-id="3d8e0-109">*pDIBImage*</span></span> 
</dt> <dd>

<span data-ttu-id="3d8e0-110">Puntatore al buffer di output.</span><span class="sxs-lookup"><span data-stu-id="3d8e0-110">Pointer to the output buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d8e0-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3d8e0-111">Return value</span></span>

<span data-ttu-id="3d8e0-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3d8e0-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d8e0-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d8e0-113">Remarks</span></span>

<span data-ttu-id="3d8e0-114">Tramite l'interfaccia [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) , un'applicazione può richiedere che venga fornita una copia dell'immagine corrente in un buffer di memoria. alcuni renderer possono restituire e \_ NOTIMPL a questo se non lo supportano.</span><span class="sxs-lookup"><span data-stu-id="3d8e0-114">Through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface, an application can request that it be given a copy of the current image in a memory buffer (some renderers can return E\_NOTIMPL to this if they do not support it).</span></span> <span data-ttu-id="3d8e0-115">La classe derivata determina come recuperare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="3d8e0-115">The derived class determines how to retrieve the image.</span></span> <span data-ttu-id="3d8e0-116">Quando l'applicazione chiama **CBaseControlVideo:: GetStaticImage**, chiama questo metodo virtuale pure che la classe derivata deve eseguire l'override per implementarla.</span><span class="sxs-lookup"><span data-stu-id="3d8e0-116">When the application calls **CBaseControlVideo::GetStaticImage**, it calls this pure virtual method that the derived class should override to implement it.</span></span> <span data-ttu-id="3d8e0-117">Viene anche chiamato dalla funzione membro [**CBaseControlVideo:: GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) .</span><span class="sxs-lookup"><span data-stu-id="3d8e0-117">This is also called by the [**CBaseControlVideo::GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) member function.</span></span>

<span data-ttu-id="3d8e0-118">La classe fornisce una funzione membro helper, [**CBaseControlVideo:: CopyImage**](cbasecontrolvideo-copyimage.md), a cui può essere assegnato un esempio che contiene un'immagine e la funzione membro copia la relativa sezione (in base al rettangolo di origine corrente) nel buffer di output fornito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3d8e0-118">The class provides a helper member function, [**CBaseControlVideo::CopyImage**](cbasecontrolvideo-copyimage.md), that can be given a sample that contains an image, and the member function will copy the relevant section of it (based on the current source rectangle) into the output buffer supplied by the application.</span></span>

<span data-ttu-id="3d8e0-119">Nell'esempio seguente viene illustrata un'implementazione di questa funzione membro in una classe derivata.</span><span class="sxs-lookup"><span data-stu-id="3d8e0-119">The following example demonstrates an implementation of this member function in a derived class.</span></span> <span data-ttu-id="3d8e0-120">In questo esempio m \_ pRenderer include un oggetto di una classe derivata da [**CBaseVideoRenderer**](cbasevideorenderer.md).</span><span class="sxs-lookup"><span data-stu-id="3d8e0-120">In this example, m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md).</span></span>


```C++
// Return a copy of the current image in the video renderer
HRESULT CVideoText::GetStaticImage(long *pBufferSize,long *pDIBImage)
{
    // Get any sample the renderer may be holding.

    IMediaSample *pMediaSample = m_pRenderer->GetCurrentSample();
    if (pMediaSample == NULL) {
        return E_UNEXPECTED;
    }

    // Call the base class helper method to do the work.

    HRESULT hr = CopyImage(pMediaSample,       // Buffer containing image
                      &m_pRenderer->m_mtIn,    // Type representing bitmap
                      pBufferSize,             // Size of buffer for DIB
                     (BYTE*) pDIBImage);       // Data buffer for output

    pMediaSample->Release();
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="3d8e0-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d8e0-121">Requirements</span></span>



| <span data-ttu-id="3d8e0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d8e0-122">Requirement</span></span> | <span data-ttu-id="3d8e0-123">Valore</span><span class="sxs-lookup"><span data-stu-id="3d8e0-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d8e0-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d8e0-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3d8e0-125"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d8e0-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3d8e0-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="3d8e0-126">Library</span></span><br/> | <dl> <span data-ttu-id="3d8e0-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3d8e0-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d8e0-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d8e0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d8e0-129">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="3d8e0-129">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




