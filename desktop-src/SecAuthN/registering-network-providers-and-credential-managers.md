---
description: Dopo aver creato il provider di rete o Gestione credenziali, è necessario registrarlo nel sistema.
ms.assetid: 4c58671d-d11d-4f32-866b-e278fc8e6114
title: Registrazione di provider di rete e gestori di credenziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de34c97b61f685c3e779bd487fbc2c5b21fa7af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231841"
---
# <a name="registering-network-providers-and-credential-managers"></a>Registrazione di provider di rete e gestori di credenziali

Dopo aver creato il provider di rete o Gestione credenziali, è necessario registrarlo nel sistema. Questa operazione è necessaria per consentire a MPR di sapere quali provider di rete sono installati. All'avvio di MPR, viene verificato il registro di sistema e vengono caricati i provider di rete o i gestori di credenziali trovati.

Poiché i provider di rete e i gestori di credenziali sono correlati, vengono registrati nelle stesse sottochiavi del registro di sistema. Di fatto, le dll del provider di rete possono anche essere gestori di credenziali.

Per informazioni dettagliate sulle chiavi del registro di sistema che è necessario creare per il provider di rete o Gestione credenziali, vedere [autenticazione delle chiavi del registro](authentication-registry-keys.md)di sistema.

 

 



