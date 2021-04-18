---
description: A partire da Windows Vista, molti oggetti a protezione diretta dispongono di metodi per ottenere o impostare il descrittore di sicurezza. Con le autorizzazioni appropriate, è possibile leggere o modificare i descrittori di sicurezza per gli oggetti a protezione diretta.
ms.assetid: da660e7e-f32d-4b7d-b979-f7b482a73fa2
ms.tgt_platform: multiple
title: Modifica della sicurezza di accesso per gli oggetti a protezione diretta
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9682c259fc2f7e45409f7ddcaaa95dac2cba1b54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313204"
---
# <a name="changing-access-security-on-securable-objects"></a>Modifica della sicurezza di accesso per gli oggetti a protezione diretta

Stampanti, servizi, chiavi del registro di sistema, applicazioni DCOM e spazi dei nomi WMI sono oggetti a protezione diretta. L'accesso agli oggetti a protezione diretta è protetto da [*descrittori di sicurezza*](/windows/desktop/SecGloss/s-gly), che specificano gli utenti che dispongono dell'accesso. A partire da Windows Vista, molti oggetti a protezione diretta dispongono di metodi per ottenere o impostare il descrittore di sicurezza. Con le autorizzazioni appropriate, è possibile leggere o modificare i descrittori di sicurezza per gli oggetti a protezione diretta. Utilizzando questi metodi, è possibile controllare gli account utente o i gruppi che hanno accesso a una stampante, un servizio, uno spazio dei nomi WMI o un altro oggetto. Per ulteriori informazioni sui descrittori di sicurezza e il relativo utilizzo in WMI, vedere [accesso a oggetti a protezione diretta WMI](access-to-wmi-securable-objects.md).

Le sezioni seguenti sono illustrate in questo argomento:

