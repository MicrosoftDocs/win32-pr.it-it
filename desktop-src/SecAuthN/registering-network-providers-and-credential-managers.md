---
description: Dopo aver creato il provider di rete o il gestore delle credenziali, è necessario registrarlo nel sistema.
ms.assetid: 4c58671d-d11d-4f32-866b-e278fc8e6114
title: Registrazione di provider di rete e gestori credenziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eec3b3eff5fc396a112986d8c736dba095701a02ffb9e72c21422b83e3596235
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919589"
---
# <a name="registering-network-providers-and-credential-managers"></a>Registrazione di provider di rete e gestori credenziali

Dopo aver creato il provider di rete o il gestore delle credenziali, è necessario registrarlo nel sistema. Questa operazione è necessaria in modo che la MPR sappia quali provider di rete sono installati. Quando viene avviata, la password MPR controlla il Registro di sistema e carica i provider di rete o i gestori delle credenziali trovati.

Poiché i provider di rete e i gestori delle credenziali sono correlati, vengono registrati nelle stesse sottochiavi del Registro di sistema. In realtà, anche le DLL del provider di rete possono essere gestori delle credenziali.

Per informazioni dettagliate sulle chiavi del Registro di sistema che è necessario creare per il provider di rete o gestione credenziali, vedere Chiavi del [Registro di sistema di autenticazione](authentication-registry-keys.md).

 

 



