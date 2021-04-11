---
description: D3DX è una raccolta di strumenti progettati per fornire funzionalità grafiche aggiuntive oltre a Direct3D. D3DX viene fornito come libreria a collegamento dinamico (DLL).
ms.assetid: d7b8c6ba-5c4f-494c-a24f-3b81a176725f
title: D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c54899b47936d309502a591fed6fdd81ea90fe3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342211"
---
# <a name="d3dx-direct3d-9"></a>D3DX (Direct3D 9)

D3DX è una raccolta di strumenti progettati per fornire funzionalità grafiche aggiuntive oltre a Direct3D. D3DX viene fornito come libreria a collegamento dinamico (DLL).

In questa versione di DirectX SDK è disponibile una sola versione di D3DX. La DLL D3DX per la vendita al dettaglio è inclusa nel pacchetto ridistribuibile fornito nell'SDK e viene installata automaticamente come parte dell' [installazione di DirectX con DirectSetup](https://msdn.microsoft.com/library/ee418267(VS.85).aspx). La libreria D3DX inclusa in questa versione dipende dai runtime Direct3D forniti con questo SDK. Le applicazioni che si collegano alla versione di D3DX in questa versione devono anche ridistribuire il runtime da questo SDK.

Più versioni di D3DX possono risiedere in modo indipendente in un singolo sistema simultaneamente. Collegando in modo statico un'applicazione a D3dx9. lib, l'applicazione si collega dinamicamente alla DLL D3DX Retail corrispondente in fase di esecuzione. Questa DLL corrisponde alle intestazioni D3DX in base a cui viene compilata l'applicazione (denominata con la \_ \_ costante della versione SDK di D3DX in D3dx9core. h). Poiché le nuove versioni di D3DX vengono fornite nelle versioni future di DirectX SDK, le applicazioni che si collegano a librerie D3DX precedenti non saranno interessate.

La libreria D3DX risolve le seguenti aree generali di funzionalità:

-   [Supporto per disegno linee in D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md)
-   [Supporto mesh in D3DX (Direct3D 9)](mesh-support-in-d3dx.md)
-   [Supporto della funzione Math in D3DX (Direct3D 9)](math-function-support-in-d3dx.md)
-   [Supporto della trama in D3DX (Direct3D 9)](texture-support-in-d3dx.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Per iniziare](getting-started.md)
</dt> </dl>

 

 



