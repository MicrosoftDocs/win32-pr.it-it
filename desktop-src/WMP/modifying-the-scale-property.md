---
title: Modifica della proprietà scale
description: Modifica della proprietà scale
ms.assetid: 32ebaa54-ed13-4b10-8876-bf8e188d7317
keywords:
- Plug-in di Windows Media Player, proprietà di esempio Echo
- plug-in, proprietà di esempio Echo
- plug-in di elaborazione dei segnali digitali, proprietà di esempio Echo
- Plug-in DSP, proprietà di esempio Echo
- Esempio di plug-in Echo DSP, proprietà scale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd91e2315db9d0d1e14d2aec55f79a8b05c442ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298087"
---
# <a name="modifying-the-scale-property"></a><span data-ttu-id="9c38c-108">Modifica della proprietà scale</span><span class="sxs-lookup"><span data-stu-id="9c38c-108">Modifying the Scale Property</span></span>

<span data-ttu-id="9c38c-109">L'implementazione della procedura guidata predefinita espone la proprietà scale.</span><span class="sxs-lookup"><span data-stu-id="9c38c-109">The default wizard implementation exposes the scale property.</span></span> <span data-ttu-id="9c38c-110">È possibile modificare l'implementazione esistente per esporre la proprietà tempo di ritardo.</span><span class="sxs-lookup"><span data-stu-id="9c38c-110">You can change the existing implementation to expose the delay time property instead.</span></span>

<span data-ttu-id="9c38c-111">Per prima cosa, usare l'esempio seguente per modificare i prototipi di funzione per Get \_ scale e put \_ scale in Echo. h.</span><span class="sxs-lookup"><span data-stu-id="9c38c-111">First, use the following example to change the function prototypes for get\_scale and put\_scale in Echo.h.</span></span> <span data-ttu-id="9c38c-112">Modificare il nome dei metodi e i tipi di dati per i parametri:</span><span class="sxs-lookup"><span data-stu-id="9c38c-112">Change the name of the methods and the data types for the parameters:</span></span>


```C++
// IEcho methods
STDMETHOD(get_delay)(DWORD *pVal);
STDMETHOD(put_delay)(DWORD newVal);

```



<span data-ttu-id="9c38c-113">Modificare quindi le implementazioni dei \_ metodi Get scale e put \_ scale in Echo. cpp.</span><span class="sxs-lookup"><span data-stu-id="9c38c-113">Next, change the implementations of the get\_scale and put\_scale methods in Echo.cpp.</span></span> <span data-ttu-id="9c38c-114">Fare in modo che il codice corrisponda agli esempi seguenti:</span><span class="sxs-lookup"><span data-stu-id="9c38c-114">Make the code match the following examples:</span></span>


```C++
// Formerly get_scale
STDMETHODIMP CEcho::get_delay(DWORD *pVal)
{
    if ( NULL == pVal )
    {
        return E_POINTER;
    }

    *pVal = m_dwDelayTime;

    return S_OK;
}

// Formerly put_scale
STDMETHODIMP CEcho::put_delay(DWORD newVal)
{
    m_dwDelayTime = newVal;

    return S_OK;
}

```



<span data-ttu-id="9c38c-115">Il codice di esempio precedente modifica i nomi dei metodi e i tipi di dati dei parametri.</span><span class="sxs-lookup"><span data-stu-id="9c38c-115">The preceding example code changes the method names and the parameter data types.</span></span> <span data-ttu-id="9c38c-116">Il nome della variabile membro deve essere stato modificato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="9c38c-116">The member variable name should have been changed previously.</span></span> <span data-ttu-id="9c38c-117">Ricordarsi di modificare i commenti che introducono anche ogni metodo.</span><span class="sxs-lookup"><span data-stu-id="9c38c-117">Remember to change the comments that introduce each method as well.</span></span>

<span data-ttu-id="9c38c-118">A questo punto, modificare la definizione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="9c38c-118">Now, change the interface definition.</span></span> <span data-ttu-id="9c38c-119">Il codice seguente sostituisce il codice nella dichiarazione dell'interfaccia IEcho in Echo. idl:</span><span class="sxs-lookup"><span data-stu-id="9c38c-119">The following code replaces the code in the IEcho interface declaration in Echo.idl:</span></span>


```C++
HRESULT get_delay([out] DWORD *pVal);
HRESULT put_delay([in] DWORD newVal);

```



## <a name="related-topics"></a><span data-ttu-id="9c38c-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9c38c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c38c-121">**Proprietà di esempio Echo**</span><span class="sxs-lookup"><span data-stu-id="9c38c-121">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 




