---
description: È possibile controllare se uno spazio dei nomi figlio eredita il descrittore di sicurezza dello spazio dei nomi padre.
ms.assetid: d4fbd5af-69e2-4c60-907a-cb2a1506b7c9
ms.tgt_platform: multiple
title: Definizione dell'ereditarietà della sicurezza dello spazio dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e242299b78ede3ff49679305a97823bc022358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317554"
---
# <a name="establishing-inheritance-of-namespace-security"></a>Definizione dell'ereditarietà della sicurezza dello spazio dei nomi

È possibile controllare se uno spazio dei nomi figlio eredita il descrittore di sicurezza dello spazio dei nomi padre.

Gli spazi dei nomi WMI hanno descrittori di sicurezza che controllano chi può accedere allo spazio dei nomi e ai dati dello spazio dei nomi. Ogni descrittore di sicurezza dispone di un elenco di controllo di accesso discrezionale (DACL) e un elenco di controllo di accesso (SACL) di sicurezza. Questi elenchi contengono voci di controllo di accesso (ACE).

A seconda delle [**costanti del flag ACE dello spazio dei nomi**](namespace-ace-flag-constants.md) impostate, le autorizzazioni applicate a uno spazio dei nomi possono essere ereditate da tutti gli spazi dei nomi figlio dello spazio dei nomi. Uno spazio dei nomi figlio eredita il descrittore di sicurezza dello spazio dei nomi padre quando viene creato lo spazio dei nomi figlio se il **contenitore eredita il flag \_ \_ ACE** nel descrittore di sicurezza dello spazio dei nomi padre. Se il **contenitore \_ eredita \_ ACE \| No \_ essere propagati \_ eredita \_ ACE** è impostato, solo lo spazio dei nomi figlio eredita il descrittore di sicurezza, non gli spazi dei nomi nipoti. Gli spazi dei nomi figlio possono eseguire l'override delle autorizzazioni di sicurezza del padre chiamando i metodi della classe [**\_ \_ SystemSecurity**](--systemsecurity.md) per scrivere un nuovo descrittore di sicurezza. Non è possibile modificare le impostazioni di sicurezza predefinite. Per altre informazioni, vedere [impostazione dei descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md). Per ulteriori informazioni sugli elenchi DACL, vedere [Access Control List (ACL)](/windows/desktop/SecAuthZ/access-control-lists) e le [**costanti di tipo ACE dello spazio dei nomi**](namespace-ace-type-constants.md).

Si noti che le autorizzazioni predefinite non possono essere modificate. Inoltre, l'impostazione del flag di protezione **\_ \_ DACL se** durante l'impostazione del descrittore di sicurezza (SD) non viene utilizzata per aggiungere una SD specializzata a uno spazio dei nomi figlio. Per eseguire l'override di una SD ereditata, è sufficiente impostarne una nuova. Per ereditare tale SD in uno spazio dei nomi figlio, passare il **contenitore \_ ereditare \_** il flag ACE nel descrittore di sicurezza dello spazio dei nomi. Per ereditare solo l'elemento figlio e non i discendenti, passare `CONTAINER_INHERIT_ACE|NO_PROPOGATE_INHERIT_ACE`

.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione di descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

 
