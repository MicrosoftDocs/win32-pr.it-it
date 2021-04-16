---
title: Sezione Marquee di esempio
description: Sezione Marquee di esempio
ms.assetid: 44ed3257-2e1a-4b8d-9d55-a13b0400422d
keywords:
- Interfacce di Windows Media Player Mobile, Marquees
- interfacce, Marquee
- riferimento per Skin, Marquees
- Marquees in Skins, sezione Marquee
- file di definizione dell'interfaccia, sezione Marquee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f66588d81b22051a9289a80c8733d5cfe154bed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471603"
---
# <a name="sample-marquee-section"></a>Sezione Marquee di esempio

Le righe seguenti mostrano una sezione di selezione tipica di un file di definizione dell'interfaccia personalizzata:


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>

//  ----------   ------       -------      ------------------------

    3,2,234,20   Tahoma,12,N  255,0,0    Title+Author, Title, Author


```



Definisce una casella di visualizzazione Marquee che mostra il titolo e l'autore se sono definiti entrambi, il titolo se è stato definito solo il titolo o il nome dell'autore se è definito solo l'autore. Se non viene definito alcun elemento, non verrà visualizzato nulla.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Testo scorrevole**](marquee.md)
</dt> </dl>

 

 




