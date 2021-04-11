---
description: D3DX è una libreria di utilità che fornisce servizi di supporto. Si tratta di un livello sopra il componente Direct3D.
ms.assetid: a44d25de-f79d-4132-a75a-0c22ccd84341
title: Supporto della funzione Math in D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac69e0385919b015d1f8d3e7d47e221c06a04fbb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124476"
---
# <a name="math-function-support-in-d3dx-direct3d-9"></a>Supporto della funzione Math in D3DX (Direct3D 9)

D3DX è una libreria di utilità che fornisce servizi di supporto. Si tratta di un livello sopra il componente Direct3D.

## <a name="math"></a>Math

Il supporto matematico, contenuto in un set di funzioni, è disponibile per:

-   Calcoli colori
-   Aerei
-   Manipolazione della matrice
-   Quaternioni
-   vettori 2D
-   vettori 3D
-   vettori 4D

Si noti che, quando abbinato agli overload C++, il supporto per i tipi matematici 3D di base è esteso.

Per ulteriori informazioni su queste funzioni, vedere [D3DX Functions](dx9-graphics-reference-d3dx-functions.md). Per individuare la funzione di cui si ha bisogno, vengono suddivise in diverse cartelle.

## <a name="float16"></a>FLOAT16

Quando si usa il tipo di dati FLOAT16, assicurarsi di limitare i valori a un massimo di D3DX \_ 16F \_ max. Qualsiasi valore di FLOAT16 che supera questa operazione determinerà un comportamento indefinito nella pipeline. Vedere [altre costanti D3DX](other-d3dx-constants.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 



