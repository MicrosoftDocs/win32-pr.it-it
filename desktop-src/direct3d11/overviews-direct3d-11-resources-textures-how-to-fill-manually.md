---
title: Come inizializzare una trama a livello di codice
description: Questo argomento include diversi esempi che illustrano come inizializzare trame create con diversi tipi di utilizzo.
ms.assetid: 65e8ae82-50aa-4303-853e-3457da18f44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5584885b885f6026ee32a3e4c52a24aad78c3c08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856425"
---
# <a name="how-to-initialize-a-texture-programmatically"></a>Procedura: inizializzare una trama a livello di codice

È possibile inizializzare una trama durante la creazione dell'oggetto oppure è possibile compilare l'oggetto a livello di codice dopo che è stato creato. Questo argomento include diversi esempi che illustrano come inizializzare trame create con diversi tipi di utilizzo. Questo esempio presuppone che si sappia già come [creare una trama](overviews-direct3d-11-resources-textures-create.md).

-   [Utilizzo predefinito](#default-usage)
-   [Utilizzo dinamico](#dynamic-usage)
-   [Utilizzo di gestione temporanea](#staging-usage)
-   [Argomenti correlati](#related-topics)

## <a name="default-usage"></a>Utilizzo predefinito

Il tipo di utilizzo più comune è l'utilizzo predefinito. Per riempire una trama predefinita (una creata con **l' \_ \_ impostazione predefinita di utilizzo di d3d11**), è possibile eseguire una delle operazioni seguenti:

-   Chiamare [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) e inizializzare *pInitialData* per puntare ai dati forniti da un'applicazione.

    oppure

-   Dopo la chiamata a [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d), usare [**sul ID3D11DeviceContext:: UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) per riempire la trama predefinita con i dati di un puntatore fornito dall'applicazione.

## <a name="dynamic-usage"></a>Utilizzo dinamico

Per riempire una trama dinamica (uno creato con **\_ \_ Dynamic Usage d3d11**):

1.  Ottenere un puntatore alla memoria della trama passando il **d3d11 di \_ scrittura della mappa di \_ \_** durante la chiamata a [**sul ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).
2.  Scrivere i dati nella memoria.
3.  Chiamare [**sul ID3D11DeviceContext:: annullare**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) al termine della scrittura dei dati.

## <a name="staging-usage"></a>Utilizzo di gestione temporanea

Per riempire una trama di gestione temporanea (uno creato con **\_ \_ gestione temporanea dell'utilizzo di d3d11**):

1.  Ottenere un puntatore alla memoria della trama passando la **scrittura della \_ mappa \_ d3d11** quando si chiama [**sul ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).
2.  Scrivere i dati nella memoria.
3.  Chiamare [**sul ID3D11DeviceContext:: annullare**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) al termine della scrittura dei dati.

Una trama di staging può quindi essere usata come parametro di origine per [**sul ID3D11DeviceContext:: CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) o [**sul ID3D11DeviceContext:: CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) per riempire una risorsa predefinita o dinamica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Trame](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




