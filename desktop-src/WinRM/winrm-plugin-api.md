---
title: WinRM Plug-in API
description: L'API (Application Programming Interface) del plug-in WinRM offre funzionalità che consentono a un utente di scrivere plug-in implementando determinate API per gli URI e le operazioni delle risorse supportate.
ms.assetid: d3e103c1-221b-441b-8bcb-883e3f2a4c1a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7359ed212e50b71343ce9a96832060e9ec8121cdf3e11f3f353698e1a4fa9dce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742778"
---
# <a name="winrm-plug-in-api"></a>WinRM Plug-in API

Windows I plug-in di gestione remota sono librerie a collegamento dinamico nativo (DLL) che collegano ed estendono le funzionalità di Gestione remota Windows. L'API (Application Programming Interface) del plug-in WinRM offre funzionalità che consentono a un [](windows-remote-management-glossary.md) utente di scrivere plug-in implementando determinate API per gli URI e le operazioni delle risorse supportate. Dopo aver configurato i plug-in per il servizio WinRM o Internet Information Services (IIS), vengono caricati rispettivamente nell'host WinRM o nell'host IIS. Le richieste remote vengono indirizzate a questi punti di ingresso del plug-in per eseguire operazioni.

La sezione di riferimento sull'API plug-in WinRM contiene informazioni dettagliate sugli elementi API seguenti:

-   [Punti di ingresso del plug-in di autorizzazione](authorization-plug-in-entry-points.md)
-   [Metodi del plug-in di autorizzazione](authorization-plug-in-methods.md)
-   [Punti di ingresso del plug-in operazioni](operations-plug-in-entry-points.md)
-   [Metodi del plug-in operazioni](operations-plug-in-methods.md)
-   [Strutture](winrm-plug-in-api-structures.md)

 

 




