---
description: WMI dispone di oggetti e metodi che consentono di leggere e modificare i descrittori di sicurezza per determinare chi ha accesso agli oggetti a protezione diretta.
ms.assetid: ce4b7c9e-2c16-40d4-8839-76e69ddb2d8c
ms.tgt_platform: multiple
title: Oggetti descrittore di sicurezza WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc315e955c2d449d0dea0db97684cc352257cd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571726"
---
# <a name="wmi-security-descriptor-objects"></a>Oggetti descrittore di sicurezza WMI

WMI dispone di oggetti e metodi che consentono di leggere e modificare i descrittori di sicurezza per determinare chi ha accesso agli oggetti a protezione diretta.

-   [Ruolo dei descrittori di sicurezza](#the-role-of-security-descriptors)
-   [Controllo di accesso e oggetti di sicurezza WMI](#access-control-and-wmi-security-objects)
-   [\_Oggetto securityDescriptor Win32](/windows)
-   [DACL e SACL](#dacl-and-sacl)
-   [\_ACE Win32, \_ trustee Win32, \_ SID Win32](/windows)
-   [Esempio: controllo dell'accesso alle stampanti](#example-checking-who-has-access-to-printers)
-   [Argomenti correlati](#related-topics)

## <a name="the-role-of-security-descriptors"></a>Ruolo dei descrittori di sicurezza

I descrittori di sicurezza definiscono gli attributi di sicurezza degli oggetti a protezione diretta, ad esempio file, chiavi del registro di sistema, spazi dei nomi WMI, stampanti, servizi o condivisioni. Un descrittore di sicurezza contiene informazioni sul proprietario e sul gruppo primario di un oggetto. Un provider può confrontare il descrittore di sicurezza delle risorse con l'identità di un utente richiedente e determinare se l'utente ha il diritto di accedere alla risorsa richiesta da un utente. Per ulteriori informazioni, vedere [accesso a oggetti a protezione diretta WMI](access-to-wmi-securable-objects.md).

Alcuni metodi WMI, ad esempio [**getsd**](--systemsecurity-getsd.md), restituiscono un descrittore di sicurezza nel formato della matrice di byte binaria. A partire da Windows Vista, utilizzare i metodi della classe [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) per convertire un descrittore di sicurezza binario in un'istanza di [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor), che può essere modificato più facilmente. Per ulteriori informazioni, vedere [modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md).

## <a name="access-control-and-wmi-security-objects"></a>Controllo di accesso e oggetti di sicurezza WMI

Di seguito è riportato un elenco di oggetti di sicurezza WMI:

-   [**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
-   [**\_ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
-   [**\_Trustee Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
-   [**\_SID Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-sid)

Nel diagramma seguente vengono illustrate le relazioni tra gli oggetti di sicurezza WMI.

![relazioni tra oggetti di sicurezza WMI](images/security-descriptor.png)

Per ulteriori informazioni sul ruolo di sicurezza dell'accesso, vedere [procedure](/windows/desktop/SecBP/best-practices-for-the-security-apis)consigliate per la sicurezza, [gestione della sicurezza WMI](maintaining-wmi-security.md)e [controllo degli accessi](/windows/desktop/SecAuthZ/access-control).

## <a name="win32_securitydescriptor-object"></a>\_Oggetto securityDescriptor Win32

Nella tabella seguente sono elencate le proprietà della classe [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .



| Proprietà         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ControlFlags** | Set di bit di controllo che qualificano il significato di una SD o dei singoli membri. Per ulteriori informazioni sull'impostazione dei valori di bit **ControlFlags** , vedere [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).<br/>                                                                                                                                                                      |
| **DACL**         | [Elenco di controllo di accesso discrezionale (ACL)](/windows/desktop/SecAuthZ/access-control-lists) di utenti e gruppi e dei rispettivi diritti di accesso a un oggetto protetto. Questa proprietà contiene una matrice di [**istanze \_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) che rappresentano le [voci di controllo di accesso](/windows/desktop/SecAuthZ/access-control-entries). Per ulteriori informazioni, vedere [creazione di un DACL](/windows/desktop/SecBP/best-practices-for-the-security-apis).<br/> |
| **Gruppo**        | Gruppo a cui appartiene questo oggetto protetto. Questa proprietà contiene un'istanza di [**\_ trustee Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) che contiene il nome, il dominio e l'ID di sicurezza (SID) del gruppo a cui appartiene il proprietario.<br/>                                                                                                                                                             |
| **Proprietario**        | Proprietario di questo oggetto protetto. Questa proprietà contiene un'istanza di [ \_ trustee Win32](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) che contiene il nome, il dominio e l'ID di sicurezza (SID) del proprietario.<br/>                                                                                                                                                                                                          |
| **SACL**         | L' [elenco di controllo di accesso di sistema (ACL)](/windows/desktop/SecAuthZ/access-control-lists) contiene una matrice di istanze [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) che rappresentano il tipo di tentativi di accesso che generano record di controllo per utenti o gruppi. Per ulteriori informazioni, vedere [SACL per un nuovo oggetto](/windows/desktop/SecAuthZ/sacl-for-a-new-object).<br/>                                                                        |



 

## <a name="dacl-and-sacl"></a>DACL e SACL

Le matrici di oggetti [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) nell'elenco di controllo di accesso discrezionale (DACL) e nell'elenco di controllo di accesso di sistema {SACL) creano un collegamento tra un utente o un gruppo e i rispettivi diritti di accesso.

Quando una proprietà DACL non contiene una voce di controllo di accesso (ACE), non vengono concessi i diritti di accesso e l'accesso all'oggetto viene negato.

> [!Note]  
> Un DACL **null** fornisce l'accesso completo a tutti gli utenti, che costituisce un grave rischio per la sicurezza. Per ulteriori informazioni, vedere [creazione di un DACL](/windows/desktop/SecBP/creating-a-dacl).

 

## <a name="win32_ace-win32_trustee-win32_sid"></a>\_ACE Win32, \_ trustee Win32, \_ SID Win32

Un [**oggetto \_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) contiene un'istanza della classe [**\_ trustee Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) che identifica un utente o un gruppo e una proprietà **accessMask** che è una maschera di maschera, che specifica le azioni che possono essere eseguite da un utente o da un gruppo. Ad esempio, a un utente o a un gruppo potrebbe essere concesso il diritto di leggere un file, ma non di scrivere nel file. Un **oggetto \_ ACE Win32** contiene anche una voce ACE che indica se si tratta o meno di un accesso Consenti o nega.

> [!Note]  
> L'ordine degli [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) in un DACL è importante perché in un elenco DACL sono consentite sia la voce di controllo di accesso (ACE) che la negazione. Per ulteriori informazioni, vedere [Order of ACE in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

 

Ogni account utente o gruppo rappresentato da un [**\_ trustee Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) dispone di un ID di sicurezza (SID) che identifica in modo univoco un account e specifica i privilegi di accesso dell'account. Il modo in cui si specificano i dati SID dipende dal sistema operativo. Per ulteriori informazioni, vedere [modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md).

Il diagramma seguente illustra il contenuto di un' [**istanza \_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .

![contenuto di un' \- istanza Ace Win32](images/win32-ace.png)

## <a name="example-checking-who-has-access-to-printers"></a>Esempio: controllo dell'accesso alle stampanti

Nell'esempio di codice VBScript riportato di seguito viene illustrato come utilizzare il descrittore di sicurezza della stampante. Lo script chiama il metodo [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) nella classe [**\_ Printer Win32**](/windows/desktop/CIMWin32Prov/win32-printer) per ottenere il descrittore, quindi determina se è presente un elenco di controllo di accesso discrezionale (DACL) nel descrittore di sicurezza. Se è presente un DACL, lo script ottiene l'elenco di voci di controllo di accesso (ACE) dal DACL. Ogni voce ACE è rappresentata da un'istanza di [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace). Lo script controlla ogni voce ACE per ottenere il nome dell'utente e determinare se l'utente ha accesso alla stampante. L'utente è rappresentato da un'istanza del [**\_ trustee Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) incorporato nell'istanza **\_ ACE Win32** .


```VB
SE_DACL_PRESENT = &h4
ACCESS_ALLOWED_ACE_TYPE = &h0
ACCESS_DENIED_ACE_TYPE  = &h1

strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")

Set colInstalledPrinters =  objWMIService.ExecQuery _
    ("Select * from Win32_Printer")

For Each objPrinter in colInstalledPrinters
   Wscript.Echo "Name: " & objPrinter.Name 
' Get security descriptor for printer
    Return = objPrinter.GetSecurityDescriptor( objSD )
    If ( return <> 0 ) Then
 WScript.Echo "Could not get security descriptor: " & Return
 wscript.Quit Return
    End If
' Extract the security descriptor flags
    intControlFlags = objSD.ControlFlags
    If intControlFlags AND SE_DACL_PRESENT Then
' Get the ACE entries from security descriptor
        colACEs = objSD.DACL
    For Each objACE in colACEs
' Get all the trustees and determine which have access to printer
        WScript.Echo objACE.Trustee.Domain & "\" & objACE.Trustee.Name
        If objACE.AceType = ACCESS_ALLOWED_ACE_TYPE Then
            WScript.Echo vbTab & "User has access to printer"
        ElseIf objACE.AceType = ACCESS_DENIED_ACE_TYPE Then
            WScript.Echo vbTab & "User does not have access to the printer"
        End If
    Next
    Else
    WScript.Echo "No DACL found in security descriptor"
End If
Next
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md)
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

 

