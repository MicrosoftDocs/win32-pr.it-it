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
# <a name="obtaining-the-drivers-certificate-chain"></a>Acquisizione della catena di certificati dei driver

Per usare Certified Output Protocol (COPP), l'applicazione deve prima di tutto compilare un grafo DirectShow che includa il filtro di rendering video mixing (VMR-7 o VMR-9). Il filtro renderer video precedente non supporta COPP. Prima di chiamare i metodi COPP, l'applicazione deve compilare un grafico di riproduzione video e connettere il decodificatore al pin di input del filtro VMR. Non è necessario riprodurre il file video.

Dopo aver compilato il grafo, eseguire una query su VMR per l'interfaccia [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) e quindi chiamare [**IAMCertifiedOutputProtection:: backexchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange). Questo metodo restituisce un numero casuale a 128 bit tipizzato come GUID, insieme a un puntatore a una matrice di byte che contiene la catena di certificati XML del driver in formato UTF-8. Il codice seguente illustra come ottenere la catena di certificati.


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

[Uso di COPP (Certified Output Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



