---
description: D3DX è una libreria di strumenti progettati per fornire funzionalità grafiche aggiuntive su Direct3D. D3DX viene fornito come libreria a collegamento dinamico (DLL).
ms.assetid: d7b8c6ba-5c4f-494c-a24f-3b81a176725f
title: D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a2164349b761cd7ff2ccca5e2158abc22bd64
ms.sourcegitcommit: 78ce1d1e3f12ee3e08390868e5b93c034f437657
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111910243"
---
# <a name="d3dx-direct3d-9"></a>D3DX (Direct3D 9)

> [!NOTE]
> La libreria D3DX è deprecata. Se l'aggiornamento a una versione più recente di Direct3D e al codice di utilità associato non è un'opzione, è possibile usare il pacchetto NuGet [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) invece di basarsi su DirectX SDK o DirectSetup legacy.

D3DX è una libreria di strumenti progettati per fornire funzionalità grafiche aggiuntive su Direct3D. D3DX viene fornito come libreria a collegamento dinamico (DLL).

In questa versione di DirectX SDK è disponibile una sola versione di D3DX. La DLL D3DX definitiva è inclusa nel file ridistribuibile fornito nell'SDK e viene installata automaticamente come parte dell'installazione di **DirectX con DirectSetup.** La libreria D3DX inclusa in questa versione dipende dai runtime Direct3D forniti con questo SDK. Anche le applicazioni che si collegano alla versione di D3DX in questa versione devono ridistribuire il runtime da questo SDK.

Più versioni di D3DX possono risiedere in modo indipendente in un singolo sistema contemporaneamente. Collegando in modo statico un'applicazione a D3dx9.lib, l'applicazione si collega in modo dinamico alla DLL D3DX finale corrispondente in fase di esecuzione. Questa DLL corrisponde alle intestazioni D3DX con cui viene compilata l'applicazione (denominata con la costante VERSION di D3DX \_ SDK \_ in D3dx9core.h). Poiché le nuove versioni di D3DX verranno rilasciate nelle versioni future di DirectX SDK, le applicazioni che si collegano alle librerie D3DX precedenti rimarranno invariate.

La libreria D3DX risolve queste aree generali di funzionalità:

-   [Supporto per il disegno di linee in D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md)
-   [Supporto mesh in D3DX (Direct3D 9)](mesh-support-in-d3dx.md)
-   [Supporto delle funzioni matematiche in D3DX (Direct3D 9)](math-function-support-in-d3dx.md)
-   [Supporto delle trame in D3DX (Direct3D 9)](texture-support-in-d3dx.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Per iniziare](getting-started.md)
</dt> </dl>

 

 



