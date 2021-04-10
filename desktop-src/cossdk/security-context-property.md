---
description: Proprietà del contesto di sicurezza
ms.assetid: 7ffae145-be13-4a2c-beb1-eaa1d11ad9a7
title: Proprietà del contesto di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b061ef7c0d0d0c146b626c11fd550c48ab488a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225773"
---
# <a name="security-context-property"></a>Proprietà del contesto di sicurezza

Come per ogni servizio automatico fornito da COM+, il controllo automatico dei ruoli è basato sulle proprietà incluse nel contesto dell'oggetto. Per determinare se è necessario eseguire un controllo di sicurezza in una chiamata a un componente, si basa sulla proprietà di sicurezza nel contesto dell'oggetto creato quando viene creata un'istanza del componente configurato.

In genere non è necessario preoccuparsi di questa proprietà. viene utilizzato direttamente da COM+, non dall'utente. In alcuni casi, tuttavia, potrebbe essere necessario un controllo rigoroso sull'attivazione di un oggetto. In questo caso, la proprietà di sicurezza può influire sul contesto in cui è attivato l'oggetto. Ovvero, se un oggetto dispone di una configurazione incompatibile con il contesto del relativo creatore, verrà attivata nel relativo contesto. La proprietà di sicurezza può influenzare questo, così come qualsiasi proprietà del contesto dell'oggetto.

Se non si vuole che le impostazioni di sicurezza influiscano sull'attivazione, è possibile scegliere solo il controllo di accesso a livello di processo. In questo modo viene eliminata la proprietà di sicurezza nel contesto dell'oggetto, anche se il controllo basato sui ruoli viene disabilitato e le [informazioni sul contesto delle chiamate di sicurezza](security-call-context-information.md) non sono disponibili.

Per ulteriori informazioni sui controlli di accesso a livello di processo, vedere [limiti di sicurezza](security-boundaries.md). Per informazioni su come impostare la sicurezza a livello di processo, vedere [impostazione di un livello di sicurezza per i controlli di accesso](setting-a-security-level-for-access-checks.md).

Per ulteriori informazioni sul contesto dell'oggetto, vedere [contesti](com--contexts.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione efficace dei ruoli](designing-roles-effectively.md)
</dt> <dt>

[Limiti di sicurezza](security-boundaries.md)
</dt> <dt>

[Informazioni sul contesto delle chiamate di sicurezza](security-call-context-information.md)
</dt> <dt>

[Utilizzo dei ruoli per l'autorizzazione client](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



