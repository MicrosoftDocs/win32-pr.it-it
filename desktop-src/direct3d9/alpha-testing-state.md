---
description: Le applicazioni C++ possono usare il test alfa per controllare quando i pixel vengono scritti nell'area di destinazione di rendering.
ms.assetid: 368c3d12-2c8b-43e3-94c3-bccfe6c73e66
title: Stato test Alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020322ee31bc08352dbb2796ea5e7141d03c77c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305061"
---
# <a name="alpha-testing-state-direct3d-9"></a><span data-ttu-id="d602d-103">Stato test Alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d602d-103">Alpha Testing State (Direct3D 9)</span></span>

<span data-ttu-id="d602d-104">Le applicazioni C++ possono usare il test alfa per controllare quando i pixel vengono scritti nell'area di destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="d602d-104">C++ applications can use alpha testing to control when pixels are written to the render-target surface.</span></span> <span data-ttu-id="d602d-105">Utilizzando lo stato di rendering [**\_ ALPHATESTENABLE di D3DRS**](./d3drenderstatetype.md) , l'applicazione imposta il dispositivo Direct3D corrente in modo che verifichi ogni pixel in base a una funzione di test alfa.</span><span class="sxs-lookup"><span data-stu-id="d602d-105">By using the [**D3DRS\_ALPHATESTENABLE**](./d3drenderstatetype.md) render state, your application sets the current Direct3D device so that it tests each pixel according to an alpha test function.</span></span> <span data-ttu-id="d602d-106">Se il test ha esito positivo, il pixel viene scritto sulla superficie.</span><span class="sxs-lookup"><span data-stu-id="d602d-106">If the test succeeds, the pixel is written to the surface.</span></span> <span data-ttu-id="d602d-107">In caso contrario, Direct3D ignora il pixel.</span><span class="sxs-lookup"><span data-stu-id="d602d-107">If it does not, Direct3D ignores the pixel.</span></span> <span data-ttu-id="d602d-108">Selezionare la funzione di test alfa con lo stato di rendering **\_ ALPHAFUNC di D3DRS** .</span><span class="sxs-lookup"><span data-stu-id="d602d-108">Select the alpha test function with the **D3DRS\_ALPHAFUNC** render state.</span></span> <span data-ttu-id="d602d-109">L'applicazione può impostare un valore alfa di riferimento per tutti i pixel da confrontare utilizzando lo stato di rendering **\_ ALPHAREF di D3DRS** .</span><span class="sxs-lookup"><span data-stu-id="d602d-109">Your application can set a reference alpha value for all pixels to compare against by using the **D3DRS\_ALPHAREF** render state.</span></span>

<span data-ttu-id="d602d-110">L'uso più comune per i test alfa è quello di migliorare le prestazioni durante la rasterizzazione di oggetti quasi trasparenti.</span><span class="sxs-lookup"><span data-stu-id="d602d-110">The most common use for alpha testing is to improve performance when rasterizing objects that are nearly transparent.</span></span> <span data-ttu-id="d602d-111">Se i dati di colore da rasterizzare sono più opachi del colore in un determinato pixel (D3DPCMPCAPS \_ GREATEREQUAL), viene scritto il pixel.</span><span class="sxs-lookup"><span data-stu-id="d602d-111">If the color data being rasterized is more opaque than the color at a given pixel (D3DPCMPCAPS\_GREATEREQUAL), then the pixel is written.</span></span> <span data-ttu-id="d602d-112">In caso contrario, il rasterizzatore ignora completamente il pixel, salvando l'elaborazione necessaria per fondere i due colori.</span><span class="sxs-lookup"><span data-stu-id="d602d-112">Otherwise, the rasterizer ignores the pixel altogether, saving the processing required to blend the two colors.</span></span> <span data-ttu-id="d602d-113">Nell'esempio di codice seguente viene verificato se una determinata funzione di confronto è supportata e, in tal caso, vengono impostati i parametri della funzione di confronto necessari per migliorare le prestazioni durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="d602d-113">The following code example checks if a given comparison function is supported and, if so, it sets the comparison function parameters required to improve performance during rendering.</span></span>


```
// This code example assumes that pCaps is a
// D3DCAPS9 structure that was filled with a 
// previous call to IDirect3D9::GetDeviceCaps.

if (pCaps.AlphaCmpCaps & D3DPCMPCAPS_GREATEREQUAL)
{
    dev->SetRenderState(D3DRS_ALPHAREF, (DWORD)0x00000001);
    dev->SetRenderState(D3DRS_ALPHATESTENABLE, TRUE); 
    dev->SetRenderState(D3DRS_ALPHAFUNC, D3DCMP_GREATEREQUAL);
}

// If the comparison is not supported, render anyway. 
// The only drawback is no performance gain.
```



<span data-ttu-id="d602d-114">Non tutti i componenti hardware supportano tutte le funzionalità di test alfa.</span><span class="sxs-lookup"><span data-stu-id="d602d-114">Not all hardware supports all alpha-testing features.</span></span> <span data-ttu-id="d602d-115">È possibile controllare le funzionalità del dispositivo chiamando il metodo [**IDirect3D9:: GetDeviceCaps**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="d602d-115">You can check the device capabilities by calling the [**IDirect3D9::GetDeviceCaps**](/windows/desktop/api) method.</span></span> <span data-ttu-id="d602d-116">Dopo aver recuperato le funzionalità del dispositivo, controllare il membro AlphaCmpCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) associata per la funzione di confronto desiderata.</span><span class="sxs-lookup"><span data-stu-id="d602d-116">After retrieving the device capabilities, check the associated [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure's AlphaCmpCaps member for the desired comparison function.</span></span> <span data-ttu-id="d602d-117">Se il membro AlphaCmpCaps contiene solo la \_ funzionalità D3DPCMPCAPS Always o solo la \_ funzionalità D3DPCMPCAPS mai, il driver non supporta i test alfa.</span><span class="sxs-lookup"><span data-stu-id="d602d-117">If the AlphaCmpCaps member contains only the D3DPCMPCAPS\_ALWAYS capability or only the D3DPCMPCAPS\_NEVER capability, the driver does not support alpha tests.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d602d-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d602d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d602d-119">Stati di rendering</span><span class="sxs-lookup"><span data-stu-id="d602d-119">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
