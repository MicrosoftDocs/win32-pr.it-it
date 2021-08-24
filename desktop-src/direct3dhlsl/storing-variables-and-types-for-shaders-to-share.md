---
title: Archiviazione di variabili e tipi per gli shader da condividere
description: L'oggetto di collegamento della classe è uno spazio dei nomi per variabili e tipi che possono essere condivisi da più shader.
ms.assetid: 8b61677b-a466-4646-b0b2-19097669f8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d40526274ea52d68b0a02dbefd02c116ded77d64e8b343a48abef2735446d971
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853171"
---
# <a name="storing-variables-and-types-for-shaders-to-share"></a>Archiviazione di variabili e tipi per gli shader da condividere

L'oggetto di collegamento della classe è uno spazio dei nomi per variabili e tipi che possono essere condivisi da più shader. Quando si passa un oggetto di collegamento di classe in una chiamata per creare uno shader, il runtime raccoglie un elenco di variabili e tipi che possono implementare ogni interfaccia nello shader e archivia i nomi di tali variabili e tipi nell'oggetto di collegamento della classe.

Pertanto, quando si chiama il metodo [**ID3D11ClassLinkage::GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance) per generare istanze di classe dall'oggetto di collegamento della classe, il runtime può recuperare la variabile o il tipo corrispondente al nome fornito in ogni shader (se tale nome è valido per un determinato shader) e che viene creato con l'oggetto collegamento di classe specificato.

Si supponga, ad esempio, di avere una classe **Light** che implementa un'interfaccia **Color** e di usare questa classe nel vertex shader e nel pixel shader. Quando si crea uno shader(ad esempio, chiamando [**ID3D11Device::CreatePixelShader),**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader)il runtime determina che il tipo di classe **Light** è disponibile sia nei vertex shader che nei pixel shader e aggiunge il tipo di classe **Light** all'oggetto collegamento della classe. È quindi possibile creare un'istanza **light** in una posizione desiderata, associare le risorse per entrambi gli shader e passare questa istanza nella matrice delle istanze della classe quando si imposta lo shader sul dispositivo , ad esempio chiamando [**ID3D11DeviceContext::P SSetShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader). Il runtime esegue quindi la sequenza seguente:

1.  Verifica che l'istanza sia stata creata con lo stesso oggetto collegamento di classe.
2.  Verifica che il **tipo di** classe Light sia availabe sia nei vertex shader che nei pixel shader.
3.  Seleziona le tabelle delle funzioni corrette, che possono essere diverse per i vertici e i pixel shader.
4.  Invia gli offset forniti dall'istanza di .

L'oggetto di collegamento della classe è in definitiva un repository di nomi di tipo e variabili. Il numero massimo di nomi disponibili per ogni elemento (tipo e variabile) è 64.000. Più sono lunghi i nomi dei tipi e delle variabili, maggiore è il requisito di archiviazione per i metadati dell'interfaccia archiviati per shader. Questo perché il runtime deve archiviare un mapping per questi nomi per ogni shader.

## <a name="related-topics"></a>Argomenti correlati

[Collegamento dinamico](overviews-direct3d-11-hlsl-dynamic-linking.md)


## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Collegamento dinamico](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 