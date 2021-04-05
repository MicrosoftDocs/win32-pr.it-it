---
title: Recupero di dati da un computer remoto
description: È possibile ottenere dati o gestire le risorse in computer remoti e nel computer locale. La connessione a un computer remoto in uno script Gestione remota Windows è molto simile all'esecuzione di una connessione locale.
ms.assetid: 578eee80-a6c1-4456-9683-14e0a3386248
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8cfc95a73dab4c9a0f19481b7ba41f3c40a3862d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872545"
---
# <a name="obtaining-data-from-a-remote-computer"></a>Recupero di dati da un computer remoto

È possibile ottenere dati o gestire le risorse in computer remoti e nel computer locale. La connessione a un computer remoto in uno script Gestione remota Windows è molto simile all'esecuzione di una connessione locale. I dati dell'istanza WMI sono disponibili e, se il computer remoto dispone di hardware BMC in grado di comunicare utilizzando il protocollo di WS-Management, sono disponibili anche i dati dell' [interfaccia di gestione piattaforma intelligente (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) . Per ulteriori informazioni, vedere [gestione remota Windows e WMI](windows-remote-management-and-wmi.md) e [gestione hardware remota](remote-hardware-management.md).

Potrebbe essere necessario creare un oggetto [**ConnectionOptions**](connectionoptions.md) per specificare le informazioni sul tipo di autenticazione richiesto per l'accesso.

Se l'account del computer remoto ha lo stesso nome utente e la stessa password di accesso, le uniche informazioni aggiuntive necessarie sono il trasporto, il nome di dominio e il nome del computer. A causa del [controllo dell'account utente](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista), l'account remoto deve essere un account di dominio e un membro del gruppo Administrators del computer remoto. Se l'account è un membro del computer locale del gruppo Administrators, il controllo dell'account utente non consente l'accesso al servizio WinRM. Per accedere a un servizio WinRM remoto in un gruppo di lavoro, è necessario disabilitare il filtro UAC per gli account locali creando la seguente voce del registro di sistema DWORD e impostandone il valore su 1: **\[ HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Policies \\ System \] LocalAccountTokenFilterPolicy**.

**Per connettersi a un computer remoto usando il nome utente e la password di accesso**

1.  Specificare il computer di destinazione con un nome di dominio completo o un indirizzo IP e assegnarlo a una costante. Se viene specificato un indirizzo IPv6, l'indirizzo deve essere racchiuso tra parentesi quadre.

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  Creare un oggetto [**WSMan**](wsman.md) .

    ```VB
    Set objWsman = CreateObject("WSMan.Automation")
    ```

    

3.  Creare la sessione, specificando il trasporto, HTTP o HTTPS, e concatenarla con la costante che rappresenta il computer di destinazione.

    ```VB
    
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

Nell'esempio di codice VBScript riportato di seguito viene illustrato lo script completo. Lo script include una subroutine per trasformare i dati da XML non elaborato a formato leggibile. Per ulteriori informazioni, vedere [visualizzazione dell'output XML dagli script WinRM](displaying-xml-output-from-winrm-scripts.md).


```VB
Const RemoteComputer = "ComputerName.domain.com"

Set objWsman = CreateObject("WSMan.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
  "wmi/root/cimv2/Win32_OperatingSystem"
Set objResponse = objSession.Enumerate(strResource)

While Not objResponse.AtEndOfStream
    DisplayOutput(objResponse.ReadItem) 
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



**Per connettersi a un computer remoto usando un account diverso**

1.  Specificare il computer di destinazione con un nome di dominio completo o un indirizzo IP e assegnarlo a una costante. Se viene specificato un indirizzo IPv6, l'indirizzo deve essere racchiuso tra parentesi quadre.

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  Creare un oggetto [**WSMan**](wsman.md) .

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    
    ```

    

3.  Chiamare il metodo [**WSMan. CreateConnectionOptions**](wsman-createconnectionoptions.md) per creare un oggetto [**ConnectionOptions**](connectionoptions.md) . L'account nel computer remoto deve essere un membro del gruppo Administrators del computer locale.

    ```VB
    Set objConnectionOptions = objWsman.CreateConnectionOptions
    objConnectionOptions.UserName = "Username"
    objConnectionOptions.Password = "Password"
    ```

    

4.  Nella chiamata [**WSMan. CreateSession**](wsman-createsession.md) specificare i flag di connessione di sessione appropriati nel parametro *Flags* . Per altre informazioni, vedere [costanti di sessione](session-constants.md). Specificare il computer di destinazione con un nome di computer completo o un indirizzo IP e il trasporto, ovvero http o HTTPS. Questo script richiede l'autenticazione [*Kerberos*](windows-remote-management-glossary.md) dal servizio WinRM remoto.

    Diversamente dagli script WMI, è possibile utilizzare diversi metodi di autenticazione negli script WinRM. Per altre informazioni, vedere [autenticazione per le connessioni remote](authentication-for-remote-connections.md).

    ```VB
    iFlags = objWsman.SessionFlagUseKerberos Or _
      objWsman.SessionFlagCredUserNamePassword
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
      iFlags, objConnectionOptions)
    ```

    

5.  Quando l'oggetto Session è disponibile, è possibile chiamare qualsiasi metodo dell'oggetto [**Session**](session.md) per ottenere i dati per una risorsa. È possibile ottenere dati per qualsiasi risorsa disponibile nel computer in cui è in esecuzione la sessione. Per ulteriori informazioni, vedere [recupero di dati dal computer locale](obtaining-data-from-the-local-computer.md).

Nell'esempio di codice VBScript riportato di seguito viene illustrato lo script completo. Lo script include una subroutine per trasformare i dati da XML non elaborato a formato leggibile. Per ulteriori informazioni, vedere [visualizzazione dell'output XML dagli script WinRM](displaying-xml-output-from-winrm-scripts.md). Lo script specifica l'autenticazione Kerberos, ma se il computer remoto si trova in un gruppo di lavoro anziché in un dominio, specificando Kerberos viene generato un errore.


```VB
Const RemoteComputer = "ComputerName.domain.com"

Set objWsman = CreateObject("Wsman.Automation")
Set objConnectionOptions = objWsman.CreateConnectionOptions
objConnectionOptions.UserName = "Username"
objConnectionOptions.Password = "Password"
iFlags = objWsman.SessionFlagUseKerberos Or _
  objWsman.SessionFlagCredUserNamePassword
Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
  iFlags, objConnectionOptions)
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
  "wmi/root/cimv2/Win32_OperatingSystem"
Set objResponse = objSession.Enumerate(strResource)

While Not objResponse.AtEndOfStream
    DisplayOutput(objResponse.ReadItem) 
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml2.DOMDocument.3.0") 
    Set xslFile = CreateObject("MSXml2.DOMDocument.3.0")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Gestione remota Windows](about-windows-remote-management.md)
</dt> <dt>

[Utilizzo di Gestione remota Windows](using-windows-remote-management.md)
</dt> <dt>

[Riferimento Gestione remota Windows](windows-remote-management-reference.md)
</dt> </dl>

 

 