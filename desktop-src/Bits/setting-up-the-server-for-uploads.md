---
title: Configurazione del server per i caricamenti
description: Per caricare file in un server utilizzando BITS, è necessario che nel server sia installato IIS e l'ISAPI estensione server BITS. Per i requisiti di IIS, vedere requisiti di IIS per i caricamenti BITS.
ms.assetid: 2f3a2f99-b9de-41da-897f-a4d9c6d5e8c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2ef81019f4c69157c267cd2438188f440299a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220970"
---
# <a name="setting-up-the-server-for-uploads"></a>Configurazione del server per i caricamenti

Per caricare file in un server utilizzando BITS, è necessario che nel server sia installato IIS e l'ISAPI estensione server BITS. Per i requisiti di IIS, vedere [requisiti di IIS per i caricamenti bits](iis-requirements-for-bits-uploads.md).

Per informazioni sulla configurazione della directory virtuale IIS utilizzata da BITS per il caricamento, vedere gli argomenti seguenti.

-   [Impostazione delle autorizzazioni per le directory virtuali](setting-permissions-on-virtual-directories.md)
-   [Scrittura di uno script per configurare la directory virtuale](writing-a-script-to-configure-the-virtual-directory.md)
-   [Utilizzo dell'interfaccia utente di IIS per configurare la directory virtuale](using-the-iis-ui-to-configure-the-virtual-directory.md)
-   [Prevenzione di più caricamenti](preventing-multiple-uploads.md)
-   [Procedure consigliate per il caricamento](upload-best-practices.md)

> [!Note]  
> Alcune installazioni IIS includono il componente di filtro UrlScan. Se UrlScan è abilitato, è necessario che l'amministratore aggiunga il \_ verbo "bits post" all'elenco di verbi HTTP consentiti di URLScan. In caso contrario, i caricamenti client BITS avranno esito negativo. Per ulteriori informazioni sull'abilitazione dei verbi in UrlScan, vedere la documentazione di UrlScan.

 

 

 




