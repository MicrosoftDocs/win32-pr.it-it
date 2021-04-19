---
description: Progettazione per la sicurezza
ms.assetid: 436f9d86-fbfa-4d5a-8580-fa1d4065c0aa
title: Progettazione per la sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69bc59b06cfcb7432806e548cc9808199b194e6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304952"
---
# <a name="designing-for-security"></a>Progettazione per la sicurezza

La strategia end-to-end per la sicurezza dipende ovviamente dal tipo di applicazione distribuita che si sta sviluppando. Di seguito sono riportati alcuni suggerimenti per risolvere i problemi di sicurezza rispetto alla logica dell'applicazione di livello intermedio:

-   Per migliorare l'efficienza e le prestazioni, è possibile eseguire l'autenticazione più vicina all'utente. Se l'applicazione prevede un'architettura da browser a business da logica a database, provare a eseguire il mapping dei client browser alle identità di dominio, eseguire l'applicazione COM+ in identità specifiche per ogni applicazione e configurare le tabelle nel livello dati in modo che siano accessibili solo da una particolare identità di applicazione. Questo scenario server attendibile è più scalabile e meno problematico rispetto all'uso del sistema DBMS per l'autenticazione.
-   Se si progetta un componente che verrà utilizzato in un'applicazione distribuita mediante la sicurezza basata sui ruoli, è possibile utilizzare la funzionalità di [sicurezza com+](com--security.md) . Questa funzionalità consente di chiamare metodi quali [**IObjectContext:: IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-iscallerinrole) e [**IObjectContext:: IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-issecurityenabled) per proteggere i blocchi di codice da accessi non autorizzati. È anche possibile usare il contesto di chiamata di sicurezza per ottenere informazioni sui chiamanti di un oggetto.
-   Se si progetta un componente che verrà utilizzato in un'applicazione distribuita senza utilizzare la protezione basata sui ruoli, la sicurezza viene controllata automaticamente solo a livello di processo. Le autorizzazioni di accesso al processo determinano a chi viene concesso l'accesso all'applicazione. Se è necessario un controllo più granulare sulle impostazioni di sicurezza a livello di processo o di interfaccia, utilizzare la funzionalità di sicurezza a livello di codice fornita da COM.
-   Se un componente che utilizza la sicurezza a livello di codice COM+ viene eseguito senza essere integrato in un'applicazione COM+, verranno generate eccezioni. Pertanto, se si desidera che tale componente venga integrato correttamente in un'applicazione che non fa parte dell'ambiente COM+, è necessario gestire tutte le eccezioni in modo appropriato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione per la disponibilità](designing-for-availability.md)
</dt> <dt>

[Progettazione per la distribuzione](designing-for-deployment.md)
</dt> <dt>

[Progettazione per la scalabilità](designing-for-scalability.md)
</dt> <dt>

[Sicurezza del componente a livello di codice](programmatic-component-security.md)
</dt> </dl>

 

 



