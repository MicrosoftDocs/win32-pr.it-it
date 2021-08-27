---
description: A partire da Windows Vista, molti oggetti a protezione diretta hanno metodi per ottenere o impostare il descrittore di sicurezza. Con le autorizzazioni appropriate, è possibile leggere o modificare i descrittori di sicurezza per gli oggetti a protezione diretta.
ms.assetid: da660e7e-f32d-4b7d-b979-f7b482a73fa2
ms.tgt_platform: multiple
title: Modifica della sicurezza degli accessi per gli oggetti a protezione diretta
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4cdaa948e6f0e695b3e77576b0a0726f0b38f3b649f005b42aa8e205c894db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050989"
---
# <a name="changing-access-security-on-securable-objects"></a>Modifica della sicurezza degli accessi per gli oggetti a protezione diretta

Stampanti, servizi, chiavi del Registro di sistema, applicazioni DCOM e spazi dei nomi WMI sono oggetti a protezione diretta. L'accesso agli oggetti a protezione diretta è protetto da [*descrittori di sicurezza*](/windows/desktop/SecGloss/s-gly), che specificano gli utenti che hanno accesso. A partire da Windows Vista, molti oggetti a protezione diretta hanno metodi per ottenere o impostare il descrittore di sicurezza. Con le autorizzazioni appropriate, è possibile leggere o modificare i descrittori di sicurezza per gli oggetti a protezione diretta. Usando questi metodi, è possibile controllare quali account utente o gruppi hanno accesso a una stampante, a un servizio, a uno spazio dei nomi WMI o a un altro oggetto. Per altre informazioni sui descrittori di sicurezza e sul relativo utilizzo in WMI, vedere [Accesso agli oggetti a protezione diretta WMI](access-to-wmi-securable-objects.md).

In questo argomento vengono illustrate le sezioni seguenti:

