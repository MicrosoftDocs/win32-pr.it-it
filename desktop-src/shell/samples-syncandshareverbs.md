---
description: Illustra come registrare un verbo che estende l'&\# 0034; Sync&\# 0034; e &\# 0034; Condividere&\# 0034; verbi nella barra dei comandi Windows Explorer.
title: Sincronizzare e condividere i verbi
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 78267C74-7597-4b98-9DAE-89F2FD515C6B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b0a83f69aa866f5eb91eeff56d4313b1ff343f84c69484eb2a9d52614ea19db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117677375"
---
# <a name="sync-and-share-verbs"></a>Sincronizzare e condividere i verbi

Illustra come registrare un verbo che estende i verbi "Sync" e "Share" nella barra dei comandi Windows Explorer.

In questo argomento sono contenute le sezioni seguenti.

-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)
-   [Rimozione dell'esempio](#removing-the-sample)

## <a name="requirements"></a>Requisiti



| Prodotto                                | Versione minima del prodotto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

| Località      | URL del percorso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Esempio di SyncAndShareVerbs](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/SyncAndShareVerbs) |

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Per eseguire l'esempio (sincronizzazione):

1.  Passare alla directory che contiene il `sync.reg` file
2.  Digitare `sync.reg ` nella riga di comando oppure fare doppio clic sull'icona per `sync.reg` registrarla.
3.  Aprire il Windows e selezionare un file.
4.  Fare clic **sull'opzione** Sincronizza sulla barra dei comandi e selezionare un'opzione **secondaria, ad esempio Paint**.

Per eseguire l'esempio (condivisione):

1.  Passare alla directory che contiene il `share.reg` file.
2.  Digitare `share.reg` nella riga di comando oppure fare doppio clic sull'icona per `share.reg` registrarla.
3.  Aprire Windows Explorer e selezionare un file. Fare clic **sull'opzione** Condividi sulla barra dei comandi.
4.  Fare clic **sull'opzione** Condividi con sulla barra dei comandi e selezionare un'opzione **secondaria, ad esempio Paint**.

## <a name="removing-the-sample"></a>Rimozione dell'esempio

Per rimuovere l'esempio (sincronizzazione):

1.  Passare alla directory che contiene il file Uninstallsync.reg.
2.  Digitare `uninstallsync.reg` nella riga di comando oppure fare doppio clic sull'icona per `uninstallsync.reg` .

Per rimuovere l'esempio (condivisione):

1.  Passare alla directory che contiene il file Uninstallshare.reg.
2.  Digitare `uninstallshare.reg` nella riga di comando oppure fare doppio clic sull'icona per `uninstallshare.reg.`

 

 



