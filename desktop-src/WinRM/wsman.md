---
title: Oggetto WSMan (WSManDisp.h)
description: Fornisce metodi e proprietà utilizzati per creare una sessione, rappresentata da un oggetto Session.
ms.assetid: 45895a4e-b7de-4469-ae78-6d1d3f9d6145
ms.tgt_platform: multiple
keywords:
- Oggetto WSMan Windows remota
- Oggetto WSMan Windows gestione remota , descritto
topic_type:
- apiref
api_name:
- WSMan
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dac26be22118a320848ea227643f9c4d3857dc01
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475967"
---
# <a name="wsman-object"></a>Oggetto WSMan

Fornisce metodi e proprietà utilizzati per creare una sessione, rappresentata da un [**oggetto**](session.md) Session. Qualsiasi Windows di gestione remota richiede la creazione di una sessione che si connette [**a**](session.md) un computer remoto, a un controller di gestione [*di base*](windows-remote-management-glossary.md) (BMC) o al computer locale. Le operazioni includono il recupero, la scrittura, l'enumerazione dei dati o la chiamata di metodi.

## <a name="members"></a>Membri

**L'oggetto WSMan** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto WSMan** dispone di questi metodi.




| Metodo | Descrizione | 
|--------|-------------|
| <a href="wsman-createconnectionoptions.md"><strong>CreateConnectionOptions</strong></a> | Crea un <a href="connectionoptions.md"><strong>oggetto ConnectionOptions</strong></a> che specifica il nome utente e la password usati durante la creazione di una sessione remota.<br /> | 
| <a href="wsman-createresourcelocator.md"><strong>CreateResourceLocator</strong></a> | Crea un <a href="resourcelocator.md"><strong>oggetto ResourceLocator</strong></a> che può specificare:<br /><ul><li>Percorso completo di una <a href="windows-remote-management-glossary.md"><em>risorsa o</em></a> di una singola parte di dati.</li><li>Selettore <a href="windows-remote-management-glossary.md"><em>per</em></a> un'istanza specifica di una risorsa.</li><li>Opzione <a href="windows-remote-management-glossary.md"><em>che</em></a> fornisce dati aggiuntivi al provider di risorse.</li></ul> | 
| <a href="wsman-createsession.md"><strong>CreateSession</strong></a> | Crea un <a href="session.md"><strong>oggetto Session</strong></a> che può quindi essere usato per le operazioni di rete successive.<br /> | 
| <a href="wsman-enumerationflaghierarchydeep.md"><strong>WSMan.EnumerationFlagHierarchyDeep</strong></a> | Restituisce il valore del flag di enumerazione <strong>EnumerationFlagHierarchyDeep</strong> da usare nel parametro <em>flags</em> di <a href="session-enumerate.md"><strong>Session.Enumerate.</strong></a><br /> | 
| <a href="wsman-enumerationflaghierarchydeepbasepropsonly.md"><strong>WSMan.EnumerationFlagHierarchyDeepBasePropsOnly</strong></a> | Restituisce il valore del flag di enumerazione <strong>EnumerationFlagHierarchyDeepBasePropsOnly</strong> da usare nel parametro <em>flags</em> di <a href="session-enumerate.md"><strong>Session.Enumerate.</strong></a><br /> | 
| <a href="wsman-enumerationflaghierarchyshallow.md"><strong>WSMan.EnumerationFlagHierarchyShallow</strong></a> | Restituisce il valore del flag di enumerazione <strong>EnumerationFlagHierarchyShallow</strong> da usare nel parametro <em>flags</em> di <a href="session-enumerate.md"><strong>Session.Enumerate.</strong></a><br /> | 
| <a href="wsman-enumerationflagnonxmltext.md"><strong>WSMan.EnumerationFlagNonXmlText</strong></a> | Restituisce il valore della costante di enumerazione <strong>WSManFlagNonXmlText</strong> da usare nel parametro <em>flags</em> del <a href="session-enumerate.md"><strong>metodo Session.Enumerate.</strong></a><br /> | 
| <a href="wsman-enumerationflagreturnepr.md"><strong>WSMan.EnumerationFlagReturnEPR</strong></a> | Restituisce il valore del flag di enumerazione <strong>EnumerationFlagReturnEPR</strong> da usare nel parametro <em>flags</em> di <a href="session-enumerate.md"><strong>Session.Enumerate.</strong></a><br /> | 
| <a href="wsman-enumerationflagreturnobject.md"><strong>WSMan.EnumerationFlagReturnObject</strong></a> | Restituisce il valore del flag di enumerazione <strong>EnumerationFlagReturnObject</strong> da usare nel parametro <em>flags</em> di <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.<br /> | 
| <a href="wsman-enumerationflagreturnobjectandepr.md"><strong>WSMan.EnumerationFlagReturnObjectAndEPR</strong></a> | Restituisce il valore del flag di enumerazione <strong>EnumerationFlagReturnObjectAndEPR</strong> da usare nel parametro <em>flags</em> di <a href="session-enumerate.md"><strong>Session.Enumerate.</strong></a><br /> | 
| <a href="wsman-geterrormessage.md"><strong>WSMan.GetErrorMessage</strong></a> | Restituisce una stringa formattata contenente il testo di un numero di errore.<br /> | 
| <a href="wsman-sessionflagcredusernamepassword.md"><strong>WSMan.SessionFlagCredUsernamePassword</strong></a> | Restituisce il valore del flag di autenticazione <strong>WSManFlagCredUsernamePassword</strong> da usare nel parametro <em>flags</em> di <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagenablespnserverport.md"><strong>WSMan.SessionFlagEnableSPNServerPort</strong></a> | Restituisce il valore del flag di autenticazione <strong>WSManFlagEnableSPNServerPort</strong> da usare nel parametro <em>flags</em> di <a href="wsman-createsession.md"><strong>WSMan.CreateSession.</strong></a><br /> | 
| <a href="wsman-sessionflagnoencryption.md"><strong>WSMan.SessionFlagNoEncryption</strong></a> | Restituisce il valore del flag di autenticazione <strong>WSManFlagNoEncryption</strong> da usare nel parametro <em>flags</em> di <a href="wsman-createsession.md"><strong>WSMan.CreateSession.</strong></a><br /> | 
| <a href="wsman-sessionflagskipcacheck.md"><strong>WSMan.SessionFlagSkipCACheck</strong></a> | Restituisce il valore del flag di autenticazione <strong>WSManFlagSkipCACheck</strong> da usare nel parametro <em>flags</em> di <a href="wsman-createsession.md"><strong>WSMan.CreateSession.</strong></a><br /> | 
| <a href="wsman-sessionflagskipcncheck.md"><strong>WSMan.SessionFlagSkipCNCheck</strong></a> | Restituisce il valore del flag di autenticazione <strong>WSManFlagSkipCNCheck</strong> da usare nel parametro <em>flags</em> di <a href="wsman-createsession.md"><strong>WSMan.CreateSession.</strong></a><br /> | 
| <a href="wsman-sessionflagusebasic.md"><strong>WSMan.SessionFlagUseBasic</strong></a> | Restituisce il valore del flag di autenticazione <strong>WSManFlagUseBasic</strong> da usare nel parametro <em>flags</em> di <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagusedigest.md"><strong>WSMan.SessionFlagUseDigest</strong></a> | Restituisce il valore del flag di autenticazione <strong>WSManFlagUseDigest</strong> da usare nel parametro <em>flags</em> di <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagusekerberos.md"><strong>WSMan.SessionFlagUseKerberos</strong></a> | Restituisce il valore del flag di autenticazione <strong>WSManFlagUseKerberos</strong> da usare nel parametro <em>flags</em> di <a href="wsman-createsession.md"><strong>WSMan.CreateSession.</strong></a><br /> | 
| <a href="wsman-sessionflagusenegotiate.md"><strong>WSMan.SessionFlagUseNegotiate</strong></a> | Restituisce il valore del flag di autenticazione <strong>WSManFlagUseNegotiate</strong> da usare nel parametro <em>flags</em> di <a href="wsman-createsession.md"><strong>WSMan.CreateSession.</strong></a><br /> | 
| <a href="wsman-sessionflagusenoauthentication.md"><strong>WSMan.SessionFlagUseNoAuthentication</strong></a> | Restituisce il valore del flag di autenticazione <strong>WSManFlagUseNoAuthentication</strong> da usare nel parametro <em>flags</em> di <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagutf8.md"><strong>WSMan.SessionFlagUTF8</strong></a> | Restituisce il valore del flag di autenticazione <strong>WSManFlagUTF8</strong> da usare nel parametro <em>flags</em> di <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.<br /> | 




 

