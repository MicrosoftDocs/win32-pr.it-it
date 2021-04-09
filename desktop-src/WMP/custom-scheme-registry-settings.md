---
title: Impostazioni del registro di sistema personalizzato
description: Impostazioni del registro di sistema personalizzato
ms.assetid: ded2b492-7755-4ba5-87cf-720a79ec79de
keywords:
- Windows Media Player, impostazioni del registro di sistema personalizzato
- Windows Media Player, schemi
- Windows Media Player, registro di sistema
- Registro di sistema, Impostazioni schema personalizzate
- Registro di sistema, schemi
- Registro di sistema, impostazioni per Windows Media Player
- schemi
- impostazioni del registro di sistema personalizzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a02649d9536140fff0ff0d3188a5b25feb49688
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044304"
---
# <a name="custom-scheme-registry-settings"></a>Impostazioni del registro di sistema personalizzato

Gli schemi sono protocolli personalizzati. Windows Media Player gestisce un elenco di schemi nel registro di sistema nel computer dell'utente. Quando l'utente tenta di riprodurre un file multimediale digitale, il giocatore verifica prima di tutto se Windows Media Format SDK supporta lo schema. In caso contrario, il lettore controlla lo schema rispetto all'elenco nel registro di sistema. Se viene trovata una corrispondenza, il lettore controlla un valore che indica quale tecnologia o *Runtime* sottostante (ad esempio Microsoft DirectShow o Windows Media Format SDK) può essere usato per riprodurre il file. Se non viene trovata alcuna corrispondenza, il lettore Visualizza all'utente una finestra di dialogo di avviso che richiede all'utente l'autorizzazione per tentare di riprodurre il file. Se si esegue lo streaming di file multimediali digitali utilizzando uno schema di protocollo personalizzato, è possibile impedire che questo avviso venga visualizzato nel computer dell'utente registrando lo schema e fornendo un valore per il Runtime.

L'elenco di schemi viene mantenuto come un set di chiavi del registro di sistema che corrispondono agli schemi registrati, senza i due punti e le due barre (://). Ad esempio, la chiave per lo schema wmhtml://, usata per lo streaming di file multimediali avanzati, è denominata "wmhtml". Viene mantenuto un elenco separato per il computer locale e per ogni utente. Per il computer locale, le chiavi dello schema sono sottochiavi della chiave del registro di sistema seguente:

**HKEY \_ \_ computer locale \\ software \\ Microsoft \\ Multimedia \\ wmplayer \\ Scheme\\**

Ad esempio, la chiave per lo schema wmhtml://per il computer locale è:

**HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Multimedia \\ wmplayer \\ schemes \\ wmhtml**

Per modificare i valori in questa chiave o creare una nuova sottochiave, l'utente corrente deve essere un amministratore del computer.

Per i singoli utenti, le chiavi dello schema sono sottochiavi della chiave del registro di sistema seguente:

**HKEY \_ \_ software utente \\ corrente \\ \\ schemi Microsoft MediaPlayer \\ Player \\\\**

Ad esempio, la chiave per lo schema wmhtml://per l'utente corrente è:

**HKEY \_ \_ software utente \\ corrente \\ Microsoft \\ MediaPlayer \\ Player \\ schemes \\ wmhtml**

Quando si verificano gli schemi registrati, il lettore controlla prima i valori presenti nel **\_ \_ computer locale HKEY**. Se non ne viene trovato nessuno per lo schema corrente, il lettore controlla i valori **nell' \_ \_ utente corrente di HKEY**. Se non viene trovato alcuno per lo schema corrente, il lettore Visualizza l'avviso per l'utente.

Ogni sottochiave dello schema può contenere uno dei seguenti valori possibili per il *Runtime*.



| Valore | Descrizione                                |
|-------|--------------------------------------------|
| 6     | Eseguire il rendering usando Windows Media Format SDK. |
| 7     | Eseguire il rendering con Microsoft DirectShow.         |



 

La modifica del valore di *Runtime* per uno schema supportato da Windows Media Format SDK non avrà alcun effetto. Il lettore utilizzerà sempre Windows Media Format SDK come runtime per gli schemi supportati da Windows Media Format SDK. Questo valore del registro di sistema è progettato per consentire la configurazione di runtime per gli schemi personalizzati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Impostazioni del registro di sistema**](registry-settings.md)
</dt> </dl>

 

 




