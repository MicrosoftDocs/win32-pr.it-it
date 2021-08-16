---
description: Descrive i processi per l'implementazione di gestori di eventi del dispositivo nel Registro di sistema.
ms.assetid: 84B12B5C-C179-4124-A1FC-B90D120336BF
title: Come registrare un gestore per un evento del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a13abe8917d93ac6a4801e0c11cb7223da25e362923df229180b8c8e6211ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859600"
---
# <a name="how-to-register-a-handler-for-a-device-event"></a>Come registrare un gestore per un evento del dispositivo

I gestori definiscono la parte software di AutoPlay. Definiscono l'icona del software e il nome descrittivo, nonché il componente Component Object Model (COM) di cui creare un'istanza e come inizializzare il componente in risposta a un evento. Ogni gestore per un evento specifico viene registrato come valore sotto la chiave **EventHandler** appropriata. Quando viene rilevato tale evento, all'utente viene richiesto di scegliere un gestore da un elenco di tutti i gestori registrati per l'evento.

## <a name="instructions"></a>Istruzioni


I gestori e i valori associati sono definiti sotto la **chiave AutoplayHandlers** \\ **Handlers.** Le sottochiavi variano a seconda che il sistema possa leggere direttamente il contenuto del dispositivo o se il dispositivo fornisce il contenuto al sistema tramite un'interfaccia proprietaria.

L'esempio seguente illustra le sottochiavi e i valori usati per un dispositivo, ad esempio una videocamera digitale o un lettore .mp3, che ne fornisce il contenuto al sistema tramite un'interfaccia proprietaria. Il gestore di esempio è **denominato MyHandler**.

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
> Mentre l'esempio mostra sia un ProgID che un valore di identificatore di classe (CLSID), in pratica questi valori si escludono a vicenda in modo che sia presente solo uno o l'altro. È preferibile il valore ProgID. A seconda del tipo usato, deve puntare a un componente COM che implementa [**l'interfaccia IHWEventHandler.**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)

 

È possibile immettere il valore Action come valore letterale, ad esempio "Play music" (Riproduci musica), come illustrato in questo esempio, o come nome di file con una stringa di risorsa. È anche possibile immettere il valore Provider come valore letterale o come nome file con una stringa di risorsa. AutoPlay combina il valore Action e il valore Provider con la parola "using" per creare una didascalia descrittiva da visualizzare nell'interfaccia utente. Nell'esempio la didascalia risultante è "Play music using Windows Media Player".

Il valore DefaultIcon punta a un file con estensione ico o a una risorsa in un file binario. Se il valore numerico che segue il nome del file binario è uguale o maggiore di zero, è il valore di indice dell'icona in tale file binario. Se è un valore negativo, è l'ID risorsa icona. È consigliabile utilizzare valori di indice negativi. Non è necessario alcun valore nel caso di un file con estensione ico. È consigliabile usare le variabili di ambiente nel percorso.

Il valore InitCmdLine passa inalterato tramite il metodo [**IHWEventHandler::Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) prima che venga chiamato qualsiasi altro metodo.

L'esempio seguente illustra le sottochiavi e i valori usati per un dispositivo che può essere letto direttamente, ad esempio un'unità CD-ROM o un altro disco rimovibile. Anche in questo caso, il gestore di esempio è **denominato MyHandler**.

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

In questo esempio i valori Action e Provider vengono visualizzati come nome di file con una stringa di risorsa anziché valori letterali, ma le stringhe a cui fanno riferimento vengono usate nello stesso modo. Vengono combinati con la parola "using" per formare una didascalia descrittiva, come illustrato in precedenza.

I valori InvokeProgID e InvokeVerb sostituiscono CLSID, InitCmdLine e ProgID. I valori InvokeProgID e InvokeVerb corrispondono ai nomi delle chiavi disponibili in **HKEY \_ CLASSES \_ ROOT,** come illustrato nella voce del Registro di sistema seguente. Questo set di chiavi di esempio corrisponde all'esempio di gestore specifico descritto in precedenza.

```
HKEY_CLASSES_ROOT
   WIA.AutoplayDropHandler
      shell
         open
            DropTarget
               Clsid = {F1ABE2B5-C073-4dba-B6EB-FD7A5111DD8F}
```

La [**funzione CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) usa il CLSID per implementare l'applicazione appropriata.

Dopo aver definito il gestore in uno di questi due modi, è necessario registrarlo per un evento specifico. A tale scopo, specificare il nome del gestore come valore per la chiave dell'evento in **EventHandlers**. L'esempio seguente illustra come **registrare MyHandler** come gestore per l'evento GenericVolumeArrival. Non ha alcun valore di dati assegnato.

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

[**Cocreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
