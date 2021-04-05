---
title: Sezione Marquee
description: Sezione Marquee
ms.assetid: ff48c922-e6fc-4ba2-89ad-dcb34be0fea5
keywords:
- Interfacce di Windows Media Player Mobile, Marquees
- interfacce, Marquee
- creazione di interfacce, sezione Marquee
- scrittura di codice per interfacce, sezione Marquee
- Marquees in Skins, sezione Marquee
- file di definizione dell'interfaccia, sezione Marquee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdf92a9f8ba3c1ca34559d355801d74ba6ed6382
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714518"
---
# <a name="marquee-section"></a>Sezione Marquee

La sezione Marquee contiene informazioni sulla casella di testo Marquee, che consente di visualizzare il testo di scorrimento:


```C++
[ Marquee ]

//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------
    100,150,100,20   Tahoma,12,N  255,0,0    Title+Author, Author, Title

```



Verrà visualizzato il titolo e l'autore dell'elemento multimediale corrente anche se è possibile visualizzare qualsiasi tipo di testo nella casella di selezione. È ad esempio possibile includere anche filename, status e playlist nel Marquee.

> [!Note]  
> Per mantenere la compatibilità con le versioni di Windows Media Player Mobile precedenti a Windows Media Player 10 Mobile, l'utilizzo di "Marquis" in un file di definizione dell'interfaccia personalizzata è ancora considerato valido.

 

Per ulteriori informazioni sulla sezione Marquee, vedere [Marquee](marquee.md) in the Skin Reference.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Scrittura del codice**](writing-the-code.md)
</dt> </dl>

 

 




