---
description: Usare questa annotazione per definire il contenuto di un file esterno come valore di inizializzazione per un parametro dell'effetto.
ms.assetid: 3da1f951-cb8b-49ce-aba2-0badb3178093
title: Annotazione inizializzazione parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d66d0cc18782d97a5a56c73ab12cd9222d33827930d60023fccf73cd2a8455
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798662"
---
# <a name="parameter-initialization-annotation"></a>Annotazione inizializzazione parametri

Usare questa annotazione per definire il contenuto di un file esterno come valore di inizializzazione per un parametro dell'effetto. Esempio:


```
string SasResourceAddress = "Value";
```



dove Value è una stringa di testo ASCII che può contenere un percorso assoluto o relativo. Un percorso relativo è relativo alla directory che contiene il file dell'effetto.

Ecco un esempio:


```
texture2D DetailTexture
<
    string SasResourceAddress = "noise.dds";
>;
```



Il valore predefinito è una stringa vuota.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimenti semantici e annotazioni standard DirectX](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



