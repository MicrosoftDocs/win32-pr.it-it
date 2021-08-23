---
description: È possibile usare un'estensione dello spazio dei nomi per consentire agli utenti di esplorare il contenuto di un file anziché presentarlo come cartella. Le estensioni di questo tipo vengono in genere utilizzate per visualizzare il contenuto dei membri di un tipo di file.
title: Come visualizzare una visualizzazione radice di un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c91e17ef12393b1a95316c37a18d51876cf988293c330610a3638c7995ab12a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596581"
---
# <a name="how-to-display-a-rooted-view-of-a-file"></a>Come visualizzare una visualizzazione radice di un file

È possibile usare un'estensione dello spazio dei nomi per consentire agli utenti di esplorare il contenuto di un file anziché presentarlo come cartella. Le estensioni di questo tipo vengono in genere utilizzate per visualizzare il contenuto dei membri di un [tipo di file](fa-file-types.md). Ad esempio, i membri di un tipo di file possono contenere più file compressi o immagini organizzati in una gerarchia. Invece di scrivere un'applicazione per consentire all'utente di visualizzare il contenuto di un file di questo tipo, è possibile scrivere un'estensione dello spazio dei nomi e consentire Windows Explorer di gestire la visualizzazione.

È necessario usare una visualizzazione radice per consentire a un'estensione di visualizzare il contenuto di un file. Il modo più comune per fornire una visualizzazione radice dei membri di un tipo di file è definire un [verbo](context.md) del menu di scelta rapida che avvia un'istanza di Explorer.exe. Impostando questo verbo come verbo predefinito, un doppio clic aprirà anche una visualizzazione radice del file. È possibile definire un verbo per tutti [](context.md)i membri del tipo di file modificando il Registro di sistema oppure definire in modo dinamico i verbi file per file implementando un gestore del menu di scelta [rapida](context-menu-handlers.md).

## <a name="instructions"></a>Istruzioni


Nell'esempio seguente viene illustrato come utilizzare il Registro di sistema per fornire una visualizzazione radice dei membri di un tipo di file modificando il Registro di sistema. La voce del Registro di sistema di esempio è una modifica di uno degli esempi in [Estensione dei menu di scelta rapida.](context.md) Le voci del Registro di sistema definiscono i file con estensione myp come tipo di file e usano il verbo **browse** per avviare una visualizzazione radice dei membri di quel tipo.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = browse
         browse
            command
               (Default) = %SYSTEMROOT%\explorer.exe /e,/root,{Extension CLSID}, "%1"
```

È possibile usare lo stesso verbo per avviare a livello di codice una visualizzazione radice di un membro del tipo di file chiamando la [**funzione ShellExecute.**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica del percorso di un'estensione dello spazio dei nomi](nse-junction.md)
</dt> <dt>

[Come aprire una visualizzazione radice di un punto di giunzione tramite il Registro di sistema](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> <dt>

[Come aprire una visualizzazione radice di un punto di giunzione tramite un file di collegamento](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> <dt>

[**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 



