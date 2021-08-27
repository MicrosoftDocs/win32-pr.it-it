---
title: Come inizializzare una trama a livello di codice
description: In questo argomento sono disponibili diversi esempi che illustrano come inizializzare trame create con diversi tipi di utilizzo.
ms.assetid: 65e8ae82-50aa-4303-853e-3457da18f44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b7d34e7e85fd647a6f45c93d61b3330825261f59d87b9c13a95547e742e365
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530563"
---
# <a name="how-to-initialize-a-texture-programmatically"></a>Procedura: Inizializzare una trama a livello di codice

È possibile inizializzare una trama durante la creazione dell'oggetto oppure riempire l'oggetto a livello di codice dopo la creazione. In questo argomento sono disponibili diversi esempi che illustrano come inizializzare trame create con diversi tipi di utilizzo. Questo esempio presuppone che si sappia già come creare [una trama.](overviews-direct3d-11-resources-textures-create.md)

-   [Utilizzo predefinito](#default-usage)
-   [Utilizzo dinamico](#dynamic-usage)
-   [Utilizzo della gestione temporanea](#staging-usage)
-   [Argomenti correlati](#related-topics)

## <a name="default-usage"></a>Utilizzo predefinito

Il tipo di utilizzo più comune è l'utilizzo predefinito. Per riempire una trama predefinita (creata con **D3D11 \_ USAGE \_ DEFAULT),** è possibile:

-   Chiamare [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) e *inizializzare pInitialData* in modo che punti ai dati forniti da un'applicazione.

    oppure

-   Dopo aver chiamato [**ID3D11Device::CreateTexture2D,**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d)usare [**ID3D11DeviceContext::UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) per riempire la trama predefinita con i dati di un puntatore fornito dall'applicazione.

## <a name="dynamic-usage"></a>Utilizzo dinamico

Per riempire una trama dinamica (creata con **D3D11 \_ USAGE \_ DYNAMIC):**

1.  Ottenere un puntatore alla memoria della trama passando **D3D11 \_ MAP \_ WRITE \_ DISCARD** quando si [**chiama ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).
2.  Scrivere dati nella memoria.
3.  Chiamare [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) al termine della scrittura dei dati.

## <a name="staging-usage"></a>Utilizzo della gestione temporanea

Per riempire una trama di staging (creata con **D3D11 \_ USAGE \_ STAGING):**

1.  Ottenere un puntatore alla memoria della trama passando **D3D11 \_ MAP \_ WRITE** quando si [**chiama ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).
2.  Scrivere dati nella memoria.
3.  Chiamare [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) al termine della scrittura dei dati.

Una trama di staging può quindi essere usata come parametro di origine per [**ID3D11DeviceContext::CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) o [**ID3D11DeviceContext::CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) per riempire una risorsa predefinita o dinamica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Trame](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




