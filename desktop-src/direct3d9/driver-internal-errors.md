---
description: In Direct3D 9 Direct3D consentirà al driver di restituire i codici di errore, ad esempio E \_ OutOfMemory, D3DERR \_ OUTOFVIDEOMEMORY e D3DERR UNSUPPORTEDCOLORARG, in \_ modo che un'applicazione sia in grado di rispondere.
ms.assetid: 483fdb03-e453-4a1b-bd8e-294e9e9a20c2
title: Errori interni del driver (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c81b0ee8ba50edb3c14fbd9a22c9fa9dc93aab8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124761"
---
# <a name="driver-internal-errors-direct3d-9"></a><span data-ttu-id="bdc3d-103">Errori interni del driver (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bdc3d-103">Driver Internal Errors (Direct3D 9)</span></span>

<span data-ttu-id="bdc3d-104">In Direct3D 9 Direct3D consentirà al driver di restituire i codici di errore, ad esempio E \_ OutOfMemory, D3DERR \_ OUTOFVIDEOMEMORY e D3DERR UNSUPPORTEDCOLORARG, in \_ modo che un'applicazione sia in grado di rispondere.</span><span class="sxs-lookup"><span data-stu-id="bdc3d-104">In Direct3D 9, Direct3D will allow the driver to return error codes such as E\_OUTOFMEMORY, D3DERR\_OUTOFVIDEOMEMORY, and D3DERR\_UNSUPPORTEDCOLORARG so that an application would be able to respond to them.</span></span> <span data-ttu-id="bdc3d-105">Tuttavia, talvolta le chiamate API che hanno generato questi tipi restituiti vengono caricate in un buffer dei comandi e vengono inserite in batch per essere inviate alla GPU (vedere [controllo delle ottimizzazioni di runtime e driver](accurately-profiling-direct3d-api-calls.md)).</span><span class="sxs-lookup"><span data-stu-id="bdc3d-105">However, sometimes the API calls that generated these return types get loaded into a command buffer and are batched up to be sent to the GPU (see [Controlling Runtime and Driver Optimizations](accurately-profiling-direct3d-api-calls.md)).</span></span> <span data-ttu-id="bdc3d-106">In questo caso, gli errori non possono essere inoltrati all'applicazione quando è necessario eseguire un'azione, quindi il codice di errore viene utilizzato dal runtime e viene effettuata una nota sull'oggetto dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bdc3d-106">In this case, the errors cannot be relayed to the application when action needs to be taken, so the error code is consumed by the runtime and a note is made on the device object that this happened.</span></span> <span data-ttu-id="bdc3d-107">Successivamente, quando l'applicazione richiama [**IDirect3DDevice9::P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)reinviate, **IDirect3DDevice9::P** reinviate restituirà D3DERR \_ DRIVERINTERNALERROR.</span><span class="sxs-lookup"><span data-stu-id="bdc3d-107">Later when the application invokes [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present), **IDirect3DDevice9::Present** will return D3DERR\_DRIVERINTERNALERROR.</span></span> <span data-ttu-id="bdc3d-108">Questo è il motivo per cui l'approccio migliore per un'applicazione da eseguire quando si riceve un DRIVERINTERNALERROR di D3DERR \_ da **IDirect3DDevice9::P inviato** il rimandamento è quello di eliminare e ricreare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bdc3d-108">This is why the best approach for an application to take when receiving a D3DERR\_DRIVERINTERNALERROR from **IDirect3DDevice9::Present** is to destroy and recreate the device.</span></span>

<span data-ttu-id="bdc3d-109">Se si vuole provare a eseguire il debug ulteriormente, di seguito sono riportati alcuni suggerimenti per provare a determinare quale chiamata API genera l'errore:</span><span class="sxs-lookup"><span data-stu-id="bdc3d-109">If you want to try to debug further, here are a couple of suggestions for trying to figure out which API call is generating the error:</span></span>

-   <span data-ttu-id="bdc3d-110">Poiché l'elenco dei possibili valori restituiti non è completo, è possibile provare a individuare la chiamata che ha avuto esito negativo circondando ogni chiamata all'API come la seguente:</span><span class="sxs-lookup"><span data-stu-id="bdc3d-110">Because the list of possible return values is not complete, you can try to find which call is failing by surrounding each API call like this:</span></span>

    ```
    TRACE ( "Calling DrawPrimitive" );
    d3ddev->DrawPrim(...);
    TRACE ( "done\n" );
    ```

    

    <span data-ttu-id="bdc3d-111">Il flusso di debug dell'output dovrebbe quindi mostrare la chiamata che causa il problema.</span><span class="sxs-lookup"><span data-stu-id="bdc3d-111">The output debug stream should then show the call that is causing the problem.</span></span>

-   <span data-ttu-id="bdc3d-112">Inoltre, a scopo di debug, provare a chiamare [**IDirect3DDevice9:: ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) immediatamente prima di ogni [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) per verificare se esiste un ulteriore problema con il driver di dispositivo (operazione non supportata, combinazione inutilizzabile di formati di trama e così via).</span><span class="sxs-lookup"><span data-stu-id="bdc3d-112">Additionally, for debugging purposes, try calling [**IDirect3DDevice9::ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) immediately before each [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) to see if there is an additional problem with the device driver (unsupported operation, unusable combination of texture formats, etc).</span></span>

    > [!Note]  
    > <span data-ttu-id="bdc3d-113">[**IDirect3DDevice9:: ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) deve essere usato con cautela e con moderazione a causa della quantità di lavoro di convalida che il driver deve eseguire per restituire una risposta.</span><span class="sxs-lookup"><span data-stu-id="bdc3d-113">[**IDirect3DDevice9::ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) should be used carefully and sparingly because of the amount of validation work the driver needs to perform to return an answer.</span></span>

     

## <a name="related-topics"></a><span data-ttu-id="bdc3d-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bdc3d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdc3d-115">Suggerimenti per la programmazione</span><span class="sxs-lookup"><span data-stu-id="bdc3d-115">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
