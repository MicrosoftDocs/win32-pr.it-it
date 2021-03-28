---
description: È possibile utilizzare un'estensione dello spazio dei nomi per consentire agli utenti di esplorare il contenuto di un file anziché presentarlo come cartella. Le estensioni di questo tipo vengono in genere utilizzate per visualizzare il contenuto dei membri di un tipo di file.
title: Come visualizzare una visualizzazione radice di un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ee16f3ce50cd79800dd98aa53256591d1f79d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881573"
---
# <a name="how-to-display-a-rooted-view-of-a-file"></a>Come visualizzare una visualizzazione radice di un file

È possibile utilizzare un'estensione dello spazio dei nomi per consentire agli utenti di esplorare il contenuto di un file anziché presentarlo come cartella. Le estensioni di questo tipo vengono in genere utilizzate per visualizzare il contenuto dei membri di un [tipo di file](fa-file-types.md). Ad esempio, i membri di un tipo di file potrebbero contenere più file o immagini compresse, organizzati in una gerarchia. Invece di scrivere un'applicazione per consentire all'utente di visualizzare il contenuto di un file di questo tipo, è possibile scrivere un'estensione dello spazio dei nomi e lasciare che Esplora risorse gestisca la visualizzazione.

Per fare in modo che un'estensione visualizzi il contenuto di un file, è necessario utilizzare una vista radice. Il modo più comune per fornire una visualizzazione radice dei membri di un tipo di file consiste nel definire un [verbo di menu di scelta rapida](context.md) che avvii un'istanza di Explorer.exe. Se si imposta questo verbo come verbo predefinito, un doppio clic apre anche una visualizzazione radice del file. È possibile definire un verbo per tutti i membri del tipo di file [modificando il registro di sistema](context.md)o definire in modo dinamico i verbi in base al file mediante l'implementazione di un [gestore di menu di scelta rapida](context-menu-handlers.md).

## <a name="instructions"></a>Istruzioni


Nell'esempio seguente viene illustrato come utilizzare il registro di sistema per fornire una visualizzazione radice dei membri di un tipo di file modificando il registro di sistema. La voce del registro di sistema di esempio è una modifica di uno degli esempi nell' [estensione dei menu di scelta rapida](context.md). Le voci del registro di sistema definiscono i file con estensione MYP come tipo di file e usano il verbo **Browse** per avviare una visualizzazione radice dei membri di quel tipo.

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

È possibile usare lo stesso verbo per avviare a livello di codice una visualizzazione radice di un membro del tipo di file chiamando la funzione [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione della posizione di un'estensione dello spazio dei nomi](nse-junction.md)
</dt> <dt>

[Come aprire una visualizzazione radice di un punto di giunzione tramite il registro di sistema](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> <dt>

[Come aprire una visualizzazione radice di un punto di giunzione tramite un file di collegamento](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> <dt>

[**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 