-   [Oggetti e metodi del descrittore di sicurezza](#objects-and-security-descriptor-methods)
-   [Conversione tra formati del descrittore di sicurezza](#converting-between-security-descriptor-formats)
-   [Problemi di sicurezza](#security-issues)
-   [Argomenti correlati](#related-topics)

## <a name="objects-and-security-descriptor-methods"></a>Oggetti e metodi del descrittore di sicurezza

L'elenco seguente contiene i metodi che gli oggetti a protezione diretta devono consentire di leggere o modificare il descrittore di sicurezza:

-   Spazi dei nomi WMI

    Un provider può stabilire la sicurezza che consente solo a determinati gruppi di accedere ai dati in uno spazio dei nomi WMI. La sicurezza dello spazio dei nomi è controllata dai metodi della [**\_ \_ classe SystemSecurity.**](--systemsecurity.md) A partire da Windows Vista, i [**metodi GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) e [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) restituiscono e scrivono [**\_ \_ oggetti SecurityDescriptor.**](--securitydescriptor.md) Per altre informazioni, vedere [Impostazione dei descrittori di sicurezza dello spazio dei nomi](setting-namespace-security-descriptors.md).

-   Chiavi del Registro di sistema

    A partire da Windows Vista, è possibile proteggere le chiavi del Registro di sistema in modo che non possano essere modificate da utenti non autorizzati. La [**classe StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) include i [**metodi GetSecurityDescriptor**](/previous-versions/windows/desktop/regprov/getsecuritydescriptor-method-in-class-stdregprov) e [**SetSecurityDescriptor.**](/previous-versions/windows/desktop/regprov/setsecuritydescriptor-method-in-class-stdregprov) Questi metodi restituiscono e scrivono [**oggetti \_ SecurityDescriptor Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)

-   Stampanti

    A partire Windows Vista, è possibile proteggere l'accesso alle istanze della [**classe \_ Printer Win32**](/windows/desktop/CIMWin32Prov/win32-printer) usando i [**metodi GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) [**e SetSecurityDescriptor.**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) Questi metodi restituiscono e scrivono [**oggetti \_ SecurityDescriptor Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)

-   Servizi

    A partire Windows Vista, è possibile proteggere l'accesso alle istanze della classe del servizio [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-service) usando i [**metodi GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-service) [**e SetSecurityDescriptor.**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-service) Questi metodi restituiscono e scrivono [**oggetti \_ SecurityDescriptor Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)

-   Applicazioni DCOM

    Le istanze dell'applicazione DCOM hanno diversi descrittori di sicurezza. A partire Windows Vista, usare i metodi della classe [**\_ DCOMApplicationSetting Win32**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting) per ottenere o modificare i vari descrittori di sicurezza. I descrittori di sicurezza vengono restituiti come istanze della [**classe \_ SecurityDescriptor Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)

    Per ottenere o modificare le autorizzazioni di configurazione, chiamare i [**metodi GetConfigurationSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting) [**o SetConfigurationSecurityDescriptor.**](/windows/desktop/CIMWin32Prov/setconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting)

    Per ottenere o modificare le autorizzazioni di accesso, chiamare i [**metodi GetAccessSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting) [**o SetAccessSecurityDescriptor.**](/windows/desktop/CIMWin32Prov/setaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting)

    Per ottenere o modificare le autorizzazioni di avvio e attivazione, chiamare i [**metodi GetLaunchSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getlaunchsecuritydescriptor-in-class-win32-dcomapplicationsetting) [**o SetLaunchSecurityDescriptor,**](/windows/desktop/CIMWin32Prov/setlaunchsecuritydescriptor-method-in-class-win32-dcomapplicationsetting)

-   File

    I [**metodi GetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/getsecuritydescriptor-method-in-class-win32-logicalfilesecuritysetting) [**e SetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/setsecuritydescriptor-method-in-class-win32-logicalfilesecuritysetting) sono nella [**classe \_ LogicalFileSecuritySetting Win32,**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) anziché nella [**classe CIM \_ DataFile.**](/windows/desktop/CIMWin32Prov/cim-datafile)

-   Condivisioni

    I [**metodi GetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/getsecuritydescriptor-method-in-class-win32-logicalsharesecuritysetting) [**e SetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/setsecuritydescriptor-method-in-class-win32-logicalsharesecuritysetting) sono nella [**classe \_ LogicalShareSecuritySetting Win32,**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) anziché nella [**classe Win32 \_ Share.**](/windows/desktop/CIMWin32Prov/win32-share)

> [!Note]  
> Quando non viene specificato un nuovo elenco di controllo di accesso di sicurezza [*(SACL)*](/windows/desktop/SecGloss/s-gly) in una chiamata a un metodo **SetSecurityDescriptor,** il SACL del descrittore di sicurezza nell'oggetto a protezione diretta di destinazione viene impostato su **NULL** in modo che l'impostazione SACL precedente non sia persistente.

 

## <a name="converting-between-security-descriptor-formats"></a>Conversione tra formati del descrittore di sicurezza

I descrittori di sicurezza sono matrici di byte binari complessi che in genere devono essere create e modificate in C++. Dopo aver usato uno dei metodi Get per ottenere il descrittore di sicurezza, la classe [**\_ Win32 SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) fornisce metodi che convertono i descrittori di sicurezza in [SDDL (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) o in istanze [**di \_ SecurityDescriptor Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)

È possibile modificare gli elenchi di controllo di accesso (ACL) più facilmente nelle [**istanze \_ di Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) o in SDDL. Per altre informazioni sulla struttura e sull'uso dei descrittori di sicurezza in WMI, vedere Oggetti descrittori [di sicurezza WMI](wmi-security-descriptor-objects.md).

In C++ o C# usare le funzioni di conversione per convertire i descrittori di sicurezza binari [in SDDL (Security Descriptor Definition Language).](/windows/desktop/SecAuthZ/security-descriptor-definition-language) Per modificare i valori del descrittore di sicurezza nelle applicazioni C++, usare [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

## <a name="security-issues"></a>Problemi di sicurezza

È consigliabile apportare modifiche ai descrittori di sicurezza con cautela in modo che la sicurezza dell'oggetto non venga compromessa. Tenere presente che l'ordine delle voci di controllo di accesso (ACE) in un elenco di controllo di accesso discrezionale (DACL) può influire sulla sicurezza dell'accesso. Per altre informazioni, vedere [Order of AEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti descrittori di sicurezza WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Classe helper del descrittore di sicurezza](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)
</dt> <dt>

[Procedure consigliate per la sicurezza](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[Gestione della sicurezza WMI](maintaining-wmi-security.md)
</dt> <dt>

[Controllo di accesso](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[Accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
