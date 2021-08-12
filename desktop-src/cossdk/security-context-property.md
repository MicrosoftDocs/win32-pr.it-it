---
description: Proprietà del contesto di sicurezza
ms.assetid: 7ffae145-be13-4a2c-beb1-eaa1d11ad9a7
title: Proprietà del contesto di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31c537dc8c9b925fff5f7fc4f3da99fd361bfb02f61008b7d7af8a421b9f1d11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546822"
---
# <a name="security-context-property"></a>Proprietà del contesto di sicurezza

Come per ogni servizio automatico fornito da COM+, il controllo automatico dei ruoli si basa sulle proprietà incluse nel contesto dell'oggetto. La determinazione dell'esecuzione di un controllo di sicurezza in una chiamata a un componente si basa sulla proprietà di sicurezza nel contesto dell'oggetto creato quando viene creata un'istanza del componente configurato.

In genere non è necessario preoccuparsi di questa proprietà. viene usato direttamente da COM+, non dall'utente. Tuttavia, in alcune circostanze, potrebbe essere necessario un controllo rigoroso sull'attivazione di un oggetto. In questo caso, la proprietà di sicurezza può influire sul contesto in cui viene attivato l'oggetto. Ciò significa che se un oggetto ha una configurazione incompatibile con il contesto dell'autore, verrà attivato nel proprio contesto. La proprietà di sicurezza può influenzare questa impostazione, così come qualsiasi proprietà nel contesto dell'oggetto.

Se non si vuole che le impostazioni di sicurezza influenzino l'attivazione, è possibile scegliere solo il controllo di accesso a livello di processo. In questo modo viene eliminata la proprietà di sicurezza nel contesto dell'oggetto, anche se disabilita in modo efficace il controllo basato sui ruoli e rende non disponibili le informazioni sul contesto [delle chiamate di](security-call-context-information.md) sicurezza.

Per altre informazioni sui controlli di accesso a livello di processo, vedere [Limiti di sicurezza.](security-boundaries.md) Per informazioni su come impostare la sicurezza a livello di processo, vedere [Impostazione di un livello di sicurezza per i controlli di accesso.](setting-a-security-level-for-access-checks.md)

Per altre informazioni sul contesto dell'oggetto, vedere [Contesti](com--contexts.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione efficace dei ruoli](designing-roles-effectively.md)
</dt> <dt>

[Limiti di sicurezza](security-boundaries.md)
</dt> <dt>

[Informazioni sul contesto di chiamata di sicurezza](security-call-context-information.md)
</dt> <dt>

[Uso dei ruoli per l'autorizzazione client](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



