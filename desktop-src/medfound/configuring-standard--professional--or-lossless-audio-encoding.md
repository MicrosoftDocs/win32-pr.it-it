---
description: Quando il codificatore Windows Media Audio enumera i tipi di output, identifica ogni tipo enumerato come standard, Professional o lossless.
ms.assetid: 1c3d22c3-10f7-454a-b1c1-372d684b6568
title: Configurazione della codifica audio standard, Professional o lossless
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e781c2c093b46a12fa4ad5434f97931a948ff9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749335"
---
# <a name="configuring-standard-professional-or-lossless-audio-encoding"></a><span data-ttu-id="16c1c-103">Configurazione della codifica audio standard, Professional o lossless</span><span class="sxs-lookup"><span data-stu-id="16c1c-103">Configuring Standard, Professional, or Lossless Audio Encoding</span></span>

<span data-ttu-id="16c1c-104">Quando il codificatore Windows Media Audio enumera i tipi di output, identifica ogni tipo enumerato come standard, Professional o lossless.</span><span class="sxs-lookup"><span data-stu-id="16c1c-104">When the Windows Media Audio encoder enumerates output types, it identifies each enumerated type as either Standard, Professional, or Lossless.</span></span> <span data-ttu-id="16c1c-105">È possibile determinare se un tipo di output è standard, Professional o lossless attenendosi alla procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="16c1c-105">You can determine whether an output type is Standard, Professional, or Lossless by performing the following steps.</span></span>

1.  <span data-ttu-id="16c1c-106">Chiamare [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) per ottenere un'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) che rappresenta il tipo di output.</span><span class="sxs-lookup"><span data-stu-id="16c1c-106">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to obtain an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface that represents the output type.</span></span>
2.  <span data-ttu-id="16c1c-107">Chiamare [**IMFMediaType:: Getrappresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation) per ottenere una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) che contiene informazioni sul tipo di output.</span><span class="sxs-lookup"><span data-stu-id="16c1c-107">Call [**IMFMediaType::GetRepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation) to get an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that contains information about the output type.</span></span>
3.  <span data-ttu-id="16c1c-108">Il membro **pbFormat** della struttura [**del \_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) punta a una struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) che contiene informazioni aggiuntive sul tipo di output.</span><span class="sxs-lookup"><span data-stu-id="16c1c-108">The **pbFormat** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure points to a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure that contains additional information about the output type.</span></span> <span data-ttu-id="16c1c-109">Esaminare il membro **wFormatTag** della struttura **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="16c1c-109">Inspect the **wFormatTag** member of the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="16c1c-110">Il valore 0x161 indica standard, il valore 0x162 indica Professional e il valore 0x163 indica senza perdita di valori.</span><span class="sxs-lookup"><span data-stu-id="16c1c-110">A value of 0x161 indicates Standard, a value of 0x162 indicates Professional, and a value of 0x163 indicates Lossless.</span></span>

<span data-ttu-id="16c1c-111">Se si impostano le proprietà nel codificatore Windows Media Audio prima di enumerare i tipi di output, è possibile limitare il numero di tipi di output enumerati.</span><span class="sxs-lookup"><span data-stu-id="16c1c-111">If you set properties on the Windows Media Audio encoder before you enumerate output types, you can limit the number of output types that are enumerated.</span></span> <span data-ttu-id="16c1c-112">Se ad esempio si impostano le proprietà VBR in modo appropriato, è possibile limitare i tipi di output enumerati a quelli presenti nella categoria lossless.</span><span class="sxs-lookup"><span data-stu-id="16c1c-112">For example, if you set the VBR properties appropriately, you can limit the enumerated output types to those that are in the Lossless category.</span></span>

## <a name="standard-audio-encoding"></a><span data-ttu-id="16c1c-113">Codifica audio standard</span><span class="sxs-lookup"><span data-stu-id="16c1c-113">Standard Audio Encoding</span></span>

<span data-ttu-id="16c1c-114">Per configurare la codifica audio standard, è possibile usare i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="16c1c-114">You can use the following steps to configure Standard audio encoding.</span></span>

