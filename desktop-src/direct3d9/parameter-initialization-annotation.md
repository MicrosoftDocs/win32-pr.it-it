---
description: Usare questa annotazione per definire il contenuto di un file esterno come valore di inizializzazione per un parametro di effetto.
ms.assetid: 3da1f951-cb8b-49ce-aba2-0badb3178093
title: Annotazione inizializzazione parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c564b5b5e273b320fdc5de6148ef5ba5dd9f1b78
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225334"
---
# <a name="parameter-initialization-annotation"></a>Annotazione inizializzazione parametri

Usare questa annotazione per definire il contenuto di un file esterno come valore di inizializzazione per un parametro di effetto. Ad esempio:


```
string SasResourceAddress = "Value";
```



dove value è una stringa di testo ASCII che può contenere un percorso assoluto o relativo. Un percorso relativo è relativo alla directory che contiene il file di effetti.

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

[Informazioni di riferimento sulla semantica e le annotazioni standard DirectX](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



