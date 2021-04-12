---
title: Aggiunta della proprietà Wet Mix
description: Aggiunta della proprietà Wet Mix
ms.assetid: 4605d893-8ac0-42fd-a1ac-51430561f174
keywords:
- Plug-in di Windows Media Player, proprietà di esempio Echo
- plug-in, proprietà di esempio Echo
- plug-in di elaborazione dei segnali digitali, proprietà di esempio Echo
- Plug-in DSP, proprietà di esempio Echo
- Esempio di plug-in Echo DSP, proprietà
- Esempio di plug-in Echo DSP, proprietà Wet Mix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad6af8e7b4857ccbf6b725044575d1b8524aaf50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330095"
---
# <a name="adding-the-wet-mix-property"></a><span data-ttu-id="1dac6-109">Aggiunta della proprietà Wet Mix</span><span class="sxs-lookup"><span data-stu-id="1dac6-109">Adding the Wet Mix Property</span></span>

<span data-ttu-id="1dac6-110">È necessario aggiungere il codice per fornire la proprietà aggiuntiva per il livello di effetto.</span><span class="sxs-lookup"><span data-stu-id="1dac6-110">You must add the code to provide the additional property for the effect level.</span></span>

<span data-ttu-id="1dac6-111">Nella sezione [aggiunta di proprietà al plug-in audio DSP di esempio](adding-properties-to-the-sample-audio-dsp-plug-in.md) vengono fornite informazioni dettagliate su come aggiungere una nuova proprietà utilizzando Visual C++.</span><span class="sxs-lookup"><span data-stu-id="1dac6-111">The section [Adding Properties to the Sample Audio DSP Plug-in](adding-properties-to-the-sample-audio-dsp-plug-in.md) provides details about how to add a new property using Visual C++.</span></span> <span data-ttu-id="1dac6-112">Questa sezione illustra come aggiungere il codice manualmente.</span><span class="sxs-lookup"><span data-stu-id="1dac6-112">This section shows you how to add the code manually.</span></span> <span data-ttu-id="1dac6-113">Questa operazione comporta l'aggiunta di codice nelle stesse tre posizioni in cui è stato modificato il codice per la proprietà tempo di ritardo.</span><span class="sxs-lookup"><span data-stu-id="1dac6-113">This entails adding code in the same three places where you modified the code for the delay time property.</span></span>

<span data-ttu-id="1dac6-114">Aggiungere i prototipi per i \_ metodi Get WETMIX e put \_ WETMIX immediatamente dopo gli altri prototipi di metodo di proprietà in Echo. h.</span><span class="sxs-lookup"><span data-stu-id="1dac6-114">Add the prototypes for the get\_wetmix and put\_wetmix methods immediately following the other property method prototypes in Echo.h.</span></span> <span data-ttu-id="1dac6-115">Usare la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="1dac6-115">Use the following syntax:</span></span>


```C++
STDMETHOD(get_wetmix)(double *pVal);
STDMETHOD(put_wetmix)(double newVal);

```



<span data-ttu-id="1dac6-116">A questo punto, aggiungere l'implementazione per ogni metodo immediatamente dopo le altre implementazioni di proprietà in Echo. cpp.</span><span class="sxs-lookup"><span data-stu-id="1dac6-116">Now, add the implementation for each method immediately following the other property implementations in Echo.cpp.</span></span> <span data-ttu-id="1dac6-117">Nell'esempio seguente viene illustrato il codice per entrambi i metodi:</span><span class="sxs-lookup"><span data-stu-id="1dac6-117">The following example shows the code for both methods:</span></span>


```C++
// Property get to retrieve the wet mix value by using the public interface.
STDMETHODIMP CEcho::get_wetmix(double *pVal)
{
    if ( NULL == pVal )
    {
        return E_POINTER;
    }

    *pVal = m_fWetMix;

    return S_OK;
}

// Property put to store the wet mix value by using the public interface.
STDMETHODIMP CEcho::put_wetmix(double newVal)
{
    m_fWetMix = newVal;

    // Calculate m_fDryMix
    m_fDryMix = 1.0 - m_fWetMix;
    
    return S_OK;
}

```



<span data-ttu-id="1dac6-118">Si noti che l'implementazione di put \_ WETMIX include il codice per calcolare il valore corretto per m \_ fDryMix.</span><span class="sxs-lookup"><span data-stu-id="1dac6-118">Notice that the implementation of put\_wetmix includes the code to calculate the correct value for m\_fDryMix.</span></span> <span data-ttu-id="1dac6-119">Ogni volta che viene specificato un nuovo valore per m \_ fWetMix, questo calcolo è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1dac6-119">Each time a new value is specified for m\_fWetMix, this calculation is required.</span></span>

<span data-ttu-id="1dac6-120">Aggiungere il codice seguente nella definizione dell'interfaccia subito dopo il codice per i metodi Delay in Echo. idl:</span><span class="sxs-lookup"><span data-stu-id="1dac6-120">Add the following code in the interface definition just after the code for the delay methods in Echo.idl:</span></span>


```C++
HRESULT get_wetmix([out] double *pVal);
HRESULT put_wetmix([in] double newVal);

```



## <a name="related-topics"></a><span data-ttu-id="1dac6-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1dac6-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1dac6-122">**Proprietà di esempio Echo**</span><span class="sxs-lookup"><span data-stu-id="1dac6-122">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 