### <a name="properties"></a>Proprietà

**L'oggetto WSMan** ha queste proprietà.



| Proprietà                                            | Tipo di accesso          | Descrizione                                                                   |
|:----------------------------------------------------|:---------------------|:------------------------------------------------------------------------------|
| [**CommandLine**](wsman-commandline.md)<br/> | Sola lettura<br/> | Ottiene la riga di comando non elaborata per il processo di hosting corrente.<br/> |
| [**Errore**](wsman-error.md)<br/>             | Sola lettura<br/> | Ottiene informazioni sull'errore.<br/>                                            |



 

## <a name="remarks"></a>Commenti

**L'oggetto WSMan** corrisponde alle [**interfacce IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) e [**IWSManEx.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) **WSMan** è l'unico oggetto che può essere creato direttamente usando [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato come creare un'istanza di **un oggetto WSMan.**


```VB
Dim objWsman
Dim Session, Resource 
Set objWsman = CreateObject( "WSMAN.Automation" )
Set Session = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/Root/CIMv2/Win32_OperatingSystem"
```



## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[WinRM Scripting API](winrm-scripting-api.md)
</dt> <dt>

[Informazioni Windows gestione remota](about-windows-remote-management.md)
</dt> <dt>

[Uso Windows gestione remota](using-windows-remote-management.md)
</dt> <dt>

[Scripting in Windows Remote Management](scripting-in-windows-remote-management.md)
</dt> <dt>

[Recupero di dati dal computer locale](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[Recupero di dati da un computer remoto](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

