---
title: '\_ \_ modificatori del registro di origine PS 1 4 per texld, texcrd'
description: Due istruzioni per l'indirizzo di trama di pixel shader versione 1 \_ 4, texld-PS \_ 1 \_ 4 e texcrd-PS, hanno una sintassi personalizzata.
ms.assetid: bbc8074f-882e-4b67-ae4d-1641ceb7f3ad
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: af2097ee682aec7da0ca36df9e4b465fb360f814
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/27/2019
ms.locfileid: "104117257"
---
# <a name="ps_1_4-source-register-modifiers-for-texld-texcrd"></a>\_ \_ modificatori del registro di origine PS 1 4 per texld, texcrd

Due istruzioni per l'indirizzo di trama di pixel shader versione 1 \_ 4, [texld-PS \_ 1 \_ 4](texld---ps-1-4.md) e [texcrd-PS](texcrd---ps.md), hanno una sintassi personalizzata. Queste istruzioni supportano il set di modificatori del registro di origine, i selettori del registro di origine e le maschere di scrittura del registro di destinazione, come illustrato di seguito.

## <a name="source-register-modifiers-for-texld-and-texcrd"></a>Modificatori del registro di origine per texld e texcrd

Questi modificatori forniscono una funzionalità di divisione proiezioni dividendo i valori x e y in base ai valori z o w.



| Modificatori del registro di origine | Descrizione                | Sintassi       |
|---------------------------|----------------------------|--------------|
| \_DZ                      | Dividere i componenti x, y per z | Registra \_ DZ |
| \_db                      | Dividere i componenti x, y per z | Registra \_ database |
| \_dw                      | Dividere i componenti x, y per w | Registra \_ DW |
| \_da                      | Dividere i componenti x, y per w | Registra \_ da |



 

### <a name="remarks"></a>Commenti

Il \_ \_ modificatore DZ o DB esegue le operazioni seguenti:


```
x' = x/z ( x' = 1.0 if z == 0)
y' = y/z ( y' = 1.0 if z == 0)
z' is undefined
w' is undefined
```



Il \_ \_ modificatore DW o da esegue le operazioni seguenti:


```
x' = x/w ( x' = 1.0 if w == 0)
y' = y/w ( y' = 1.0 if w == 0)
z' is undefined
w' is undefined
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modificatori del registro di origine pixel shader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




