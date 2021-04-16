---
title: Modifica delle impostazioni predefinite di sicurezza per un computer
description: Modifica delle impostazioni predefinite di sicurezza per un computer
ms.assetid: c6d84375-59ea-42d5-87f9-af514b6f7d7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607e7a17e7db1f8852dff42e62384c730090bbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395266"
---
# <a name="modifying-the-security-defaults-for-a-computer"></a>Modifica delle impostazioni predefinite di sicurezza per un computer

Non è consigliabile modificare le impostazioni di sicurezza a livello di sistema, in quanto questa operazione influirà su tutte le applicazioni server COM che non impostano una sicurezza a livello di processo e potrebbe impedire il corretto funzionamento. Se si modificano le impostazioni di sicurezza a livello di sistema in modo da influire sulle impostazioni di sicurezza per una particolare applicazione COM, è necessario modificare le impostazioni di sicurezza a livello di processo per quella particolare applicazione COM. Per ulteriori informazioni sull'impostazione della sicurezza a livello di processo, vedere [impostazione Process-Wide sicurezza](setting-processwide-security.md).

Determinati valori del registro di sistema determinano le impostazioni di sicurezza per le applicazioni che non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). È possibile modificare queste impostazioni usando Dcomcnfg.exe.

Per altre informazioni, vedere i seguenti argomenti:

-   [Valori del registro di sistema per System-Wide sicurezza](registry-values-for-machine-wide-security.md)
-   [Impostazione della sicurezza System-Wide tramite DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione della sicurezza a livello di processo](setting-processwide-security.md)
</dt> <dt>

[Impostazione della sicurezza per le applicazioni COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