1.  <span data-ttu-id="16c1c-115">Impostare le proprietà scelte nel codificatore.</span><span class="sxs-lookup"><span data-stu-id="16c1c-115">Set the properties of your choice on the encoder.</span></span>
2.  <span data-ttu-id="16c1c-116">Enumerare i tipi di output possibili.</span><span class="sxs-lookup"><span data-stu-id="16c1c-116">Enumerate the possible output types.</span></span>
3.  <span data-ttu-id="16c1c-117">Esaminare i tipi enumerati e sceglierne uno con un tag di formato audio 0x161.</span><span class="sxs-lookup"><span data-stu-id="16c1c-117">Inspect the enumerated types and choose one that has an audio format tag of 0x161.</span></span>
4.  <span data-ttu-id="16c1c-118">Impostare il tipo di output sul tipo scelto chiamando [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="16c1c-118">Set the output type to your chosen type by calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

## <a name="professional-audio-encoding"></a><span data-ttu-id="16c1c-119">Codifica audio professionale</span><span class="sxs-lookup"><span data-stu-id="16c1c-119">Professional Audio Encoding</span></span>

<span data-ttu-id="16c1c-120">Per configurare la codifica audio professionale, è possibile usare i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="16c1c-120">You can use the following steps to configure Professional audio encoding.</span></span>

1.  <span data-ttu-id="16c1c-121">Impostare le proprietà scelte nel codificatore.</span><span class="sxs-lookup"><span data-stu-id="16c1c-121">Set the properties of your choice on the encoder.</span></span>
2.  <span data-ttu-id="16c1c-122">Enumerare i tipi di output possibili.</span><span class="sxs-lookup"><span data-stu-id="16c1c-122">Enumerate the possible output types.</span></span>
3.  <span data-ttu-id="16c1c-123">Esaminare i tipi enumerati e sceglierne uno con un tag di formato audio 0x162.</span><span class="sxs-lookup"><span data-stu-id="16c1c-123">Inspect the enumerated types and choose one that has an audio format tag of 0x162.</span></span>
4.  <span data-ttu-id="16c1c-124">Impostare il tipo di output sul tipo scelto chiamando [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="16c1c-124">Set the output type to your chosen type by calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

## <a name="lossless-audio-encoding"></a><span data-ttu-id="16c1c-125">Codifica audio senza perdita di contenuti</span><span class="sxs-lookup"><span data-stu-id="16c1c-125">Lossless Audio Encoding</span></span>

<span data-ttu-id="16c1c-126">Per configurare la codifica audio senza perdita di codice, è possibile usare i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="16c1c-126">You can use the following steps to configure Lossless audio encoding.</span></span>

1.  <span data-ttu-id="16c1c-127">Impostare la proprietà [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) su **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="16c1c-127">Set the [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) property to **VARIANT\_TRUE**.</span></span>
2.  <span data-ttu-id="16c1c-128">Impostare la proprietà [**MFPKEY \_ vincolate \_ Enumerated \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) su **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="16c1c-128">Set the [**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) property to **VARIANT\_TRUE**.</span></span>
3.  <span data-ttu-id="16c1c-129">Impostare la proprietà [**MFPKEY \_ desired \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) su 100.</span><span class="sxs-lookup"><span data-stu-id="16c1c-129">Set the [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) property to 100.</span></span>
4.  <span data-ttu-id="16c1c-130">Enumerare i tipi di output.</span><span class="sxs-lookup"><span data-stu-id="16c1c-130">Enumerate output types.</span></span>
5.  <span data-ttu-id="16c1c-131">Impostare il tipo di output su uno dei tipi enumerati nel passaggio 4 chiamando [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="16c1c-131">Set the output type to one of the types enumerated in step 4 by calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

<span data-ttu-id="16c1c-132">Il codice seguente enumera tutti i tipi di output lossless per il codificatore Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="16c1c-132">The following code enumerates all of the lossless output types for the Windows Media Audio encoder.</span></span> <span data-ttu-id="16c1c-133">Il codice stampa il valore del tag di formato audio per ogni tipo enumerato.</span><span class="sxs-lookup"><span data-stu-id="16c1c-133">The code prints the value of the audio format tag for each enumerated type.</span></span> <span data-ttu-id="16c1c-134">Poiché tutti i tipi enumerati sono lossless, tutti i tag di formato hanno un valore 0x163.</span><span class="sxs-lookup"><span data-stu-id="16c1c-134">Because all of the enumerated types are lossless, all of those format tags have a value of 0x163.</span></span> <span data-ttu-id="16c1c-135">Si supponga che pIMT sia un puntatore a un'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) su un oggetto Windows Media Audio Encoder e che pStore sia un puntatore a un'interfaccia **IPropertyStore** sullo stesso oggetto.</span><span class="sxs-lookup"><span data-stu-id="16c1c-135">Assume that pIMT is a pointer to an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a Windows Media Audio encoder object and that pStore is a pointer to an **IPropertyStore** interface on the same object.</span></span> <span data-ttu-id="16c1c-136">Si supponga inoltre che HR sia una variabile di tipo **HRESULT** dichiarata in precedenza nel codice.</span><span class="sxs-lookup"><span data-stu-id="16c1c-136">Also assume that hr is a variable of type **HRESULT** that was declared previously in the code.</span></span>


```
PROPVARIANT prop;
prop.vt = VT_BOOL;
prop.boolVal = VARIANT_TRUE;
hr = pStore->SetValue(MFPKEY_VBRENABLED, prop);

if(SUCCEEDED(hr))
{
   hr = pStore->SetValue(MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY, prop);

   if(SUCCEEDED(hr))
   {
      prop.vt = VT_UI4;
      prop.ulVal = 100;
      hr = pStore->SetValue(MFPKEY_DESIRED_VBRQUALITY, prop);
      
      if(SUCCEEDED(hr))
      {           
         HRESULT hrAvailableType = S_OK;
         LONG j = 0;
         while(MF_E_NO_MORE_TYPES != hrAvailableType)
         {
            IMFMediaType* pOutputType = NULL;     
            hrAvailableType = pIMFT->GetOutputAvailableType(
               0, j, &pOutputType);

            if(SUCCEEDED(hrAvailableType))
            {
               AM_MEDIA_TYPE* pTypeRep = NULL;
               hr = pOutputType->GetRepresentation(
                  AM_MEDIA_TYPE_REPRESENTATION, (VOID**)&pTypeRep); 
                     
               if(SUCCEEDED(hr))
               {
                  WAVEFORMATEX* pwfex = (WAVEFORMATEX*)pTypeRep->pbFormat;
                  printf_s("%x\n", pwfex->wFormatTag);
                  pOutputType->FreeRepresentation(
                     AM_MEDIA_TYPE_REPRESENTATION, (VOID*)pTypeRep);
               }

               pOutputType->Release();
               ++j;
            }                                                                  
         } // while                 
      }                                
   } 
}
```



## <a name="related-topics"></a><span data-ttu-id="16c1c-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="16c1c-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16c1c-138">Configurazione della codifica audio</span><span class="sxs-lookup"><span data-stu-id="16c1c-138">Configuring Audio Encoding</span></span>](configuringaudioencoding.md)
</dt> </dl>

 

 
