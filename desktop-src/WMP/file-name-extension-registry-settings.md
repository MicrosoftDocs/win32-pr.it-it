---
title: Impostazioni del registro di sistema estensione del nome file
description: Impostazioni del registro di sistema estensione del nome file
ms.assetid: a5c31cf7-e1e1-4f1a-8e94-ed08f99ad973
keywords:
- Windows Media Player, registro di sistema
- Windows Media Player, estensioni di file
- Registro di sistema, estensioni di file
- Registro di sistema, impostazioni per Windows Media Player
- impostazioni del registro di sistema estensione del nome file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c526e38ae1b2b76b942e0646df6f8aaa3b8e3417
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712952"
---
# <a name="file-name-extension-registry-settings"></a>Impostazioni del registro di sistema estensione del nome file

Se i file multimediali digitali hanno un formato personalizzato, è possibile specificare Windows Media Player con informazioni sul formato personalizzato inserendo le voci nel registro di sistema nel computer dell'utente. Windows Media Player controlla le voci del registro di sistema per determinare come gestire i file. Nell'elenco seguente vengono illustrate alcune delle operazioni che è possibile eseguire creando voci del registro di sistema relative al formato di file multimediale personalizzato.

-   Concedere all'utente l'autorizzazione per la riproduzione, la copia o la transcodifica dei file.
-   Specificare la tecnologia sottostante che il lettore deve utilizzare per riprodurre i file.
-   Specificare la posizione in cui il lettore deve visualizzare i file nella visualizzazione libreria.
-   Specificare un plug-in che il lettore deve usare per convertire i file in un formato standard.
-   Specificare un codice di formato MTP (Media Transport Protocol) che il lettore può usare per determinare se un dispositivo portatile specifico supporta il formato di file.

La maggior parte delle voci fornite si troverà sotto una sottochiave associata all'estensione del nome file personalizzata. È possibile creare tale sottochiave nel \_ \_ sottoalbero del computer locale HKEY e nel \_ \_ sottoalbero HKEY Current User. Windows Media Player cerca innanzitutto nel \_ \_ sottoalbero del computer locale HKEY. Se non trova il risultato necessario, Cerca nel \_ \_ sottoalbero dell'utente corrente di HKEY. Si noti che il codice che tenta di scrivere nel registro di sistema nel computer dell'utente può scrivere nel \_ sottoalbero del computer locale HKEY \_ solo se l'utente corrente dispone di privilegi amministrativi.

Per scrivere informazioni sul formato di file personalizzato nel \_ \_ sottoalbero del computer locale hKey, creare la sottochiave seguente.

**HKEY \_ \_Computer locale \\ software \\ Microsoft \\ Multimedia \\ wmplayer \\ Extensions \\** *customExtension*

dove *customExtension* è l'estensione del nome di file, incluso il separatore del punto (.). Se, ad esempio, l'estensione per il formato di file personalizzato è. xyz, creare la sottochiave seguente.

**HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Multimedia \\ wmplayer \\ Extensions \\ . xyz**

Per scrivere informazioni sul formato di file personalizzato nel \_ sottoalbero dell'utente corrente di HKEY \_ , creare la sottochiave seguente.

**HKEY \_ \_Software utente \\ corrente \\ Microsoft \\ MediaPlayer \\ Player \\ Extensions \\** *customExtension*

È possibile scrivere una o più delle voci seguenti nella sottochiave *customExtension* .

-   **Autorizzazioni**
-   **Runtime**
-   **FormatCode**

Per specificare i plug-in di conversione per il formato di file multimediale personalizzato, creare una sottochiave **ConvertPluginCLSID** nella sottochiave *customExtension* .

Per specificare la posizione in cui Windows Media Player deve visualizzare i file nella visualizzazione libreria, scrivere una voce che rappresenti il formato di file personalizzato nella sottochiave seguente.

**HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ MediaPlayer \\ MLS \\ Extensions**

Negli argomenti seguenti vengono descritte le sottochiavi e le voci del registro di sistema che forniscono Windows Media Player con informazioni sui formati di file multimediali personalizzati.

-   [Voce del registro di sistema autorizzazioni](permissions-registry-entry.md)
-   [Voce del registro di sistema runtime](runtime-registry-entry.md)
-   [Voce del registro di sistema FormatCode](formatcode-registry-entry.md)
-   [Voci del registro di sistema di classificazione delle librerie](library-classification-registry-entries.md)
-   [Sottochiave ConvertPluginCLSID](convertpluginclsid-subkey.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Impostazioni del registro di sistema**](registry-settings.md)
</dt> <dt>

[**Plug-in di conversione di Windows Media Player**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




