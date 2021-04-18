---
description: L'accesso agli spazi dei nomi WMI e i relativi dati sono controllati dai descrittori di sicurezza.
ms.assetid: 3c2dc148-df6a-4bcb-a657-59b56c358d14
ms.tgt_platform: multiple
title: Sicurezza degli spazi dei nomi WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f605a6cd1136e70d6c5243b9e143fdb167d41808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309890"
---
# <a name="securing-wmi-namespaces"></a>Sicurezza degli spazi dei nomi WMI

L'accesso agli spazi dei nomi WMI e i relativi dati sono controllati dai [*descrittori di sicurezza*](gloss-s.md). È possibile proteggere i dati negli [*spazi dei nomi*](gloss-n.md) modificando il descrittore di sicurezza dello spazio dei nomi per controllare chi ha accesso ai dati e ai metodi. Per ulteriori informazioni, vedere [accesso a oggetti a protezione diretta WMI](access-to-wmi-securable-objects.md).


Negli argomenti seguenti viene descritta la sicurezza dello spazio dei nomi WMI e viene illustrato come controllare l'accesso agli spazi dei nomi.

<dl> <dt>

<span id="Access_to_WMI_Namespaces"></span><span id="access_to_wmi_namespaces"></span><span id="ACCESS_TO_WMI_NAMESPACES"></span>[Accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md)
</dt> <dd>

La sicurezza dello spazio dei nomi WMI si basa sugli [*ID di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) degli utenti di Windows standard e sugli elenchi di controllo di accesso. Gli amministratori e gli utenti dispongono di autorizzazioni predefinite diverse.

</dd> <dt>

<span id="Setting_Namespace_Security_Descriptors"></span><span id="setting_namespace_security_descriptors"></span><span id="SETTING_NAMESPACE_SECURITY_DESCRIPTORS"></span>[Impostazione di descrittori di sicurezza dello spazio dei nomi](setting-namespace-security-descriptors.md)
</dt> <dd>

Quando uno spazio dei nomi è presente nel repository WMI, è possibile modificare la sicurezza sullo spazio dei nomi utilizzando il controllo WMI o chiamando i metodi di [**\_ \_ SystemSecurity**](--systemsecurity.md).

</dd> <dt>

<span id="Requiring_an_Encrypted_Connection_to_a_Namespace"></span><span id="requiring_an_encrypted_connection_to_a_namespace"></span><span id="REQUIRING_AN_ENCRYPTED_CONNECTION_TO_A_NAMESPACE"></span>[Richiesta di una connessione crittografata a uno spazio dei nomi](requiring-an-encrypted-connection-to-a-namespace.md)
</dt> <dd>

Il qualificatore **RequiresEncryption** in uno spazio dei nomi richiede che lo script o l'applicazione client WMI usi il livello di autenticazione che crittografa le chiamate di procedura remota. È necessario crittografare le richieste di dati in ingresso e i callback asincroni.

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

[Oggetti descrittore di sicurezza WMI](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
