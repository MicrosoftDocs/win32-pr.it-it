---
title: API del plug-in WinRM
description: Il plug-in WinRM Application Programming Interface (API) fornisce funzionalità che consentono a un utente di scrivere plug-in implementando determinate API per le operazioni e gli URI delle risorse supportati.
ms.assetid: d3e103c1-221b-441b-8bcb-883e3f2a4c1a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ccc8920f7df788b4df355b0cbc23478e97111d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955627"
---
# <a name="winrm-plug-in-api"></a>API del plug-in WinRM

I plug-in Gestione remota Windows sono librerie di collegamento dinamico (dll) native che consentono di collegare ed estendere le funzionalità di WinRM. Il plug-in WinRM Application Programming Interface (API) fornisce funzionalità che consentono a un utente di scrivere plug-in implementando determinate API per le operazioni e gli [*URI delle risorse*](windows-remote-management-glossary.md) supportati. Una volta configurati i plug-in per il servizio WinRM o Internet Information Services (IIS), vengono caricati rispettivamente nell'host WinRM o nell'host IIS. Le richieste remote vengono instradate a questi punti di ingresso plug-in per eseguire le operazioni.

La sezione di riferimento dell'API del plug-in WinRM contiene informazioni dettagliate sugli elementi API seguenti:

-   [Punti di ingresso del plug-in di autorizzazione](authorization-plug-in-entry-points.md)
-   [Metodi plug-in di autorizzazione](authorization-plug-in-methods.md)
-   [Punti di ingresso del plug-in per le operazioni](operations-plug-in-entry-points.md)
-   [Metodi del plug-in per le operazioni](operations-plug-in-methods.md)
-   [Strutture](winrm-plug-in-api-structures.md)

 

 




