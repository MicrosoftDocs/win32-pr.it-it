---
description: Come implementare IUnknown
ms.assetid: 4e363ccb-9725-4be6-bb31-283bf1d658f5
title: Come implementare IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27c12e25d56adab1841a375ac6c1ce0857a73b5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520498"
---
# <a name="how-to-implement-iunknown"></a>Come implementare IUnknown

Microsoft DirectShow si basa sul Component Object Model (COM). Se si scrive un filtro personalizzato, è necessario implementarlo come oggetto COM. Le classi base di DirectShow forniscono un Framework dal quale eseguire questa operazione. L'uso delle classi base non è obbligatorio, ma può semplificare il processo di sviluppo. Questo articolo descrive alcuni dei dettagli interni degli oggetti COM e la relativa implementazione nelle classi base di DirectShow.

In questo articolo si presuppone che l'utente sia in grado di programmare le applicazioni client COM, in altre parole, di comprendere i metodi in **IUnknown**, ma non presuppone alcuna esperienza precedente nello sviluppo di oggetti com. DirectShow gestisce molti dei dettagli sullo sviluppo di un oggetto COM. Se si ha esperienza nello sviluppo di oggetti COM, è consigliabile leggere la sezione [uso di CUnknown](using-cunknown.md), che descrive la classe di base [**CUnknown**](cunknown.md) .

COM è una specifica, non un'implementazione. Definisce le regole che un componente deve seguire. l'inserimento di tali regole viene applicato allo sviluppatore. In DirectShow tutti gli oggetti derivano da un set di classi base C++. I costruttori e i metodi della classe base eseguono la maggior parte delle operazioni di "contabilità" COM, ad esempio mantenendo un conteggio dei riferimenti coerente. Derivando il filtro da una classe di base, si eredita la funzionalità della classe. Per utilizzare in modo efficace le classi di base, è necessario conoscere in modo generale il modo in cui implementano la specifica COM.

Questo articolo contiene gli argomenti seguenti.

-   [Funzionamento di IUnknown](how-iunknown-works.md)
-   [Uso di CUnknown](using-cunknown.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow e COM](directshow-and-com.md)
</dt> </dl>

 

 



