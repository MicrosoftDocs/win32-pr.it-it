---
title: Icone della classe
description: L'icona utilizzata per rappresentare un oggetto classe può essere specificata nell'attributo iconPath nel contenitore DisplaySpecifiers.
ms.assetid: 0ff8da8a-d3d3-4a15-8103-4fe6ec307427
ms.tgt_platform: multiple
keywords:
- Nome visualizzazione classe AD, icone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691d4ef22babeded12ec9b951f92247df99521b6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956344"
---
# <a name="class-icons"></a>Icone della classe

L'icona utilizzata per rappresentare un oggetto classe può essere specificata nell'attributo **iconPath** nel contenitore DisplaySpecifiers. Ogni classe può inoltre archiviare più Stati dell'icona. Ad esempio, una classe di cartelle può avere icone per gli stati aperti, chiusi e disabilitati. L'implementazione corrente accetta un massimo di sedici diversi Stati di icona per classe.

L'attributo **iconPath** può essere specificato in uno dei due modi seguenti.


```C++
<state>,<icon file name>
```



oppure


```C++
<state>,<module file name>,<resource ID>
```



In questi esempi lo " &lt; stato &gt; " è un numero intero con un valore compreso tra 0 e 15. Il valore 0 viene definito come lo stato predefinito o chiuso dell'icona. Il valore 1 viene definito come lo stato aperto dell'icona. Il valore 2 è lo stato disabilitato. Tutti gli altri valori sono definiti dall'applicazione.

Il nome del file &lt; icona &gt; è il percorso e il nome del file di icona che contiene l'immagine dell'icona.

Il &lt; nome del file &gt; di modulo è il percorso e il nome file di un modulo, ad esempio un file exe o dll, che contiene l'immagine dell'icona in una risorsa. " &lt; ID risorsa &gt; " è un numero intero che specifica l'identificatore della risorsa icona all'interno del modulo.

## <a name="adding-a-value-to-the-iconpath-attribute"></a>Aggiunta di un valore all'attributo **iconPath**

Per aggiungere un valore all'attributo **iconPath** , seguire questa procedura.

1.  Determinare se il valore dell'attributo esiste. Se è necessario sostituire un valore, eliminare innanzitutto il valore esistente usando il metodo [**IADs::P UTEX**](/windows/desktop/api/iads/nf-iads-iads-putex) con il parametro *LnControlCode* impostato su **Ads \_ proprietà \_ Delete** e il parametro *vProp* impostato sul valore da rimuovere. Non usare la **\_ Proprietà Ads \_ Clear** o **l' \_ \_ aggiornamento della proprietà ADS** per *lnControlCode*.
2.  Creare la stringa che rappresenta i dati dell'icona dell'attributo. Per un esempio, vedere il formato riportato sopra.
3.  Per aggiungere il nuovo valore, usare il metodo [**IADs::P UTEX**](/windows/desktop/api/iads/nf-iads-iads-putex) con il parametro *LnControlCode* impostato su **Ads \_ Property \_ Append**.
4.  Per eseguire il commit delle modifiche nella directory, chiamare [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).

 

 