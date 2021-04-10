---
title: Debug del codice
description: Debug del codice
ms.assetid: 315bc692-86bc-481e-abe4-f35309807a58
keywords:
- Interfacce di Media Player Windows, debug del codice
- interfacce, debug del codice
- debug del codice per le interfacce
- Interfacce di Media Player Windows, registrazione
- interfacce, registrazione
- funzionalità di registrazione nelle interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77e2305020b945d90adc1a47387ab2a13a3536e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332031"
---
# <a name="debugging-code"></a>Debug del codice

Spesso si desidera vedere cosa accade all'interno dell'interfaccia. Questa operazione può essere eseguita tramite un controllo di testo o tramite un file di log.

È possibile creare un elemento di **testo** e posizionarlo temporaneamente su una parte dell'interfaccia. Ad esempio, è possibile usare il codice seguente per creare l'elemento di **testo** :


```C++
<!-- debugging control -- remove later -->        
<TEXT
    id = "debug"
    foregroundColor = "white"
    backgroundColor = "black"
    value = "debug"
    top = "100"
    left = "50"
    height = "15"
    width = "100" 
    z-order = "5" />
<!-- end debugging control -->
```



Se, ad esempio, si desidera visualizzare la posizione corrente del contenuto multimediale digitale in Windows Media Player, è possibile utilizzare codice simile al seguente per visualizzare la posizione corrente nella casella di testo.


```C++
<PLAYER
    id = "myplayer">
    <CONTROLS
        id = "mycontrols"
        currentPosition_onchange="value=player.controls.currentPosition"/>
</PLAYER>

```



## <a name="to-write-debugging-information-to-a-log-file"></a>Per scrivere le informazioni di debug in un file di log

Per abilitare o disabilitare il debug, modificare il valore della seguente chiave del registro di sistema:

**HKEY \_ \_ software utente \\ corrente \\ Microsoft \\ MediaPlayer \\ Preferences \\ ScriptDebugging**

Quando si imposta il valore su 1, la registrazione è abilitata. Quando si imposta il valore su 0 (impostazione predefinita), la registrazione è disabilitata.

Se la registrazione è abilitata, un file verrà inserito nel computer dell'utente nella stessa cartella dell'interfaccia. Il file verrà denominato "*filename* \_ 0 \_log.txt", dove *filename* è il nome del file di interfaccia. Il codice nell'interfaccia può scrivere testo in questo file usando il *tema*. metodo **logString** . Questo può essere utile se si desidera determinare cosa accade all'interno del codice mentre è in esecuzione. Si noti che il file di testo è codificato con caratteri Unicode.

Quando la registrazione è abilitata ed è stato installato un sistema di sviluppo che fornisce funzionalità di debug (ad esempio Microsoft Visual Studio), le eccezioni non gestite dal codice di script comporteranno l'apertura di una finestra di dialogo di avviso del debugger per ogni eccezione. Si tratta di una funzionalità utile che consente di eseguire il debug del codice di script. Inoltre, è possibile alleghi manualmente il processo di Media Player Windows al debugger quando è abilitata la registrazione.

Questo SDK include un'interfaccia di esempio, denominata "registrazione", che illustra la funzionalità di registrazione nelle interfacce. Per ulteriori informazioni sull'utilizzo degli esempi, vedere [esempi](samples.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sulle interfacce**](about-skins.md)
</dt> </dl>

 

 




