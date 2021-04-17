---
title: Oggetti dati del server
description: L'API SDO (Server Data Objects) consente di configurare e amministrare a livello di codice un sistema che esegue NPS.
ms.assetid: 9d159e15-f534-4ab1-9641-db70064beb51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eebd0f837f9a8a36af1eb9118189015e677e2af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300076"
---
# <a name="server-data-objects"></a>Oggetti dati del server

> [!Note]  
> Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008. Il contenuto di questo argomento si applica sia a IAS che a NPS. In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.

 

L'API SDO (Server Data Objects) consente di configurare e amministrare a livello di codice un sistema che esegue NPS. Usando SDO, uno sviluppatore può anche scrivere applicazioni che gestiscono profili e criteri di accesso remoto. I criteri e i profili di accesso remoto vengono utilizzati dal servizio Routing e accesso remoto (RRAS), nonché da server dei criteri di rete per determinare se un client remoto è autorizzato a connettersi a un server di accesso alla rete (NAS).

L'API SDO è applicabile in qualsiasi ambiente che utilizza criteri di accesso remoto o NPS.

Con l'API SDO, uno sviluppatore può modificare qualsiasi elemento della configurazione NPS accessibile tramite l'interfaccia utente del server dei criteri di server.

L'API SDO consente inoltre di impostare o recuperare i valori accessibili tramite la pagina delle proprietà impostazioni di connessione remota utente.

L'API SDO è costituita da interfacce COM. Ognuna delle interfacce nell'API SDO eredita dall'interfaccia COM [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . L'interfaccia **IDispatch** consente agli sviluppatori di chiamare i metodi dell'interfaccia SDO da Visual Basic o da qualsiasi client di automazione, nonché da C/C++.

Gli sviluppatori possono anche chiamare l'API SDO da linguaggi di scripting, ad esempio VBScript. Tuttavia, poiché VBScript è limitato all'uso dei soli parametri di tipo VARIANT, non tutte le funzionalità di SDO sono disponibili.

## <a name="in-this-section"></a>Contenuto della sezione

[Overview](/windows/desktop/Nps/sdo-about-server-data-objects)

Informazioni generali sull'API oggetti dati server.

[Usando](/windows/desktop/Nps/sdo-using-server-data-objects)

Codice di esempio che illustra come usare l'API di oggetti dati del server.

[Riferimento](/windows/desktop/Nps/sdo-server-data-objects-reference)

Documentazione dei tipi enumerati e delle interfacce che compongono l'API oggetti dati server.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Server dei criteri di rete (servizio di autenticazione Internet)](portal.md)
</dt> <dt>

[Servizio di accesso remoto](/windows/desktop/RRAS/portal)
</dt> </dl>

 

 