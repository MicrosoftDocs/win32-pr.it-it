---
description: Acquisizione della catena di certificati dei driver
ms.assetid: bc7b346c-3382-4f2b-90b6-03f6a1a5a9ce
title: Acquisizione della catena di certificati dei driver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3f46e395550ca4bcb02396fe09126c1232f2c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103875974"
---
# <a name="obtaining-the-drivers-certificate-chain"></a><span data-ttu-id="6f821-103">Acquisizione della catena di certificati dei driver</span><span class="sxs-lookup"><span data-stu-id="6f821-103">Obtaining the Drivers Certificate Chain</span></span>

<span data-ttu-id="6f821-104">Per usare Certified Output Protocol (COPP), l'applicazione deve prima di tutto compilare un grafo DirectShow che includa il filtro di rendering video mixing (VMR-7 o VMR-9).</span><span class="sxs-lookup"><span data-stu-id="6f821-104">To use Certified Output Protection Protocol (COPP), the application first must build a DirectShow graph that includes the Video Mixing Render filter (VMR-7 or VMR-9).</span></span> <span data-ttu-id="6f821-105">Il filtro renderer video precedente non supporta COPP.</span><span class="sxs-lookup"><span data-stu-id="6f821-105">The older Video Renderer filter does not support COPP.</span></span> <span data-ttu-id="6f821-106">Prima di chiamare i metodi COPP, l'applicazione deve compilare un grafico di riproduzione video e connettere il decodificatore al pin di input del filtro VMR.</span><span class="sxs-lookup"><span data-stu-id="6f821-106">Before calling any COPP methods, the application must build a video playback graph and connect the decoder to the VMR filter's input pin.</span></span> <span data-ttu-id="6f821-107">Non è necessario riprodurre il file video.</span><span class="sxs-lookup"><span data-stu-id="6f821-107">It is not necessary to play the video file.</span></span>

<span data-ttu-id="6f821-108">Dopo aver compilato il grafo, eseguire una query su VMR per l'interfaccia [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) e quindi chiamare [**IAMCertifiedOutputProtection:: backexchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange).</span><span class="sxs-lookup"><span data-stu-id="6f821-108">After building the graph, query the VMR for the [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) interface, and then call [**IAMCertifiedOutputProtection::KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange).</span></span> <span data-ttu-id="6f821-109">Questo metodo restituisce un numero casuale a 128 bit tipizzato come GUID, insieme a un puntatore a una matrice di byte che contiene la catena di certificati XML del driver in formato UTF-8.</span><span class="sxs-lookup"><span data-stu-id="6f821-109">This method returns a 128-bit random number typed as a GUID, along with a pointer to a byte array that contains the driver's XML certificate chain in UTF-8 format.</span></span> <span data-ttu-id="6f821-110">Il codice seguente illustra come ottenere la catena di certificati.</span><span class="sxs-lookup"><span data-stu-id="6f821-110">The following code shows how to get the certificate chain.</span></span>


```C++
GUID guidRandom;
BYTE *pbCertificateChain = NULL;
DWORD cbCertificateChainLen;   // Size of the certificate chain, in bytes.
hr = pCOPP->KeyExchange(&guidRandom, &pbCertificateChain,
         &cbCertificateChainLen);
if (SUCCEEDED(hr))
{
    // TODO: Validate the certificate chain and get the driver's
    // public key. 

    // When you are done, free the buffer that contains the 
    // certificate chain.
    CoTaskMemFree(pbCertificateChain);
}
```



## <a name="related-topics"></a><span data-ttu-id="6f821-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6f821-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f821-112">Uso di COPP (Certified Output Protocol)</span><span class="sxs-lookup"><span data-stu-id="6f821-112">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



