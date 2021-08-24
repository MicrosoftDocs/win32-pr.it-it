---
title: Sezione del rettangolo di esempio
description: Sezione del rettangolo di esempio
ms.assetid: 44ed3257-2e1a-4b8d-9d55-a13b0400422d
keywords:
- Windows Media Player Skin per dispositivi mobili, controlli di selezione
- skins, marquees
- informazioni di riferimento su skin, marquees
- marquees in skins,sezione Marquee
- file di definizione dell'interfaccia, sezione Marquee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f8a3e013bb3a09a06f03715f0e7c4914e8e8d344c55843a643d5b8a9bf0479
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508121"
---
# <a name="sample-marquee-section"></a>Sezione del rettangolo di esempio

Le righe seguenti mostrano una tipica sezione Marquee di un file di definizione dell'interfaccia:


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>

//  ----------   ------       -------      ------------------------

    3,2,234,20   Tahoma,12,N  255,0,0    Title+Author, Title, Author


```



In questo modo viene definita una casella di visualizzazione del riquadro di selezione che mostra il titolo e l'autore se sono definiti entrambi, il titolo se è definito solo Title o il nome dell'autore se è definito solo Author. Se nessuno dei due elementi è definito, non verrà visualizzato nulla.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Testo scorrevole**](marquee.md)
</dt> </dl>

 

 




