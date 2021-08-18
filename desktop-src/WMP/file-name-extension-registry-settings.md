---
title: File Name Extension Registry Impostazioni
description: File Name Extension Registry Impostazioni
ms.assetid: a5c31cf7-e1e1-4f1a-8e94-ed08f99ad973
keywords:
- Windows Media Player,Registro di sistema
- Windows Media Player,estensioni di file
- Registro di sistema, estensioni di file
- Registro di sistema, impostazioni per Windows Media Player
- Impostazioni del Registro di sistema dell'estensione del nome file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4acea080c59b4f78d4b4053f6ae67e5d1eb2c820d68b4e4702485130d8f33a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996631"
---
# <a name="file-name-extension-registry-settings"></a>File Name Extension Registry Impostazioni

Se i file multimediali digitali hanno un formato personalizzato, è possibile fornire Windows Media Player informazioni sul formato personalizzato inserendo le voci nel Registro di sistema nel computer dell'utente. Windows Media Player esamina le voci del Registro di sistema per determinare come gestire i file. L'elenco seguente illustra diverse operazioni che è possibile eseguire creando voci del Registro di sistema relative al formato di file multimediale personalizzato.

-   Concedere al lettore l'autorizzazione per riprodurre, copiare o transcodificare i file.
-   Specificare la tecnologia sottostante che il lettore deve usare per riprodurre i file.
-   Specificare dove il lettore deve visualizzare i file nella visualizzazione della libreria.
-   Specificare un plug-in che il lettore deve usare per convertire i file in un formato standard.
-   Specificare un codice di formato MTP (Media Transport Protocol) che il lettore può usare per determinare se un particolare dispositivo portatile supporta il formato di file.

La maggior parte delle voci fornite si trova in una sottochiave associata all'estensione di file personalizzata. È possibile creare tale sottochiave nel sottoalbero HKEY LOCAL MACHINE e nel sottoalbero \_ \_ HKEY CURRENT \_ \_ USER. Windows Media Player cerca prima nel sottoalbero HKEY \_ LOCAL \_ MACHINE. Se non trova le informazioni necessarie, viene cercata nel sottoalbero HKEY \_ CURRENT \_ USER. Si noti che qualsiasi codice che tenta di scrivere nel Registro di sistema nel computer dell'utente può scrivere nel sottoalbero HKEY LOCAL MACHINE solo se l'utente corrente dispone di \_ \_ privilegi amministrativi.

Per scrivere informazioni sul formato di file personalizzato nel sottoalbero HKEY \_ LOCAL \_ MACHINE, creare la sottochiave seguente.

**HKEY \_ Local \_ MACHINE Software Microsoft Multimedia \\ \\ \\ \\ WMPlayer \\ Extensions \\** *customExtension*

dove *customExtension è* l'estensione del nome file incluso il separatore punto (.). Ad esempio, se l'estensione per il formato di file personalizzato è xyz, creare la sottochiave seguente.

**HKEY \_ LOCAL MACHINE Software Microsoft Multimedia \_ \\ \\ \\ \\ WMPlayer \\ Extensions \\ .xyz**

Per scrivere informazioni sul formato di file personalizzato nel sottoalbero HKEY \_ CURRENT \_ USER, creare la sottochiave seguente.

**HKEY \_ CURRENT \_ USER Software Microsoft \\ \\ \\ MediaPlayer \\ Player \\ Extensions \\** *customExtension*

È possibile scrivere una o più delle voci seguenti nella *sottochiave customExtension.*

-   **Autorizzazioni**
-   **Runtime**
-   **FormatCode**

Per specificare i plug-in di conversione per il formato di file multimediale personalizzato, creare una **sottochiave ConvertPluginCLSID** nella *sottochiave customExtension.*

Per specificare dove Windows Media Player visualizzare i file nella visualizzazione della libreria, scrivere una voce che rappresenta il formato di file personalizzato nella sottochiave seguente.

**HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ MediaPlayer \\ MLS \\ Extensions**

Negli argomenti seguenti vengono descritte le sottochiavi e le voci del Registro di sistema Windows Media Player informazioni sui formati di file multimediali personalizzati.

-   [Voce del Registro di sistema Permissions](permissions-registry-entry.md)
-   [Voce del Registro di sistema di runtime](runtime-registry-entry.md)
-   [Voce del Registro di sistema FormatCode](formatcode-registry-entry.md)
-   [Voci del Registro di sistema di classificazione delle librerie](library-classification-registry-entries.md)
-   [Sottochiave ConvertPluginCLSID](convertpluginclsid-subkey.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Registro di sistema Impostazioni**](registry-settings.md)
</dt> <dt>

[**Windows Media Player Plug-in di conversione**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




