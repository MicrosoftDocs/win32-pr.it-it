---
description: Sia le applicazioni C++ che gli script in esecuzione con un account amministratore completo possono modificare un descrittore di sicurezza dello spazio dei nomi.
ms.assetid: d3e56b30-d5a8-446a-89aa-645b44a75af6
ms.tgt_platform: multiple
title: Impostazione dei descrittori di sicurezza dello spazio dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccc112376a960c3760bc51450cc30b8da3a38c24fa52e985321b2662ae319a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050299"
---
# <a name="setting-namespace-security-descriptors"></a>Impostazione dei descrittori di sicurezza dello spazio dei nomi

Sia le applicazioni C++ che gli script in esecuzione con un account amministratore completo possono modificare un descrittore di sicurezza dello spazio dei nomi.

## <a name="namespace-security-descriptors"></a>Descrittori di sicurezza dello spazio dei nomi

Ogni spazio dei nomi WMI ha un [*descrittore*](/windows/desktop/SecGloss/s-gly)di sicurezza , che consente a ogni spazio dei nomi di avere impostazioni di sicurezza univoche che determinano chi ha accesso ai dati e ai metodi dello spazio dei nomi. Per altre informazioni sulla sicurezza dell'accesso WMI, vedere [Accesso a oggetti a protezione diretta WMI.](access-to-wmi-securable-objects.md) [L'accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md) descrive le impostazioni di sicurezza predefinite per gli spazi dei nomi WMI e il controllo di sicurezza in WMI.

È possibile impostare le autorizzazioni dell'account per ogni spazio dei nomi WMI nel repository WMI (CIM) nei modi seguenti:

-   Quando lo spazio dei nomi viene creato nel file MOF. Per altre informazioni, vedere [Impostazione della sicurezza dello spazio dei nomi quando viene creato lo spazio dei nomi.](setting-namespace-security-when-the-namespace-is-created.md)
-   Manualmente, usando il controllo WMI. Per altre informazioni, vedere [Impostazione della sicurezza dello spazio dei nomi con il controllo WMI.](setting-namespace-security-with-the-wmi-control.md)
-   A livello di codice, chiamando i metodi della [**\_ \_ classe SystemSecurity.**](--systemsecurity.md)

I metodi seguenti [**\_ \_ dell'oggetto SystemSecurity**](--systemsecurity.md) associato a ogni spazio dei nomi consentono di leggere o modificare la sicurezza in uno spazio dei nomi.

<dl> <dt>

<span id="GetCallerAccessRights"></span><span id="getcalleraccessrights"></span><span id="GETCALLERACCESSRIGHTS"></span>[**GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md)
</dt> <dd>

Imposta il *parametro rights* come bitmap con ogni bit corrispondente a un diritto di accesso.

</dd> <dt>

<span id="GetSD"></span><span id="getsd"></span><span id="GETSD"></span>[**GetSD**](--systemsecurity-getsd.md)
</dt> <dd>

Ottiene il descrittore di sicurezza per lo spazio dei nomi a cui è connesso l'utente. Questo metodo restituisce un descrittore di sicurezza in formato matrice di byte binario. Se si scrive uno script, usare il [**metodo GetSecurityDescriptor.**](getsecuritydescriptor-method-in-class---systemsecurity-.md)

</dd> <dt>

<span id="SetSD"></span><span id="setsd"></span><span id="SETSD"></span>[**SetSD**](--systemsecurity-setsd.md)
</dt> <dd>

Imposta il descrittore di sicurezza (SD) per lo spazio dei nomi a cui è connesso un utente. Questo metodo richiede un descrittore di sicurezza in formato matrice di byte binario. Se si scrive uno script, usare il [**metodo SetSecurityDescriptor.**](setsecuritydescriptor-method-in-class---systemsecurity.md)

</dd> <dt>

<span id="GetSecurityDescriptor"></span><span id="getsecuritydescriptor"></span><span id="GETSECURITYDESCRIPTOR"></span>[**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md)
</dt> <dd>

Ottiene il descrittore di sicurezza che controlla l'accesso allo spazio dei nomi WMI associato all'istanza di [**\_ \_ SystemSecurity.**](--systemsecurity.md) Il descrittore di sicurezza viene restituito come istanza di [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).

</dd> <dt>

<span id="SetSecurityDescriptor"></span><span id="setsecuritydescriptor"></span><span id="SETSECURITYDESCRIPTOR"></span>[**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md)
</dt> <dd>

Scrive una versione aggiornata del descrittore di sicurezza che controlla l'accesso alla stampante. Il descrittore di sicurezza è rappresentato da un'istanza di [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).

</dd> <dt>

<span id="Get9XUserList"></span><span id="get9xuserlist"></span><span id="GET9XUSERLIST"></span>[**Get9XUserList**](--systemsecurity-get9xuserlist.md)
</dt> <dd>

Ottiene i diritti di accesso remoto per un elenco di singoli utenti in computer che eseguono versioni obsolete di Windows, in cui il controllo di accesso tramite Windows descrittori di sicurezza non è disponibile.

</dd> <dt>

<span id="Set9XUserList"></span><span id="set9xuserlist"></span><span id="SET9XUSERLIST"></span>[**Set9XUserList**](--systemsecurity-set9xuserlist.md)
</dt> <dd>

Imposta i diritti di accesso remoto per un elenco di singoli utenti nei computer che eseguono versioni obsolete di Windows, in cui il controllo di accesso tramite Windows descrittori di sicurezza non è disponibile.

</dd> </dl>

Se si scrivono script, usare [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) e [**SetSecurityDescriptor.**](setsecuritydescriptor-method-in-class---systemsecurity.md) È possibile usare i metodi della [**classe \_ SecurityDescriptorHelper Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) per modificare i descrittori di sicurezza.

Se si programma in C++, è possibile modificare il descrittore di sicurezza binario usando [SDDL (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language)e i metodi di conversione [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

Tenere presente che, a partire da Windows Vista, Controllo [dell'account](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) utente influisce sull'accesso ai dati WMI e su ciò che può essere configurato con il [*controllo WMI*](gloss-w.md). Per altre informazioni, vedere [Controllo dell'account utente e WMI.](user-account-control-and-wmi.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Protezione degli spazi dei nomi WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Costanti di sicurezza WMI](wmi-security-constants.md)
</dt> <dt>

[Accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md)
</dt> <dt>

[Oggetti descrittore di sicurezza WMI](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
