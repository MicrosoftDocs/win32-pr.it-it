---
title: Registro di sistema dello schema personalizzato Impostazioni
description: Registro di sistema dello schema personalizzato Impostazioni
ms.assetid: ded2b492-7755-4ba5-87cf-720a79ec79de
keywords:
- Windows Media Player,impostazioni del Registro di sistema degli schemi personalizzati
- Windows Media Player,schemi
- Windows Media Player,registro
- Registro di sistema, impostazioni schema personalizzate
- registro, schemi
- Registro di sistema, impostazioni per Windows Media Player
- schemi
- impostazioni del Registro di sistema dello schema personalizzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1f20b69570a18d256049bb0e785099e43b091d080e4f9f65e62655c3103d68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750394"
---
# <a name="custom-scheme-registry-settings"></a>Registro di sistema dello schema personalizzato Impostazioni

Gli schemi sono protocolli personalizzati. Windows Media Player gestisce un elenco di schemi nel Registro di sistema nel computer dell'utente. Quando l'utente tenta di riprodurre un file multimediale digitale, Il lettore controlla prima se l'SDK Windows Media Format supporta lo schema. In caso contrario, il lettore controlla lo schema rispetto all'elenco nel registro. Se viene trovata una corrispondenza, il lettore controlla quindi un valore che indica quale tecnologia o *runtime* sottostante (ad esempio Microsoft DirectShow o Windows Media Format SDK) può essere usato per riprodurre il file. Se non viene trovata alcuna corrispondenza, il lettore visualizza all'utente una finestra di dialogo di avviso che richiede all'utente l'autorizzazione per provare a riprodurre il file. Se si esegue lo streaming di file multimediali digitali usando uno schema di protocollo personalizzato, è possibile evitare che questo avviso venga visualizzato nel computer dell'utente registrando lo schema e specificando un valore per il runtime.

L'elenco degli schemi viene gestito come set di chiavi del Registro di sistema corrispondenti a schemi registrati, senza i due punti e le due barre (://). Ad esempio, la chiave per lo schema wmhtml://, che viene usato per lo streaming di contenuti multimediali rtf, è denominata "wmhtml". Viene mantenuto un elenco separato per il computer locale e per ogni utente. Per il computer locale, le chiavi dello schema sono sottochiavi della chiave del Registro di sistema seguente:

**HKEY \_ LOCAL MACHINE Software Schemi \_ \\ \\ \\ \\ WMPlayer multimediali Microsoft \\\\**

Ad esempio, la chiave per lo schema wmhtml:// per il computer locale è:

**HKEY \_ LOCAL MACHINE Software Microsoft Multimedia \_ \\ \\ \\ \\ WMPlayer \\ Schemes \\ wmhtml**

Per modificare i valori di questa chiave o creare una nuova sottochiave, l'utente corrente deve essere un amministratore del computer.

Per i singoli utenti, le chiavi dello schema sono sottochiavi della chiave del Registro di sistema seguente:

**HKEY \_ CURRENT \_ USER \\ Software \\ Microsoft \\ MediaPlayer \\ Player \\ Schemes\\**

Ad esempio, la chiave per lo schema wmhtml:// per l'utente corrente è:

**HKEY \_ CURRENT USER Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Player Schemes \\ \\ wmhtml**

Quando si verifica la presenza di schemi registrati, il lettore controlla innanzitutto i valori che si trovano in **HKEY \_ LOCAL \_ MACHINE**. Se non ne viene trovato nessuno per lo schema corrente, il lettore controlla quindi i valori in **HKEY \_ CURRENT \_ USER**. Se non ne viene trovato nessuno per lo schema corrente, il lettore visualizza l'avviso all'utente.

Ogni sottochiave dello schema può contenere uno dei valori possibili seguenti per *runtime*.



| Valore | Descrizione                                |
|-------|--------------------------------------------|
| 6     | Eseguire il rendering usando Windows Media Format SDK. |
| 7     | Eseguire il rendering con Microsoft DirectShow.         |



 

La modifica *del valore* runtime per uno schema supportato Windows Media Format SDK non avrà alcun effetto. Il lettore userà sempre Windows Media Format SDK come runtime per gli schemi supportati Windows Media Format SDK. Questo valore del Registro di sistema è progettato per consentire la configurazione di runtime per gli schemi personalizzati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Registro di sistema Impostazioni**](registry-settings.md)
</dt> </dl>

 

 




