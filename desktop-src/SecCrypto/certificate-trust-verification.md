---
description: Deve esistere un trust tra il destinatario di un messaggio firmato e il firmatario del messaggio.
ms.assetid: 770e4674-8896-4062-a93a-a17bd30a9129
title: Verifica dell'attendibilità del certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9f88d9c944de8f1c6c40e7657c463740fa94fb94a55a8b9bb0f6e33c69d81f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126821"
---
# <a name="certificate-trust-verification"></a>Verifica dell'attendibilità del certificato

Deve esistere un trust tra il destinatario di un messaggio firmato e il firmatario del messaggio. Un metodo per stabilire questa attendibilità è tramite un certificato [*,*](../secgloss/c-gly.md)un documento elettronico che verifica che le entità o le persone siano chi dichiarano di essere. Un certificato viene rilasciato a un'entità da terze parti considerato attendibile da entrambe le altre parti. Ogni destinatario di un messaggio firmato decide quindi se l'autorità emittente del certificato del firmatario è attendibile. [*CryptoAPI ha*](../secgloss/c-gly.md) implementato una metodologia per consentire agli sviluppatori di applicazioni di creare applicazioni che verificano automaticamente i certificati in base a un elenco predefinito di certificati attendibili o [*radici*](../secgloss/r-gly.md). Questo elenco di entità attendibili (detti soggetti) è denominato [*elenco*](../secgloss/c-gly.md) di certificati attendibili (CTL).

L'esempio seguente di utilizzo di un CTL include un amministratore intranet (rete aziendale) che vuole controllare solo le origini esterne attendibili. In questo caso, l'amministratore può creare un elenco di certificati o radici attendibili, firmarlo e renderlo disponibile per tutti i client nella rete sotto forma di CTL. Un'applicazione progettata per usare questa funzionalità CryptoAPI accetterebbe quindi solo messaggi firmati o software scaricato firmato da entità nell'elenco.

Per un elenco di queste funzioni, vedere [Funzioni di verifica dei certificati](cryptography-functions.md).

 

 
