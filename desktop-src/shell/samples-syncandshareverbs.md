---
description: Viene illustrato come registrare un verbo che estende il &\# 0034; Sync&\# 0034; e &\# 0034; Condividere&\# 0034; verbi nella barra dei comandi di Esplora risorse.
title: Sincronizzare e condividere i verbi
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 78267C74-7597-4b98-9DAE-89F2FD515C6B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 734d59ce7b527ad068c03be9083ca67dfca20667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980751"
---
# <a name="sync-and-share-verbs"></a>Sincronizzare e condividere i verbi

Viene illustrato come registrare un verbo che estende i verbi "Sync" e "Share" nella barra dei comandi di Esplora risorse.

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

| Location      | URL percorso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Esempio SyncAndShareVerbs](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/SyncAndShareVerbs) |

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Per eseguire l'esempio (sincronizzazione):

1.  Passare alla directory che contiene il `sync.reg` file
2.  Digitare `sync.reg ` nella riga di comando oppure fare doppio clic sull'icona per `sync.reg` registrarla.
3.  Aprire Esplora risorse e selezionare un file.
4.  Fare clic sull'opzione **Sincronizza** sulla barra dei comandi e selezionare una sottoopzione, ad esempio **Paint**.

Per eseguire l'esempio (share):

1.  Passare alla directory che contiene il `share.reg` file.
2.  Digitare `share.reg` nella riga di comando oppure fare doppio clic sull'icona per `share.reg` registrarla.
3.  Aprire Esplora risorse e selezionare un file. Fare clic sull'opzione **Condividi** sulla barra dei comandi.
4.  Fare clic sull'opzione **Condividi con** nella barra dei comandi e selezionare una sottoopzione, ad esempio **Paint**.

## <a name="removing-the-sample"></a>Rimozione dell'esempio

Per rimuovere l'esempio (sincronizzazione):

1.  Passare alla directory che contiene il file Uninstallsync. reg.
2.  Digitare `uninstallsync.reg` nella riga di comando oppure fare doppio clic sull'icona relativa a `uninstallsync.reg` .

Per rimuovere l'esempio (share):

1.  Passare alla directory che contiene il file Uninstallshare. reg.
2.  Digitare `uninstallshare.reg` nella riga di comando oppure fare doppio clic sull'icona per `uninstallshare.reg.`

 

 



