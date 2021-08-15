---
description: L'accesso agli spazi dei nomi WMI e ai relativi dati è controllato dai descrittori di sicurezza.
ms.assetid: 3c2dc148-df6a-4bcb-a657-59b56c358d14
ms.tgt_platform: multiple
title: Protezione degli spazi dei nomi WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3cdf2b6e5c5cf035fed70e3e0dd949a812505f1f1ded8f1599043cdd75ba4c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992371"
---
# <a name="securing-wmi-namespaces"></a>Protezione degli spazi dei nomi WMI

L'accesso agli spazi dei nomi WMI e ai relativi dati è controllato [*dai descrittori di sicurezza*](gloss-s.md). È possibile proteggere i dati negli spazi [*dei*](gloss-n.md) nomi modificando il descrittore di sicurezza dello spazio dei nomi per controllare chi può accedere ai dati e ai metodi. Per altre informazioni, vedere [Accesso agli oggetti a protezione diretta WMI.](access-to-wmi-securable-objects.md)


Gli argomenti seguenti descrivono la sicurezza dello spazio dei nomi WMI e come controllare l'accesso agli spazi dei nomi.

<dl> <dt>

<span id="Access_to_WMI_Namespaces"></span><span id="access_to_wmi_namespaces"></span><span id="ACCESS_TO_WMI_NAMESPACES"></span>[Accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md)
</dt> <dd>

La sicurezza dello spazio dei nomi WMI si basa su Windows [*id*](/windows/desktop/SecGloss/s-gly) di sicurezza utente (SID) e elenchi di controllo di accesso. Gli amministratori e gli utenti hanno autorizzazioni predefinite diverse.

</dd> <dt>

<span id="Setting_Namespace_Security_Descriptors"></span><span id="setting_namespace_security_descriptors"></span><span id="SETTING_NAMESPACE_SECURITY_DESCRIPTORS"></span>[Impostazione dei descrittori di sicurezza dello spazio dei nomi](setting-namespace-security-descriptors.md)
</dt> <dd>

Dopo aver presente uno spazio dei nomi nel repository WMI, è possibile modificare la sicurezza per lo spazio dei nomi usando il controllo WMI o chiamando i metodi di [**\_ \_ SystemSecurity**](--systemsecurity.md).

</dd> <dt>

<span id="Requiring_an_Encrypted_Connection_to_a_Namespace"></span><span id="requiring_an_encrypted_connection_to_a_namespace"></span><span id="REQUIRING_AN_ENCRYPTED_CONNECTION_TO_A_NAMESPACE"></span>[Richiesta di una connessione crittografata a uno spazio dei nomi](requiring-an-encrypted-connection-to-a-namespace.md)
</dt> <dd>

Il **qualificatore RequiresEncryption** in uno spazio dei nomi richiede che lo script o l'applicazione client WMI usi il livello di autenticazione che crittografa le chiamate di procedura remota. Sia le richieste di dati in ingresso che i callback asincroni devono essere crittografati.

</dd> <dt>

<span id="Establishing_Inheritance_of_Namespace_Security"></span><span id="establishing_inheritance_of_namespace_security"></span><span id="ESTABLISHING_INHERITANCE_OF_NAMESPACE_SECURITY"></span>[Definizione dell'ereditarietà della sicurezza dello spazio dei nomi](establishing-inheritance-of-namespace-security.md)
</dt> <dd>

È possibile controllare se uno spazio dei nomi figlio eredita il descrittore di sicurezza dello spazio dei nomi padre.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione della sicurezza WMI](maintaining-wmi-security.md)
</dt> <dt>

[Connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Creazione di uno spazio dei nomi con l'API WMI](creating-a-namespace-with-the-wmi-api.md)
</dt> <dt>

[Oggetti descrittori di sicurezza WMI](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
