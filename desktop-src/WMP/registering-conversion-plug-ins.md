---
title: Registrazione di plug-in di conversione
description: Registrazione di plug-in di conversione
ms.assetid: d7d6e733-7288-4707-a54a-dcaa71601646
keywords:
- Windows Media Player, plug-in di conversione
- Plug-in di Windows Media Player, conversione
- plug-in, conversione
- plug-in di conversione, registrazione
- Registro di sistema, plug-in di conversione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301d24e38cb4672936923cea9edd7fe6b3d2dc5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298063"
---
# <a name="registering-conversion-plug-ins"></a>Registrazione di plug-in di conversione

I formati di terze parti devono essere registrati prima che Windows Media Player possa creare un'istanza e usare il plug-in di conversione. Per registrare il file per la conversione, è necessario registrare l'estensione del nome file associata al formato.

L'elenco delle estensioni di file registrate viene mantenuto come un set di chiavi del registro di sistema. Per informazioni dettagliate sulla registrazione di formati di terze parti, vedere [impostazioni del registro di sistema per l'estensione del nome file](file-name-extension-registry-settings.md). Nella tabella seguente sono elencate le impostazioni relative ai valori del registro di sistema per registrare un formato di terze parti per la conversione tramite un plug-in di conversione.



| Valore                  | Impostazione                                                     |
|------------------------|-------------------------------------------------------------|
| **Runtime**            | 13                                                          |
| **Autorizzazioni**        | 8 (autorizzazione per la libreria).                             |
| **ConvertPluginCLSID** | ID della classe del plug-in di conversione, nel formato del registro di sistema. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Riferimento alla programmazione di plug-in di conversione**](conversion-plug-ins-programming-reference.md)
</dt> </dl>

 

 




