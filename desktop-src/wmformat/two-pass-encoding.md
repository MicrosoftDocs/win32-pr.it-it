---
title: Codifica Two-Pass
description: Codifica Two-Pass
ms.assetid: 354cd0a5-9a64-4171-9604-694e60b382ad
keywords:
- Windows Media Format SDK, codifica a due passaggi
- Windows Media Format SDK, codifica a 2 passaggi
- codec, codifica a due passaggi
- codec, codifica a 2 passaggi
- codifica a due passaggi, informazioni
- codifica a 2 passaggi, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6764f80857447e122c97c69683243a65da7e83b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044474"
---
# <a name="two-pass-encoding"></a>Codifica Two-Pass

La codifica a due passaggi è un metodo di codifica disponibile con alcuni codec, ad esempio il codec Windows Media Video 9. Quando si usa la codifica a due passaggi, il codec elabora due volte tutti gli esempi per il flusso. Al primo passaggio, il codec raccoglie informazioni sul contenuto del flusso. Al secondo passaggio, il codec usa le informazioni raccolte al primo passaggio per ottimizzare il processo di codifica per il flusso.

Nella modalità di codifica della velocità in bit costante i file codificati in due passaggi sono in genere più efficienti rispetto ai file codificati in un singolo passaggio. Il VBR basato sulla qualità, che è un passaggio, produce una qualità più uniforme rispetto a quella basata sulla velocità in bit, ovvero due passaggi.

Non è possibile usare la codifica a due passaggi sui flussi live.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di codec**](codec-features.md)
</dt> <dt>

[**Uso della codifica Two-Pass**](using-two-pass-encoding.md)
</dt> </dl>

 

 




