---
description: WMI si basa su Windows di sicurezza standard per controllare e proteggere l'accesso a oggetti a protezione diretta come spazi dei nomi WMI, stampanti, servizi e applicazioni DCOM.
ms.assetid: 5893457d-3fc2-4d64-a6c2-0f410052ce52
ms.tgt_platform: multiple
title: Accesso agli oggetti a protezione diretta WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e87274b7e911482adff72af9f20df8e0a869743a17f69bdb348542fcde148d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118109655"
---
# <a name="access-to-wmi-securable-objects"></a>Accesso agli oggetti a protezione diretta WMI

WMI si basa su Windows [](/windows/desktop/SecGloss/s-gly) di sicurezza standard per controllare e proteggere l'accesso a oggetti a protezione diretta come spazi dei nomi WMI, stampanti, servizi e applicazioni DCOM. Per altre informazioni, vedere [Accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md).

In questa sezione vengono trattati gli argomenti seguenti:

-   [Descrittori di sicurezza e SID](#security-descriptors-and-sids)
-   [Controllo di accesso](#access-control)
-   [Modifica della sicurezza degli accessi](#changing-access-security)
-   [Argomenti correlati](#related-topics)

## <a name="security-descriptors-and-sids"></a>Descrittori di sicurezza e SID

WMI mantiene la sicurezza dell'accesso confrontando il [*token di*](/windows/desktop/SecGloss/a-gly) accesso dell'utente che tenta di accedere a un oggetto a protezione diretta con il descrittore di sicurezza dell'oggetto.

Quando un utente o un gruppo viene creato in un sistema, all'account viene assegnato un ID di sicurezza [*(SID)*](/windows/desktop/SecGloss/s-gly) Il SID garantisce che un account creato con lo stesso nome di un account eliminato in precedenza non erediti le impostazioni di sicurezza precedenti. Un token di accesso viene creato combinando il SID, l'elenco dei gruppi di cui l'utente è membro e l'elenco dei privilegi abilitati o disabilitati. Questi token vengono assegnati a tutti i processi e i thread di proprietà dell'utente.

## <a name="access-control"></a>Controllo di accesso

Quando l'utente vuole usare un oggetto protetto, il token di accesso viene confrontato con l'elenco di controllo di accesso discrezionale [*(DACL)*](/windows/desktop/SecGloss/d-gly) nel descrittore di sicurezza dell'oggetto. L'elenco DACL contiene autorizzazioni denominate [*voci di controllo di accesso ( ACE).*](/windows/desktop/SecGloss/a-gly) Gli elenchi di controllo di accesso di sistema [*(SACL)*](/windows/desktop/SecGloss/s-gly) esereranno le stesse operazioni degli elenchi di controllo di accesso di sistema, ma possono generare eventi di controllo di sicurezza. A partire da Windows Vista, WMI può creare voci di controllo nel log Sicurezza di Windows dati. Per altre informazioni sul controllo in WMI, vedere [Accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md).

Sia l'elenco DACL che l'elenco SACL sono costituiti da un elenco di voci di controllo di accesso che descrivono quali utenti dispongono di diritti di accesso specifici, tra cui la scrittura nel repository WMI, l'accesso remoto e l'esecuzione e le autorizzazioni di accesso. WMI archivia questi ACL nel repository WMI.

Le ACE contengono tre tipi di livelli di accesso o diritti di concessione/negazione: allow, deny per DACL e controllo di sistema (per SACL). Le ACE Di negazione precedono le ACE consentite nell'elenco DACL o sacl. Quando si controllano i diritti di accesso utente, WMI viene eseguito in modo consecutivo nell'elenco di controllo di accesso finché non trova una voce ACE consentita che si applica al token di accesso richiedente. Le ACE rimanenti non vengono controllate dopo questo punto. Se non viene trovata alcuna ACE consentita appropriata, l'accesso viene negato. Per altre informazioni, vedere [Order of ACe in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl) e [Creating a DACL](/windows/desktop/SecBP/creating-a-dacl).

## <a name="changing-access-security"></a>Modifica della sicurezza degli accessi

Con le autorizzazioni appropriate, è possibile modificare la sicurezza in un oggetto a protezione diretta con uno script o un'applicazione. È anche possibile modificare le impostazioni di sicurezza negli spazi dei nomi [*WMI*](gloss-w.md) usando il controllo WMI o aggiungendo una stringa [SDDL (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) nel file [*Managed Object Format (MOF)*](gloss-m.md) che definisce le classi per lo spazio dei nomi. Per altre informazioni, vedere Accesso agli spazi dei nomi [WMI](access-to-wmi-namespaces.md), [Protezione](securing-wmi-namespaces.md)degli spazi dei nomi WMI e Modifica della sicurezza degli [accessi per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti descrittori di sicurezza WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Costanti di sicurezza WMI](wmi-security-constants.md)
</dt> <dt>

[Controllo dell'account utente e WMI](user-account-control-and-wmi.md)
</dt> <dt>

[Oggetti descrittori di sicurezza WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
