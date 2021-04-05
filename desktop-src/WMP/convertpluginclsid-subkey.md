---
title: Sottochiave ConvertPluginCLSID
description: Sottochiave ConvertPluginCLSID
ms.assetid: 2bf5b6ad-31e9-40c2-a682-c7ad813e8f7a
keywords:
- Media Player di Windows, sottochiave ConvertPluginCLSID
- Windows Media Player, estensioni di file
- Windows Media Player, registro di sistema
- Registro di sistema, estensioni di file
- Registro di sistema, sottochiave ConvertPluginCLSID
- Registro di sistema, impostazioni per Windows Media Player
- impostazioni del registro di sistema estensione del nome file
- Sottochiave ConvertPluginCLSID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4229617c3999708d89fac976e94b2747b5a69145
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044807"
---
# <a name="convertpluginclsid-subkey"></a>Sottochiave ConvertPluginCLSID

Quando Windows Media Player 11 rileva un'estensione del nome di file personalizzata, Cerca una sottochiave del registro di sistema corrispondente all'estensione. La sottochiave è descritta in [impostazioni del registro di sistema estensione del nome file](file-name-extension-registry-settings.md). In alcuni casi, la sottochiave dell'estensione contiene una sottochiave denominata **ConvertPluginCLSID**.

Si supponga, ad esempio, di aver creato un formato di file personalizzato (con estensione xyz) e un plug-in di conversione che converte i file in un formato supportato da Windows Media Player quindi archiviare l'ID classe del plug-in in una o entrambe le sottochiavi riportate di seguito.

**HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Multimedia \\ wmplayer \\ Extensions \\ . xyz \\ ConvertPluginCLSID**

**HKEY \_ \_ software utente \\ corrente \\ Microsoft \\ MediaPlayer \\ Player \\ Extensions \\ . xyz \\ ConvertPluginCLSID**

La sottochiave **ConvertPluginCLSID** specifica gli ID di classe dei plug-in che Windows Media Player può usare per convertire un file multimediale dal formato personalizzato in un formato supportato dal lettore.

La sottochiave **ConvertPluginCLSID** contiene le voci seguenti.

-   Una voce predefinita che rappresenta il plug-in di conversione predefinito.
-   Una voce denominata che rappresenta il plug-in di conversione predefinito.
-   Voci denominate aggiuntive che rappresentano plug-in di conversione alternativi.

Si supponga, ad esempio, che un formato di file personalizzato disponga di un plug-in di conversione predefinito e di due plug-in di conversione alternativi. Le voci del registro di sistema nella sottochiave **ConvertPluginCLSID** hanno il formato seguente.



| Nome                                                                          | Type        | valore                                                                |
|-------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------|
| Predefinito                                                                       | **REG \_ SZ** | ID classe nel formato del registro di sistema del plug-in di conversione predefinito. |
| ID classe nel formato del registro di sistema del plug-in di conversione predefinito.          | **REG \_ SZ** | Nome descrittivo del plug-in di conversione predefinito.                 |
| ID di classe, nel formato del registro di sistema, del primo plug-in di conversione alternativa.  | **REG \_ SZ** | Nome descrittivo del primo plug-in per la conversione alternativa.         |
| ID di classe, nel formato del registro di sistema, del secondo plug-in di conversione alternativa. | **REG \_ SZ** | Nome descrittivo del secondo plug-in di conversione alternativa.        |



 

Si noti che il plug-in di conversione predefinito è rappresentato da due voci del registro di sistema: la voce predefinita e una voce denominata. Windows Media Player utilizza la voce predefinita per determinare quale plug-in è il plug-in di conversione predefinito (primario). Windows Media Player usa le voci denominate per ottenere nomi descrittivi per tutti i plug-in di conversione, incluso il plug-in predefinito.

Il nome descrittivo di un plug-in di conversione è determinato dall'azienda che crea il plug-in. Windows Media Player potrebbe visualizzare il nome descrittivo nella relativa interfaccia utente.

Quando Windows Media Player tenta di convertire un file da un formato personalizzato in un formato standard, carica innanzitutto il plug-in predefinito. Se il plug-in predefinito non riesce a convertire il file e restituisce il plug-in NS \_ e \_ WMP \_ Convert \_ plugin \_ Unknown \_ file \_ Owner, il lettore carica ogni plug-in alternativo fino a quando non si verifica una conversione corretta o non ci sono altri plug-in da provare. Il lettore non visualizza un messaggio di avviso se non viene trovato alcun plug-in di conversione per l'estensione del nome file.

La voce del registro di sistema **ConvertPluginCLSID** è supportata da Windows Media Player 11.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Impostazioni del registro di sistema estensione del nome file**](file-name-extension-registry-settings.md)
</dt> <dt>

[**Plug-in di conversione di Windows Media Player**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




