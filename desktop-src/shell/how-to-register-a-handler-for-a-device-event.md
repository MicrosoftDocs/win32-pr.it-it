---
description: Descrive i processi per l'implementazione dei gestori di eventi del dispositivo nel registro di sistema.
ms.assetid: 84B12B5C-C179-4124-A1FC-B90D120336BF
title: Come registrare un gestore per un evento del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34ef15071b349afa3f863e7c57b64c280c2aef8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881562"
---
# <a name="how-to-register-a-handler-for-a-device-event"></a>Come registrare un gestore per un evento del dispositivo

I gestori definiscono la parte software di AutoPlay. Definiscono l'icona e il nome descrittivo del software, nonché il componente Component Object Model (COM) per creare un'istanza di e come inizializzare il componente in risposta a un evento. Ogni gestore per un evento specifico viene registrato come valore nella chiave **EventHandler** appropriata. Quando viene rilevato l'evento, all'utente viene richiesto di scegliere un gestore da un elenco di tutti i gestori registrati per tale evento.

## <a name="instructions"></a>Istruzioni


I gestori e i relativi valori associati sono definiti sotto la chiave dei \\ **gestori** AutoplayHandlers. Le sottochiavi variano a seconda che il sistema sia in grado di leggere direttamente il contenuto del dispositivo o se il dispositivo fornisce contenuto al sistema tramite un'interfaccia proprietaria.

Nell'esempio seguente vengono illustrate le sottochiavi e i valori utilizzati per un dispositivo, ad esempio una videocamera digitale o un lettore MP3, che fornisce il contenuto al sistema tramite un'interfaccia proprietaria. Il gestore di esempio è denominato **DataHandler**.

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     Handlers
                        MyHandler
                           Action [REG_SZ] = Play music
                           CLSID [REG_SZ] = {a51f2ed3-634e-4a97-9d55-efcf08e7b32f}
                           DefaultIcon [REG_EXPAND_SZ] = %ProgramFiles%\Windows Media Player\wmplayer.exe,0
                           InitCmdLine [REG_SZ] = /Play
                           ProgID [REG_SZ] = WMP.PlayMusicFiles
                           Provider [REG_SZ] = Windows Media Player
```

> [!Note]  
> Mentre l'esempio mostra sia un ProgID che un valore di identificatore di classe (CLSID), in pratica questi valori si escludono a vicenda, in modo che sia presente solo uno o l'altro. Il valore ProgID è preferibile. A seconda di quale viene usato, deve puntare a un componente COM che implementa l'interfaccia [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) .

 

È possibile immettere il valore dell'azione come valore letterale, ad esempio "Play Music", come illustrato in questo esempio, oppure come nome file con una stringa di risorsa. È anche possibile immettere il valore del provider come valore letterale o come nome file con una stringa di risorsa. AutoPlay combina il valore dell'azione e il valore del provider con la parola "using" per creare una didascalia intuitiva da visualizzare nell'interfaccia utente. Nell'esempio la didascalia risultante è "Play Music using Windows Media Player".

Il valore DefaultIcon punta a un file con estensione ico o a una risorsa in un file binario. Se il valore numerico che segue il nome del file binario è pari a zero o superiore, è il valore di indice dell'icona in tale file binario. Se è un valore negativo, si tratta dell'ID risorsa dell'icona. Sono consigliati valori di indice negativi. Non è necessario alcun valore nel caso di un file con estensione ico. Si consiglia di usare le variabili di ambiente nel percorso.

Il valore InitCmdLine passa senza modifiche tramite il metodo [**IHWEventHandler:: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) prima che vengano chiamati altri metodi.

Nell'esempio seguente vengono illustrate le sottochiavi e i valori utilizzati per un dispositivo che può essere letto direttamente, ad esempio un'unità CD-ROM o un altro disco rimovibile. Anche in questo caso, il gestore di esempio è denominato **DataHandler**.

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     Handlers
                        MyHandler
                           Action [REG_SZ] = @%systemroot%\System32\wiaacmgr.exe,-276
                           DefaultIcon [REG_EXPAND_SZ] = %systemroot%\System32\wiaacmgr.exe,-2
                           InvokeProgID [REG_SZ] = WIA.AutoPlayDropHandler
                           InvokeVerb [REG_SZ] = open
                           Provider [REG_SZ] = @%systemroot%\System32\wiaacmgr.exe,-101
```

In questo esempio, i valori dell'azione e del provider vengono visualizzati come nome file con una stringa di risorsa invece che con valori letterali, ma le stringhe a cui fanno riferimento vengono utilizzate nello stesso modo. Vengono combinati con la parola "using" per creare una didascalia descrittiva, come illustrato in precedenza.

I valori InvokeProgID e InvokeVerb sostituiscono CLSID, InitCmdLine e ProgID. I valori InvokeProgID e InvokeVerb corrispondono ai nomi di chiave presenti nella **\_ \_ radice delle classi HKEY**, come illustrato nella voce del registro di sistema seguente. Questo set di chiavi di esempio corrisponde all'esempio di gestore specifico descritto in precedenza.

```
HKEY_CLASSES_ROOT
   WIA.AutoplayDropHandler
      shell
         open
            DropTarget
               Clsid = {F1ABE2B5-C073-4dba-B6EB-FD7A5111DD8F}
```

La funzione [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) utilizza il CLSID per implementare l'applicazione appropriata.

Dopo aver definito il gestore in uno di questi due modi, è necessario registrarlo per un evento specifico. A tale scopo, è necessario fornire il nome del gestore come valore per la chiave di tale evento in **EventHandlers**. Nell'esempio seguente viene illustrato come registrare il gestore di **gestione** per l'evento GenericVolumeArrival. Non è stato assegnato alcun valore di dati.

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     EventHandlers
                        GenericVolumeArrival
                           MyHandler [REG_SZ]
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
