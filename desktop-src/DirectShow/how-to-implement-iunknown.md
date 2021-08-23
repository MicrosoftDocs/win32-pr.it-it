---
description: Come implementare IUnknown
ms.assetid: 4e363ccb-9725-4be6-bb31-283bf1d658f5
title: Come implementare IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f905ac7e31be955a7b24f8504fc6b52ca8031e4a7deef86ef8bccd537b5ca6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748701"
---
# <a name="how-to-implement-iunknown"></a>Come implementare IUnknown

Microsoft DirectShow è basato sul Component Object Model (COM). Se si scrive un filtro personalizzato, è necessario implementarlo come oggetto COM. Le DirectShow di base forniscono un framework da cui eseguire questa operazione. L'uso delle classi di base non è obbligatorio, ma può semplificare il processo di sviluppo. Questo articolo descrive alcuni dettagli interni degli oggetti COM e la relativa implementazione nelle classi DirectShow di base.

Questo articolo presuppone che si sappia programmare applicazioni client COM, ovvero che si comprendino i metodi in **IUnknown,** ma che non si presupponga alcuna esperienza precedente di sviluppo di oggetti COM. DirectShow gestisce molti dei dettagli dello sviluppo di un oggetto COM. Se si ha esperienza nello sviluppo di oggetti COM, leggere la sezione [Using CUnknown](using-cunknown.md)( Uso di CUnknown ), che descrive la classe di base [**CUnknown.**](cunknown.md)

COM è una specifica, non un'implementazione. Definisce le regole che un componente deve seguire; L'applicazione di queste regole viene lasciata allo sviluppatore. In DirectShow, tutti gli oggetti derivano da un set di classi di base C++. I costruttori e i metodi della classe di base esegano la maggior parte delle operazioni di "bookkeeping" COM, ad esempio mantenendo un conteggio dei riferimenti coerente. Derivando il filtro da una classe di base, si eredita la funzionalità della classe . Per usare in modo efficace le classi di base, è necessaria una conoscenza generale del modo in cui implementano la specifica COM.

Questo articolo contiene gli argomenti seguenti.

-   [Funzionamento di IUnknown](how-iunknown-works.md)
-   [Uso di CUnknown](using-cunknown.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow e COM](directshow-and-com.md)
</dt> </dl>

 

 



