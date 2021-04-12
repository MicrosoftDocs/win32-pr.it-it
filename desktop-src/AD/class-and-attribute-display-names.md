---
title: Nomi visualizzati della classe e dell'attributo
description: Questo argomento contiene informazioni sulle linee guida e per i nomi visualizzati delle classi e degli attributi.
ms.assetid: c85905b2-ed8b-4032-8c54-fd4de8b34ecf
ms.tgt_platform: multiple
keywords:
- Visualizza gli identificatori di Active Directory, della classe e dell'attributo
- Nome visualizzazione classe AD
- nome visualizzato attributo AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d65cd6ac6fc3077ff0d2bba15ffa9904b147654
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472670"
---
# <a name="class-and-attribute-display-names"></a>Nomi visualizzati della classe e dell'attributo

L'identificatore di visualizzazione per una classe di oggetti contiene gli attributi seguenti che possono essere usati per specificare i nomi visualizzati localizzati usati nell'interfaccia utente per gli oggetti di tale classe:

-   L'attributo **classDisplayName** è una stringa Unicode a valore singolo che specifica il nome visualizzato della classe.
-   L'attributo **nell'attributeDisplayNames** è una proprietà multivalore che specifica i nomi da utilizzare nell'interfaccia utente per gli attributi della classe di oggetti.

I valori **nell'attributeDisplayNames** sono stringhe Unicode; ogni elemento è costituito da una coppia di nomi delimitati da virgole:


```C++
<attribute name>,<display text>
```



In questo esempio " &lt; nome attributo &gt; " è l' **ldapDisplayName** dell'attributo e " &lt; testo visualizzato &gt; " è il testo da visualizzare come nome dell'attributo nell'interfaccia utente.

## <a name="guidelines-for-class-and-attribute-display-names"></a>Linee guida per i nomi visualizzati delle classi e degli attributi

Poiché molti fornitori possono estendere le classi con nuovi attributi o creare classi completamente nuove, è importante che i nomi visualizzati della classe e dell'attributo non siano ambigui e non comportino conflitti.

Ogni fornitore deve anteporre al nome visualizzato della classe un identificatore descrittivo univoco in base al nome del fornitore. Se, ad esempio, la società fittizia Fabrikam Inc. crea una nuova classe derivata dalla classe "Contact", può avere un nome visualizzato di classe univoco "contatto Fabrikam".

Se un fornitore estende una classe esistente con nuovi attributi, deve identificare in modo univoco il nome visualizzato dell'attributo in modo che non si verifichino conflitti con altri nomi visualizzati dell'attributo. Anche in questo caso, il prefisso del nome visualizzato dell'attributo con identificatore descrittivo univoco in base al nome del fornitore è una procedura consigliata. Se, ad esempio, l'azienda Fabrikam estende la classe utente con un nuovo attributo HR, può visualizzare in modo univoco l'attributo "informazioni su Fabrikam HR".

Inoltre, dal punto di vista della localizzazione, ogni fornitore deve localizzare i nomi visualizzati della classe e dell'attributo in ogni lingua supportata da Windows 2000.

## <a name="adding-a-value-to-the-attributedisplaynames-attribute"></a>Aggiunta di un valore all'attributo nell'attributeDisplayNames

**Per aggiungere un valore di mapping dei nomi all'attributo **nell'attributeDisplayNames****

1.  Determinare se esiste il valore del mapping dei nomi per l'attributo. Se è necessario sostituire un valore di mapping dei nomi, eliminare innanzitutto il valore esistente, usando il metodo [**IADs::P UTEX**](/windows/desktop/api/iads/nf-iads-iads-putex) , con il parametro *LnControlCode* impostato su **Ads \_ proprietà \_ Delete** e il parametro *vProp* impostato sul valore da rimuovere. Non usare la **\_ Proprietà Ads \_ Clear** o **l' \_ \_ aggiornamento della proprietà ADS** per *lnControlCode*.
2.  Creare la stringa che rappresenta il nome visualizzato dell'attributo. Per un esempio, vedere il formato riportato sopra.
3.  Usare il metodo [**IADs::P UTEX**](/windows/desktop/api/iads/nf-iads-iads-putex) con il parametro *LnControlCode* impostato su **Ads \_ Property \_ Append** per aggiungere il nuovo valore.
4.  Chiamare [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) per eseguire il commit delle modifiche nella directory.

Per ulteriori informazioni sulla denominazione di nuove classi e attributi, vedere [Naming Attributes and classes](naming-attributes-and-classes.md).

 

 