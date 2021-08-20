---
title: Recupero di dati da un computer remoto
description: È possibile ottenere dati o gestire le risorse nei computer remoti e nel computer locale. La connessione a un computer remoto in Windows script di gestione remota è molto simile all'esecuzione di una connessione locale.
ms.assetid: 578eee80-a6c1-4456-9683-14e0a3386248
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cf3531e19c0848691ededa0c3b6b2fad642de33c2a5f2d465ac899716970a512
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823408"
---
# <a name="obtaining-data-from-a-remote-computer"></a>Recupero di dati da un computer remoto

È possibile ottenere dati o gestire le risorse nei computer remoti e nel computer locale. La connessione a un computer remoto in Windows script di gestione remota è molto simile all'esecuzione di una connessione locale. I dati dell'istanza WMI sono disponibili e, se il computer remoto dispone di hardware BMC in grado di comunicare tramite il protocollo WS-Management, sono disponibili anche i dati [di Intelligent Platform Management Interface (IPMI).](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) Per altre informazioni, vedere [Windows gestione remota e WMI](windows-remote-management-and-wmi.md) e Gestione hardware [remota.](remote-hardware-management.md)

Potrebbe essere necessario creare un oggetto [**ConnectionOptions**](connectionoptions.md) per specificare le informazioni sul tipo di autenticazione richiesto per l'accesso.

Se l'account nel computer remoto ha lo stesso nome utente e password di accesso, le uniche informazioni aggiuntive necessarie sono il trasporto, il nome di dominio e il nome del computer. A causa [di Controllo dell'account](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista)utente , l'account remoto deve essere un account di dominio e un membro del gruppo Administrators del computer remoto. Se l'account è un membro del computer locale del gruppo Administrators, Controllo dell'account utente non consente l'accesso al servizio Gestione remota Windows. Per accedere a un servizio WinRM remoto in un gruppo di lavoro, il filtro di Controllo dell'account utente per gli account locali deve essere disabilitato creando la seguente voce del Registro di sistema DWORD e impostandone il valore su 1: **\[ HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion Policies System \\ \\ \] LocalAccountTokenFilterPolicy**.

**Per connettersi a un computer remoto usando il nome utente e la password di accesso**

1.  Specificare il computer di destinazione con un nome di dominio completo o un indirizzo IP e assegnarlo a una costante. Se viene specificato un indirizzo IPv6, l'indirizzo deve essere racchiuso tra parentesi quadre.

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  Creare un [**oggetto WSMan.**](wsman.md)

    ```VB
    Set objWsman = CreateObject("WSMan.Automation")
    ```

    

3.  Creare la sessione, specificando il trasporto, HTTP o HTTPS e concatenarla con la costante che rappresenta il computer di destinazione.

    ```VB
    
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

Nell'esempio di codice VBScript seguente viene illustrato lo script completo. Lo script include una subroutine per trasformare i dati da XML non elaborato a formato leggibile. Per altre informazioni, vedere [Visualizzazione dell'output XML dagli script WinRM.](displaying-xml-output-from-winrm-scripts.md)


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

    

2.  Creare un [**oggetto WSMan.**](wsman.md)

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    
    ```

    

3.  Chiamare il [**metodo WSMan.CreateConnectionOptions**](wsman-createconnectionoptions.md) per creare un [**oggetto ConnectionOptions.**](connectionoptions.md) L'account nel computer remoto deve essere membro del gruppo Administrators del computer locale.

    ```VB
    Set objConnectionOptions = objWsman.CreateConnectionOptions
    objConnectionOptions.UserName = "Username"
    objConnectionOptions.Password = "Password"
    ```

    

4.  Nella chiamata [**WSman.CreateSession**](wsman-createsession.md) specificare i flag di connessione della sessione appropriati nel *parametro flags.* Per altre informazioni, vedere [Costanti di sessione.](session-constants.md) Specificare il computer di destinazione con un nome computer completo o un indirizzo IP e il trasporto, ovvero http o https. Questo script richiede [*l'autenticazione Kerberos*](windows-remote-management-glossary.md) dal servizio Gestione remota Windows remoto.

    A differenza degli script WMI, è possibile usare diversi metodi di autenticazione negli script winrm. Per altre informazioni, vedere [Autenticazione per connessioni remote.](authentication-for-remote-connections.md)

    ```VB
    iFlags = objWsman.SessionFlagUseKerberos Or _
      objWsman.SessionFlagCredUserNamePassword
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
      iFlags, objConnectionOptions)
    ```

    

5.  Quando l'oggetto sessione è disponibile, è possibile chiamare uno dei metodi [**dell'oggetto Session**](session.md) per ottenere i dati per una risorsa. È possibile ottenere i dati per qualsiasi risorsa disponibile nel computer in cui è in esecuzione la sessione. Per altre informazioni, vedere [Recupero di dati dal computer locale.](obtaining-data-from-the-local-computer.md)

Nell'esempio di codice VBScript seguente viene illustrato lo script completo. Lo script include una subroutine per trasformare i dati da XML non elaborato a formato leggibile. Per altre informazioni, vedere [Visualizzazione dell'output XML dagli script WinRM.](displaying-xml-output-from-winrm-scripts.md) Lo script specifica l'autenticazione Kerberos, ma se il computer remoto si trova in un gruppo di lavoro anziché in un dominio, se si specifica Kerberos viene generato un errore.


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

[Informazioni Windows gestione remota](about-windows-remote-management.md)
</dt> <dt>

[Uso Windows gestione remota](using-windows-remote-management.md)
</dt> <dt>

[Windows Informazioni di riferimento sulla gestione remota](windows-remote-management-reference.md)
</dt> </dl>

 

 