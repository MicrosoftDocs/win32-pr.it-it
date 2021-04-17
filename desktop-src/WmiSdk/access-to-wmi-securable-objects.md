---
description: WMI si basa su descrittori di sicurezza standard di Windows per controllare e proteggere l'accesso a oggetti a protezione diretta come gli spazi dei nomi WMI, le stampanti, i servizi e le applicazioni DCOM.
ms.assetid: 5893457d-3fc2-4d64-a6c2-0f410052ce52
ms.tgt_platform: multiple
title: Accesso a oggetti a protezione diretta WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad4ea78cd45d57856b0909283e7c2624fb26bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233476"
---
# <a name="access-to-wmi-securable-objects"></a>Accesso a oggetti a protezione diretta WMI

WMI si basa su [*descrittori di sicurezza*](/windows/desktop/SecGloss/s-gly) standard di Windows per controllare e proteggere l'accesso a oggetti a protezione diretta come gli spazi dei nomi WMI, le stampanti, i servizi e le applicazioni DCOM. Per ulteriori informazioni, vedere [accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md).

In questa sezione vengono trattati gli argomenti seguenti:

-   [Descrittori di sicurezza e SID](#security-descriptors-and-sids)
-   [Controllo di accesso](#access-control)
-   [Modifica della sicurezza dell'accesso](#changing-access-security)
-   [Argomenti correlati](#related-topics)

## <a name="security-descriptors-and-sids"></a>Descrittori di sicurezza e SID

WMI mantiene la sicurezza dell'accesso confrontando il [*token di accesso*](/windows/desktop/SecGloss/a-gly) dell'utente che tenta di accedere a un oggetto a protezione diretta con il descrittore di sicurezza dell'oggetto.

Quando un utente o un gruppo viene creato in un sistema, all'account viene assegnato un [*ID di sicurezza (SID)*](/windows/desktop/SecGloss/s-gly) . il SID garantisce che un account creato con lo stesso nome di un account eliminato in precedenza non erediti le impostazioni di sicurezza precedenti. Un token di accesso viene creato combinando il SID, l'elenco dei gruppi di cui l'utente è membro e l'elenco dei privilegi abilitati o disabilitati. Questi token vengono assegnati a tutti i processi e i thread di proprietà dell'utente.

## <a name="access-control"></a>Controllo di accesso

Quando l'utente desidera utilizzare un oggetto protetto, il token di accesso viene confrontato con l' [*elenco di controllo di accesso discrezionale (DACL)*](/windows/desktop/SecGloss/d-gly) nel descrittore di sicurezza dell'oggetto. L'elenco DACL contiene autorizzazioni denominate [*ACE (Access Control Entry)*](/windows/desktop/SecGloss/a-gly). Gli [*elenchi di controllo di accesso di sistema (SACL)*](/windows/desktop/SecGloss/s-gly) eseguono la stessa operazione degli elenchi DACL, ma possono generare eventi di controllo di sicurezza. A partire da Windows Vista, WMI può creare voci di controllo nel registro di sicurezza di Windows. Per ulteriori informazioni sul controllo in WMI, vedere [accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md).

Sia il DACL che il SACL sono costituiti da un elenco di voci ACE che descrivono quali utenti dispongono di diritti di accesso specifici, inclusa la scrittura nel repository WMI, l'accesso remoto e l'esecuzione e le autorizzazioni di accesso. WMI archivia questi ACL nel repository WMI.

Le voci ACE contengono tre tipi di livelli di accesso o diritti Concedi/nega: Consenti, nega per DACL e controllo di sistema (per SACL). Le voci ACE Deny precedono le voci ACE nell'elenco DACL o SACL. Quando si controllano i diritti di accesso dell'utente, WMI viene eseguito consecutivamente attraverso l'elenco di controllo di accesso fino a quando non viene trovata una voce ACE Allow applicabile al token di accesso richiedente. Le voci ACE rimanenti non vengono controllate dopo questo punto. Se non viene trovata alcuna voce ACE appropriata, l'accesso viene negato. Per ulteriori informazioni, vedere [Order of ACE in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl) e [Creating a DACL](/windows/desktop/SecBP/creating-a-dacl).

## <a name="changing-access-security"></a>Modifica della sicurezza dell'accesso

Con le autorizzazioni appropriate, è possibile modificare la sicurezza in un oggetto a protezione diretta con uno script o un'applicazione. È inoltre possibile modificare le impostazioni di sicurezza negli spazi dei nomi WMI utilizzando il [*controllo WMI*](gloss-w.md) oppure aggiungendo una stringa [SDDL (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) nel file di [*Managed Object Format (MOF)*](gloss-m.md) che definisce le classi per lo spazio dei nomi. Per ulteriori informazioni, vedere [accedere agli spazi dei nomi WMI](access-to-wmi-namespaces.md), [proteggere gli spazi dei nomi WMI](securing-wmi-namespaces.md)e [modificare la sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti descrittore di sicurezza WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Costanti di sicurezza WMI](wmi-security-constants.md)
</dt> <dt>

[Controllo dell'account utente e WMI](user-account-control-and-wmi.md)
</dt> <dt>

[Oggetti descrittore di sicurezza WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
