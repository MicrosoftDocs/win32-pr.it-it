---
title: Configurazione del server per i caricamenti
description: Per caricare file in un server tramite BITS, è necessario che nel server siano installati IIS e l'estensione del server BITS ISAPI. Per i requisiti iis, vedere Requisiti IIS per i caricamenti BITS.
ms.assetid: 2f3a2f99-b9de-41da-897f-a4d9c6d5e8c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e075478f6e0335c6bf601a9289d93d4d3fac2aefd9e4f1ef820e938a1bfc0ab7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004721"
---
# <a name="setting-up-the-server-for-uploads"></a>Configurazione del server per i caricamenti

Per caricare file in un server tramite BITS, è necessario che nel server siano installati IIS e l'estensione del server BITS ISAPI. Per i requisiti iis, vedere [Requisiti IIS per i caricamenti BITS](iis-requirements-for-bits-uploads.md).

Per informazioni sulla configurazione della directory virtuale IIS utilizzata da BITS per i caricamenti, vedere gli argomenti seguenti.

-   [Impostazione delle autorizzazioni per le directory virtuali](setting-permissions-on-virtual-directories.md)
-   [Scrittura di uno script per configurare la directory virtuale](writing-a-script-to-configure-the-virtual-directory.md)
-   [Uso dell'interfaccia utente di IIS per configurare la directory virtuale](using-the-iis-ui-to-configure-the-virtual-directory.md)
-   [Prevenzione di più caricamenti](preventing-multiple-uploads.md)
-   [Upload Procedure consigliate](upload-best-practices.md)

> [!Note]  
> Alcune installazioni di IIS includono il componente di filtro UrlScan. Se UrlScan è abilitato, l'amministratore deve aggiungere il verbo "BITS \_ POST" all'elenco di verbi HTTP consentiti di UrlScan. In caso contrario, i caricamenti del client BITS avranno esito negativo. Per altre informazioni sull'abilitazione dei verbi in UrlScan, vedere la documentazione di UrlScan.

 

 

 




