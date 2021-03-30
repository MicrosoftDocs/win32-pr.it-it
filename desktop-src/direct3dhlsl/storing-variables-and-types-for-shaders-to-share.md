---
title: Archiviazione di variabili e tipi per gli shader da condividere
description: L'oggetto collegamento di classe è uno spazio dei nomi per variabili e tipi che possono essere condivisi da più shader.
ms.assetid: 8b61677b-a466-4646-b0b2-19097669f8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f9423154cd42de28b2d447776fe21a7b8e57620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976823"
---
# <a name="storing-variables-and-types-for-shaders-to-share"></a>Archiviazione di variabili e tipi per gli shader da condividere

L'oggetto collegamento di classe è uno spazio dei nomi per variabili e tipi che possono essere condivisi da più shader. Quando si passa un oggetto collegamento di classe in una chiamata per creare uno shader, il runtime raccoglie un elenco di variabili e tipi che possono implementare ogni interfaccia nello shader e archivia i nomi di tali variabili e tipi nell'oggetto del collegamento alla classe.

Pertanto, quando si chiama il metodo [**ID3D11ClassLinkage:: GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance) per generare istanze di classe dall'oggetto del collegamento alla classe, il runtime può recuperare la variabile o il tipo che corrisponde al nome fornito in ogni shader (se tale nome è valido per un determinato shader) e che viene creato con l'oggetto del collegamento alla classe specificato.

Si supponga, ad esempio, di disporre di una classe **Light** che implementi un'interfaccia **colore** e di usare questa classe nel vertex shader e pixel shader. Quando si crea uno shader, ad esempio chiamando [**ID3D11Device:: CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader), il runtime determina che il tipo di classe **Light** è disponibile sia in vertex che in pixel shader e aggiunge il tipo di classe **Light** all'oggetto del collegamento alla classe. È quindi possibile creare un'istanza di **Light** in una posizione desiderata, associare le risorse per entrambi gli shader e passare questa istanza nella matrice di istanze della classe quando si imposta lo shader sul dispositivo (ad esempio, chiamando [**sul ID3D11DeviceContext::P ssetshader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader)). Il runtime esegue quindi la sequenza seguente:

1.  Verifica che l'istanza di sia stata creata con lo stesso oggetto di collegamento di classe.
2.  Verifica che il tipo di classe **Light** sia disponibili sia in vertex che in pixel shader.
3.  Seleziona le tabelle di funzioni corrette, che possono essere diverse per gli shader Vertex e pixel.
4.  Invia gli offset forniti dall'istanza di.

L'oggetto collegamento alla classe è in definitiva un repository di nomi di tipo e di variabile. Il numero massimo di nomi disponibili per ogni elemento (tipo e variabile) è 64K. Più è lungo il tipo e i nomi delle variabili, più elevato è il requisito di archiviazione per i metadati dell'interfaccia archiviati per shader. Questo perché il runtime deve archiviare un mapping per questi nomi per ogni shader.

## <a name="related-topics"></a>Argomenti correlati

[Collegamento dinamico](overviews-direct3d-11-hlsl-dynamic-linking.md)


## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Collegamento dinamico](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 