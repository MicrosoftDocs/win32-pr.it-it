---
title: Nomi visualizzati di classi e attributi
description: Questo argomento contiene informazioni su e linee guida per i nomi visualizzati di classi e attributi.
ms.assetid: c85905b2-ed8b-4032-8c54-fd4de8b34ecf
ms.tgt_platform: multiple
keywords:
- identificatori di visualizzazione AD, nomi visualizzati di classi e attributi
- nomi visualizzati della classe AD
- nomi visualizzati degli attributi AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213132acfa6463b1c1e8a7615f5d7f488e53edfcdf9b75f8df5759fcd0e4d398
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022592"
---
# <a name="class-and-attribute-display-names"></a>Nomi visualizzati di classi e attributi

L'identificatore di visualizzazione per una classe di oggetti contiene gli attributi seguenti che possono essere usati per specificare i nomi visualizzati localizzati usati nell'interfaccia utente per gli oggetti di tale classe:

-   **L'attributo classDisplayName** è una stringa Unicode a valore singolo che specifica il nome visualizzato della classe.
-   **L'attributo attributeDisplayNames** è una proprietà multivalore che specifica i nomi da usare nell'interfaccia utente per gli attributi della classe di oggetti.

I **valori attributeDisplayNames** sono stringhe Unicode. ogni elemento è costituito da una coppia di nomi delimitata da virgole:


```C++
<attribute name>,<display text>
```



In questo esempio " attribute name " è &lt; &gt; **lDAPDisplayName** dell'attributo e " display text " è il testo da visualizzare come nome dell'attributo &lt; nell'interfaccia &gt; utente.

## <a name="guidelines-for-class-and-attribute-display-names"></a>Linee guida per i nomi visualizzati di classi e attributi

Poiché molti fornitori possono estendere le classi con nuovi attributi o creare classi completamente nuove, è importante che i nomi visualizzati delle classi e degli attributi non siano ambigui e non creino conflitti.

Ogni fornitore deve antescire al nome visualizzato della classe un identificatore descrittivo univoco in base al nome del fornitore. Ad esempio, se la società fittizia Fabrikam Inc., crea una nuova classe derivata dalla classe "contact", può avere un nome visualizzato univoco della classe "Fabrikam Contact".

Se un fornitore estende una classe esistente con nuovi attributi, deve identificare nuovamente in modo univoco il nome visualizzato dell'attributo in modo che non si verifichino conflitti con altri nomi visualizzati degli attributi. Anche in questo caso, è consigliabile fare in modo che il nome visualizzato dell'attributo sia preceduto da un identificatore descrittivo univoco in base al nome del fornitore. Ad esempio, se la società Fabrikam estende la classe utente con un nuovo attributo HR, potrebbe visualizzare in modo univoco l'attributo come "Fabrikam HR Information".

Inoltre, dal punto di vista della localizzazione, ogni fornitore deve localizzare i nomi visualizzati della classe e dell'attributo in ogni lingua supportata da Windows 2000.

## <a name="adding-a-value-to-the-attributedisplaynames-attribute"></a>Aggiunta di un valore all'attributo attributeDisplayNames

**Per aggiungere un valore di mapping dei nomi **all'attributo attributeDisplayNames****

1.  Determinare se il valore di mapping dei nomi per l'attributo esiste. Se è necessario sostituire un valore di mapping dei nomi, eliminare prima il valore esistente usando il metodo [**IADs::P utEx,**](/windows/desktop/api/iads/nf-iads-iads-putex) con il parametro *lnControlCode* impostato su **ADS \_ PROPERTY \_ DELETE** e il parametro *vProp* impostato sul valore da rimuovere. Non usare **ADS \_ PROPERTY CLEAR \_ o** **ADS PROPERTY \_ \_ UPDATE** per *lnControlCode*.
2.  Creare la stringa che rappresenta il nome visualizzato dell'attributo. Per un esempio, vedere il formato precedente.
3.  Usare il [**metodo IADs::P utEx**](/windows/desktop/api/iads/nf-iads-iads-putex) con il parametro *lnControlCode* impostato su **ADS \_ PROPERTY \_ APPEND** per aggiungere il nuovo valore.
4.  Chiamare [**IADs::SetInfo per**](/windows/desktop/api/iads/nf-iads-iads-setinfo) eseguire il commit delle modifiche nella directory.

Per altre informazioni sulla denominazione di nuove classi e attributi, vedere [Naming Attributes and Classes](naming-attributes-and-classes.md).

 

 