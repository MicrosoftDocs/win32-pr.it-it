---
title: Icone delle classi
description: L'icona usata per rappresentare un oggetto classe può essere specificata nell'attributo iconPath nel contenitore DisplaySpecifiers.
ms.assetid: 0ff8da8a-d3d3-4a15-8103-4fe6ec307427
ms.tgt_platform: multiple
keywords:
- nomi visualizzati della classe AD , icone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efe3548daa223cdfa05dee8ec3df8f2f8bc800c5ba7449920744de1a67ac8745
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022602"
---
# <a name="class-icons"></a>Icone delle classi

L'icona usata per rappresentare un oggetto classe può essere specificata **nell'attributo iconPath** nel contenitore DisplaySpecifiers. Ogni classe può inoltre archiviare più stati di icona. Ad esempio, una classe di cartelle può avere icone per gli stati aperto, chiuso e disabilitato. L'implementazione corrente accetta un massimo di sedici stati di icona diversi per ogni classe.

**L'attributo iconPath** può essere specificato in uno dei due modi seguenti.


```C++
<state>,<icon file name>
```



oppure


```C++
<state>,<module file name>,<resource ID>
```



In questi esempi, " state " è un numero intero con un valore compreso tra &lt; &gt; 0 e 15. Il valore 0 è definito come stato predefinito o chiuso dell'icona. Il valore 1 è definito come stato aperto dell'icona. Il valore 2 è lo stato disabilitato. Tutti gli altri valori sono definiti dall'applicazione.

Il " nome file icona " è il percorso e il nome file di un file di &lt; &gt; icona che contiene l'immagine dell'icona.

" module file name " è il percorso e il nome file di un modulo, ad esempio un FILE EXE o UNA DLL, che contiene l'immagine dell'icona &lt; &gt; in una risorsa. L' " &lt; ID risorsa " è un numero intero che specifica l'identificatore di risorsa della risorsa icona &gt; all'interno del modulo.

## <a name="adding-a-value-to-the-iconpath-attribute"></a>Aggiunta di un valore **all'attributo iconPath**

Per aggiungere un valore **all'attributo iconPath,** seguire questa procedura.

1.  Determinare se il valore dell'attributo esiste. Se un valore deve essere sostituito, eliminare prima il valore esistente usando il metodo [**IADs::P utEx**](/windows/desktop/api/iads/nf-iads-iads-putex) con il parametro *lnControlCode* impostato su **ADS \_ PROPERTY \_ DELETE** e il parametro *vProp* impostato sul valore da rimuovere. Non usare **ADS \_ PROPERTY CLEAR \_ o** **ADS PROPERTY \_ \_ UPDATE** per *lnControlCode*.
2.  Creare la stringa che rappresenta i dati dell'icona dell'attributo. Per un esempio, vedere il formato precedente.
3.  Per aggiungere il nuovo valore, usare il metodo [**IADs::P utEx**](/windows/desktop/api/iads/nf-iads-iads-putex) con il parametro *lnControlCode* impostato su **ADS \_ PROPERTY \_ APPEND**.
4.  Per eseguire il commit delle modifiche nella directory, [**chiamare IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).

 

 