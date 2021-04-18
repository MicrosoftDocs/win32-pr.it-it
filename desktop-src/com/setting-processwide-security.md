---
title: Impostazione della sicurezza Process-Wide
description: Esistono diversi modi per impostare la sicurezza a livello di processo.
ms.assetid: 596ba257-cbde-4243-aa29-78749304867a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc483bc6f52963eadc12891e657db1cbe51fb10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298983"
---
# <a name="setting-process-wide-security"></a>Impostazione della sicurezza Process-Wide

Esistono diversi modi per impostare la sicurezza a livello di processo. Il primo modo, usando lo strumento Dcomcnfg.exe, è più semplice perché non richiede alcuna programmazione. La seconda tecnica offre al programmatore maggiore controllo e richiede una chiamata a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Un'altra tecnica consiste nell'impostare la sicurezza a livello di processo nel registro di sistema tramite la chiave [AppID](appid-key.md) .

Per ulteriori informazioni su queste tecniche, vedere gli argomenti seguenti:

-   [Impostazione della sicurezza Process-Wide tramite DCOMCNFG](setting-processwide-security-using-dcomcnfg.md)
-   [Impostazione Process-Wide sicurezza con CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md)
-   [Impostazione della sicurezza Process-Wide tramite il registro di sistema](setting-processwide-security-through-the-registry.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione della sicurezza a livello di proxy di interfaccia](setting-security-at-the-interface-proxy-level.md)
</dt> <dt>

[Impostazione della sicurezza per le applicazioni COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




