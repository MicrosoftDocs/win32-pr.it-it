---
description: Recupero della catena di certificati dei driver
ms.assetid: bc7b346c-3382-4f2b-90b6-03f6a1a5a9ce
title: Recupero della catena di certificati dei driver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2641c27c3d24ab45a87b16e8c805228c316d9f89428cd29abbaff347b5aae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684561"
---
# <a name="obtaining-the-drivers-certificate-chain"></a>Recupero della catena di certificati dei driver

Per usare il protocollo COPP (Certified Output Protection Protocol), l'applicazione deve prima di tutto compilare un grafo di DirectShow che include il filtro di rendering di combinazione video (VMR-7 o VMR-9). Il filtro del renderer video precedente non supporta COPP. Prima di chiamare qualsiasi metodo COPP, l'applicazione deve compilare un grafico di riproduzione video e connettere il decodificatore al pin di input del filtro VMR. Non è necessario riprodurre il file video.

Dopo aver compilato il grafo, eseguire una query sulla macchina virtuale per [**l'interfaccia IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) e quindi chiamare [**IAMCertifiedOutputProtection::KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange). Questo metodo restituisce un numero casuale a 128 bit digitato come GUID, insieme a un puntatore a una matrice di byte che contiene la catena di certificati XML del driver in formato UTF-8. Il codice seguente illustra come ottenere la catena di certificati.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del protocollo COPP (Certified Output Protection Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