-   [Oggetti e metodi del descrittore di sicurezza](#objects-and-security-descriptor-methods)
-   [Conversione tra formati di descrittore di sicurezza](#converting-between-security-descriptor-formats)
-   [Problemi di sicurezza](#security-issues)
-   [Argomenti correlati](#related-topics)

## <a name="objects-and-security-descriptor-methods"></a>Oggetti e metodi del descrittore di sicurezza

Nell'elenco seguente sono inclusi i metodi che gli oggetti a protezione diretta devono consentire di leggere o modificare il descrittore di sicurezza:

-   Spazi dei nomi WMI

    Un provider può stabilire la sicurezza che consente solo a determinati gruppi di accedere ai dati in uno spazio dei nomi WMI. La sicurezza dello spazio dei nomi è controllata dai metodi della classe [**\_ \_ SystemSecurity**](--systemsecurity.md) . A partire da Windows Vista, i metodi [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) e [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) restituiscono e scrivono oggetti [**\_ \_ securityDescriptor**](--securitydescriptor.md) . Per ulteriori informazioni, vedere [impostazione di descrittori di sicurezza dello spazio dei nomi](setting-namespace-security-descriptors.md).

-   Chiavi del Registro di sistema

    A partire da Windows Vista, è possibile proteggere le chiavi del registro di sistema in modo che non possano essere modificate dagli utenti non autorizzati. La classe [**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) include i metodi [**GetSecurityDescriptor**](/previous-versions/windows/desktop/regprov/getsecuritydescriptor-method-in-class-stdregprov) e [**SetSecurityDescriptor**](/previous-versions/windows/desktop/regprov/setsecuritydescriptor-method-in-class-stdregprov) . Questi metodi restituiscono e scrivono oggetti [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .

-   Stampanti

    A partire da Windows Vista, è possibile proteggere l'accesso alle istanze della classe [**\_ Printer Win32**](/windows/desktop/CIMWin32Prov/win32-printer) usando i metodi [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) e [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) . Questi metodi restituiscono e scrivono oggetti [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .

-   Servizi

    A partire da Windows Vista, è possibile proteggere l'accesso alle istanze della classe del [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service) usando i metodi [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-service) e [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-service) . Questi metodi restituiscono e scrivono oggetti [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .

-   Applicazioni DCOM

    Le istanze dell'applicazione DCOM hanno diversi descrittori di sicurezza. A partire da Windows Vista, utilizzare i metodi della classe [**Win32 \_ DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting) per ottenere o modificare i vari descrittori di sicurezza. I descrittori di sicurezza vengono restituiti come istanze della classe [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .

    Per ottenere o modificare le autorizzazioni di configurazione, chiamare i metodi [**GetConfigurationSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting) o [**SetConfigurationSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting) .

    Per ottenere o modificare le autorizzazioni di accesso, chiamare i metodi [**GetAccessSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting) o [**SetAccessSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting) .

    Per ottenere o modificare le autorizzazioni di avvio e attivazione, chiamare i metodi [**GetLaunchSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getlaunchsecuritydescriptor-in-class-win32-dcomapplicationsetting) o [**SetLaunchSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setlaunchsecuritydescriptor-method-in-class-win32-dcomapplicationsetting) .

-   File

    I metodi [**GetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/getsecuritydescriptor-method-in-class-win32-logicalfilesecuritysetting) e [**SetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/setsecuritydescriptor-method-in-class-win32-logicalfilesecuritysetting) si trovano nella [**classe \_ LogicalFileSecuritySetting di Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) , anziché nella classe del file di [**\_ DataFile CIM**](/windows/desktop/CIMWin32Prov/cim-datafile) .

-   Condivisioni

    I metodi [**GetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/getsecuritydescriptor-method-in-class-win32-logicalsharesecuritysetting) e [**SetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/setsecuritydescriptor-method-in-class-win32-logicalsharesecuritysetting) si trovano nella [**classe \_ LogicalShareSecuritySetting di Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) , anziché nella classe [**della \_ condivisione Win32**](/windows/desktop/CIMWin32Prov/win32-share) .

> [!Note]  
> Quando un nuovo [*elenco di controllo di accesso (SACL) di sicurezza*](/windows/desktop/SecGloss/s-gly) non viene specificato in una chiamata a un metodo **SETSECURITYDESCRIPTOR** , il SACL del descrittore di sicurezza nell'oggetto a protezione diretta di destinazione viene impostato su **null** in modo che l'impostazione SACL precedente non sia persistente.

 

## <a name="converting-between-security-descriptor-formats"></a>Conversione tra formati di descrittore di sicurezza

I descrittori di sicurezza sono matrici di byte binarie complesse che devono essere in genere create e modificate in C++. Dopo aver usato uno dei metodi get per ottenere il descrittore di sicurezza, la classe [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) fornisce metodi che convertono i descrittori di sicurezza in un [linguaggio SDDL (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) o in istanze [**\_ securityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .

È possibile modificare più facilmente gli elenchi di controllo di accesso (ACL) nelle istanze [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) o in SDDL. Per ulteriori informazioni sulla struttura e sull'utilizzo dei descrittori di sicurezza in WMI, vedere [oggetti del descrittore di sicurezza WMI](wmi-security-descriptor-objects.md).

In C++ o C# usare le funzioni di conversione per convertire i descrittori di sicurezza binari in [SDDL (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language). Per modificare i valori dei descrittori di sicurezza nelle applicazioni C++, usare [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor ha**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

## <a name="security-issues"></a>Problemi di sicurezza

È consigliabile che le modifiche ai descrittori di sicurezza vengano eseguite con grande cautela, in modo che la sicurezza dell'oggetto non venga compromessa. Tenere presente che l'ordine delle voci di controllo di accesso (ACE) in un elenco di controllo di accesso discrezionale (DACL) può influire sulla sicurezza dell'accesso. Per ulteriori informazioni, vedere [Order of ACE in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti descrittore di sicurezza WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Classe helper del descrittore di sicurezza](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)
</dt> <dt>

[Procedure di sicurezza consigliate](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[Gestione della sicurezza WMI](maintaining-wmi-security.md)
</dt> <dt>

[Controllo di accesso](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[Accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
