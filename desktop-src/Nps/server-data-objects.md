---
title: Oggetti dati del server
description: L'API SDO (Server Data Objects) consente di configurare e amministrare a livello di codice un sistema che esegue Server dei criteri di rete.
ms.assetid: 9d159e15-f534-4ab1-9641-db70064beb51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d51c4a8b04b9da6994daa4941d255f0d74f68ea858d4a3909ed9ecc1ae28514
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128411"
---
# <a name="server-data-objects"></a>Oggetti dati del server

> [!Note]  
> Il servizio di autenticazione Internet (IAS) è stato rinominato Server dei criteri di rete (NPS) a partire Windows Server 2008. Il contenuto di questo argomento si applica sia a IAS che a Server dei criteri di rete. In tutto il testo, Server dei criteri di rete viene usato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.

 

L'API SDO (Server Data Objects) consente di configurare e amministrare a livello di codice un sistema che esegue Server dei criteri di rete. Usando SDO, uno sviluppatore può anche scrivere applicazioni che amministrano profili e criteri di accesso remoto. I profili e i criteri di accesso remoto vengono usati dal Servizio Routing e Accesso remoto (RRAS) e da Server dei criteri di rete per determinare se a un client remoto è consentito connettersi a un server di accesso alla rete (NAS).

L'API SDO è applicabile in qualsiasi ambiente che usa Criteri di rete o Criteri di accesso remoto.

Con l'API SDO, uno sviluppatore può modificare qualsiasi elemento della configurazione di Server dei criteri di rete accessibile tramite l'interfaccia utente di Server dei criteri di rete.

L'API SDO consente anche di impostare o recuperare uno dei valori accessibili tramite la pagina delle proprietà delle impostazioni di accesso remoto dell'utente.

L'API SDO è costituita da interfacce COM. Ognuna delle interfacce nell'API SDO eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) COM. **L'interfaccia IDispatch** consente agli sviluppatori di chiamare i metodi dell'interfaccia SDO da Visual Basic o da qualsiasi client di automazione, nonché da C/C++.

Gli sviluppatori possono anche chiamare l'API SDO da linguaggi di scripting come VBScript. Tuttavia, poiché VBScript è limitato all'uso di parametri di tipo VARIANT, non tutte le funzionalità di SDO sono disponibili.

## <a name="in-this-section"></a>Contenuto della sezione

[Overview](/windows/desktop/Nps/sdo-about-server-data-objects)

Informazioni generali sull'API Server Data Objects.

[Utilizzando](/windows/desktop/Nps/sdo-using-server-data-objects)

Codice di esempio che illustra come usare l'API Server Data Objects.

[Riferimento](/windows/desktop/Nps/sdo-server-data-objects-reference)

Documentazione dei tipi enumerati e delle interfacce che costituiscono l'API oggetti dati del server.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Server dei criteri di rete (servizio di autenticazione Internet)](portal.md)
</dt> <dt>

[Servizio di accesso remoto](/windows/desktop/RRAS/portal)
</dt> </dl>

 

 