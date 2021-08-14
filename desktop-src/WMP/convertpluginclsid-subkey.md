---
title: Sottochiave ConvertPluginCLSID
description: Sottochiave ConvertPluginCLSID
ms.assetid: 2bf5b6ad-31e9-40c2-a682-c7ad813e8f7a
keywords:
- Windows Media Player,ConvertPluginCLSID sottochiave
- Windows Media Player, estensioni di file
- Windows Media Player,registro
- Registro di sistema, estensioni di file
- registro, sottochiave ConvertPluginCLSID
- Registro di sistema, impostazioni per Windows Media Player
- Impostazioni del Registro di sistema dell'estensione del nome file
- Sottochiave ConvertPluginCLSID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5deeda3e7eb0b5fe465152aa7711717d086c94a06ebed4f9549dc9f6a9b62dd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341665"
---
# <a name="convertpluginclsid-subkey"></a>Sottochiave ConvertPluginCLSID

Quando Windows Media Player 11 rileva un'estensione di file personalizzata, cerca una sottochiave del Registro di sistema corrispondente all'estensione. La sottochiave è descritta in [File Name Extension Registry Impostazioni](file-name-extension-registry-settings.md). In alcuni casi, la sottochiave dell'estensione ha una sottochiave denominata **ConvertPluginCLSID**.

Si supponga, ad esempio, di aver creato un formato di file personalizzato (con estensione xyz) e un plug-in di conversione che converte i file in un formato supportato da Windows Media Player Quindi si archivierebbe l'ID classe del plug-in in una o entrambe le sottochiavi seguenti.

**HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Multimedia \\ WMPlayer \\ Extensions \\ .xyz \\ ConvertPluginCLSID**

**HKEY \_ CURRENT \_ USER \\ Software \\ Microsoft \\ MediaPlayer \\ Player \\ Extensions \\ .xyz \\ ConvertPluginCLSID**

La **sottochiave ConvertPluginCLSID** specifica gli ID di classe dei plug-in che Windows Media Player possono usare per convertire un file multimediale dal formato personalizzato a un formato supportato dal lettore.

La **sottochiave ConvertPluginCLSID** contiene le voci seguenti.

-   Voce predefinita che rappresenta il plug-in di conversione predefinito.
-   Voce denominata che rappresenta il plug-in di conversione predefinito.
-   Voci denominate aggiuntive che rappresentano plug-in di conversione alternativi.

Si supponga, ad esempio, che un formato di file personalizzato abbia un plug-in di conversione predefinito e due plug-in di conversione alternativi. Le voci del Registro di sistema nella **sottochiave ConvertPluginCLSID** hanno il formato seguente.



| Nome                                                                          | Type        | valore                                                                |
|-------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------|
| Predefinito                                                                       | **REG \_ SZ** | ID della classe, in formato registro, del plug-in di conversione predefinito. |
| ID della classe, in formato registro, del plug-in di conversione predefinito.          | **REG \_ SZ** | Nome descrittivo del plug-in di conversione predefinito.                 |
| ID della classe, in formato registro, del primo plug-in di conversione alternativo.  | **REG \_ SZ** | Nome descrittivo del primo plug-in di conversione alternativo.         |
| ID della classe, in formato registro, del secondo plug-in di conversione alternativo. | **REG \_ SZ** | Nome descrittivo del secondo plug-in di conversione alternativo.        |



 

Si noti che il plug-in di conversione predefinito è rappresentato da due voci del Registro di sistema: la voce predefinita e una voce denominata. Windows Media Player usa la voce predefinita per determinare quale plug-in è il plug-in di conversione predefinito (primario). Windows Media Player usa le voci denominate per ottenere nomi descrittivi per tutti i plug-in di conversione, incluso il plug-in predefinito.

Il nome descrittivo di un plug-in di conversione è determinato dalla società che crea il plug-in. Windows Media Player possibile visualizzare il nome descrittivo nella relativa interfaccia utente.

Quando Windows Media Player tenta di convertire un file da un formato personalizzato a un formato standard, carica prima il plug-in predefinito. Se il plug-in predefinito non riesce a convertire il file e restituisce NS E WMP CONVERT PLUGIN UNKNOWN FILE OWNER, il lettore carica ogni plug-in alternativo fino a quando non viene eseguita una conversione corretta o non sono presenti altri \_ \_ \_ \_ \_ \_ \_ plug-in da provare. Il lettore non visualizza un messaggio di avviso se non viene trovato alcun plug-in di conversione per l'estensione del nome file.

La **voce del Registro di sistema ConvertPluginCLSID** è supportata Windows Media Player 11.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**File Name Extension Registry Impostazioni**](file-name-extension-registry-settings.md)
</dt> <dt>

[**Windows Media Player Plug-in di conversione**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




