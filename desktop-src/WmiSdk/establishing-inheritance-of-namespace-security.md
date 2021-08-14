---
description: È possibile controllare se uno spazio dei nomi figlio eredita il descrittore di sicurezza dello spazio dei nomi padre.
ms.assetid: d4fbd5af-69e2-4c60-907a-cb2a1506b7c9
ms.tgt_platform: multiple
title: Definizione dell'ereditarietà della sicurezza dello spazio dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951bd5a2a14aa0a62620090d07df9bc56e8a0832674f2c1eee84369f4e2b4dae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119411911"
---
# <a name="establishing-inheritance-of-namespace-security"></a>Definizione dell'ereditarietà della sicurezza dello spazio dei nomi

È possibile controllare se uno spazio dei nomi figlio eredita il descrittore di sicurezza dello spazio dei nomi padre.

Gli spazi dei nomi WMI hanno descrittori di sicurezza che controllano chi può accedere allo spazio dei nomi e ai dati dello spazio dei nomi. Ogni descrittore di sicurezza ha un elenco di controllo di accesso discrezionale (DACL) e un elenco di controllo di accesso di sicurezza (SACL). Questi elenchi contengono voci di controllo di accesso (ACE).

A seconda delle costanti del [**flag ACE**](namespace-ace-flag-constants.md) dello spazio dei nomi impostate, le autorizzazioni applicate a uno spazio dei nomi possono essere ereditate da tutti gli spazi dei nomi figlio di tale spazio dei nomi. Uno spazio dei nomi figlio eredita il descrittore di sicurezza dello spazio dei nomi padre quando lo spazio dei nomi figlio viene creato se il flag **\_ CONTAINER INHERIT \_ ACE** si trova nel descrittore di sicurezza dello spazio dei nomi padre. Se **l'opzione CONTAINER \_ INHERIT \_ ACE NO \| \_ PROPOGATE \_ INHERIT \_ ACE** è impostata, solo lo spazio dei nomi figlio eredita il descrittore di sicurezza, non gli spazi dei nomi nipote. Gli spazi dei nomi figlio possono eseguire l'override delle autorizzazioni di sicurezza dell'elemento padre chiamando i metodi della [**\_ \_ classe SystemSecurity**](--systemsecurity.md) per scrivere un nuovo descrittore di sicurezza. Le impostazioni di sicurezza predefinite non possono essere modificate. Per altre informazioni, vedere [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md)( Impostazione dei descrittori di sicurezza diPace ). Per altre informazioni sui daCL, vedere Elenchi di controllo di accesso [(ACL)](/windows/desktop/SecAuthZ/access-control-lists) e Costanti del tipo [**ACE dello**](namespace-ace-type-constants.md)spazio dei nomi .

Si noti che le autorizzazioni predefinite non possono essere modificate. Inoltre, l'impostazione del flag **\_ EDIZIONE STANDARD DACL \_ PROTECTED** durante l'impostazione del descrittore di sicurezza (SD) non viene usata per aggiungere un SD specializzato a uno spazio dei nomi figlio. Per eseguire l'override di un'istanza di SD ereditata, è sufficiente impostarne una nuova. Per ereditare tale SD in uno spazio dei nomi figlio, passare il flag **\_ CONTAINER INHERIT \_ ACE** nel descrittore di sicurezza dello spazio dei nomi. Per ereditare solo per l'elemento figlio e non per i discendenti, passare `CONTAINER_INHERIT_ACE|NO_PROPOGATE_INHERIT_ACE`

.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione dei descrittori di sicurezza di Namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

 
