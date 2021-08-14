---
title: Two-Pass codifica
description: Two-Pass codifica
ms.assetid: 354cd0a5-9a64-4171-9604-694e60b382ad
keywords:
- Windows Media Format SDK, codifica a due passi
- Windows Media Format SDK, codifica a 2 passi
- codec, codifica a due passi
- codec, codifica a 2 passi
- codifica a due passi, informazioni
- codifica a 2 passi, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6cd769049b5fa3869c844e00d9ee14cfae596b197d06d414b04a544d831bbeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845339"
---
# <a name="two-pass-encoding"></a>Two-Pass codifica

La codifica a due passi è un metodo di codifica disponibile con alcuni codec, ad esempio Windows codec Media Video 9. Quando si usa la codifica a due passi, il codec elabora due volte tutti gli esempi per il flusso. Al primo passaggio, il codec raccoglie informazioni sul contenuto del flusso. Al secondo passaggio, il codec usa le informazioni raccolte al primo passaggio per ottimizzare il processo di codifica per il flusso.

Nella modalità di codifica Velocità in bit costante i file codificati in due passaggi sono in genere più efficienti dei file codificati in un unico passaggio. VbR basato sulla qualità, ovvero un passaggio, produce una qualità più coerente rispetto alla vbr basata sulla velocità in bit, ovvero a due passi.

Non è possibile usare la codifica a due passi nei flussi live.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità codec**](codec-features.md)
</dt> <dt>

[**Uso Two-Pass codifica**](using-two-pass-encoding.md)
</dt> </dl>

 

 




