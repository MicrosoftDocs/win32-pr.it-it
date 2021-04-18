---
description: Deve esistere una relazione di trust tra il destinatario di un messaggio firmato e il firmatario del messaggio.
ms.assetid: 770e4674-8896-4062-a93a-a17bd30a9129
title: Verifica dell'attendibilità del certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b711e0a86dcc5ae9cdedea278d6a3a698dfd633
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315812"
---
# <a name="certificate-trust-verification"></a>Verifica dell'attendibilità del certificato

Deve esistere una relazione di trust tra il destinatario di un messaggio firmato e il firmatario del messaggio. Un metodo per stabilire questa relazione di trust è tramite un [*certificato*](../secgloss/c-gly.md), un documento elettronico che verifica che le entità o le persone siano quelle che attestano di essere. Un certificato viene rilasciato a un'entità da terze parti ritenuti attendibili da entrambe le altre parti. Quindi, ogni destinatario di un messaggio firmato decide se l'emittente del certificato del firmatario è attendibile. [*CryptoAPI*](../secgloss/c-gly.md) ha implementato una metodologia che consente agli sviluppatori di applicazioni di creare applicazioni che verificano automaticamente i certificati in base a un elenco predefinito di certificati o [*radici*](../secgloss/r-gly.md)attendibili. Questo elenco di entità attendibili (denominato subjects) è denominato [*elenco certificati attendibili*](../secgloss/c-gly.md) (CTL).

L'esempio seguente di utilizzo di un elenco di scopi consentiti riguarda un amministratore Intranet (Intra-Company Network) che desidera controllare solo quali origini esterne sono attendibili. In questo caso, l'amministratore può creare un elenco di certificati o radici attendibili, firmarlo e renderlo disponibile per tutti i client della rete sotto forma di CTL. Un'applicazione progettata per utilizzare questa funzionalità CryptoAPI accetta quindi solo i messaggi firmati o il software scaricato firmato da entità nell'elenco.

Per un elenco di queste funzioni, vedere [funzioni di verifica del certificato](cryptography-functions.md).

 

 
