---
title: Oggetto WSMan (WSManDisp. h)
description: Fornisce metodi e proprietà utilizzati per creare una sessione, rappresentata da un oggetto sessione.
ms.assetid: 45895a4e-b7de-4469-ae78-6d1d3f9d6145
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows oggetto WSMan
- Gestione remota Windows oggetto WSMan, descritto
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
ms.openlocfilehash: e02cb92b2d72d657791d4a16bd1e999b77645a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400296"
---
# <a name="wsman-object"></a>WSMan (oggetto)

Fornisce metodi e proprietà utilizzati per creare una sessione, rappresentata da un oggetto [**sessione**](session.md) . Qualsiasi operazione di Gestione remota Windows richiede la creazione di una [**sessione**](session.md) che si connette a un computer remoto, a un [*controller di gestione di base*](windows-remote-management-glossary.md) (BMC) o al computer locale. Le operazioni includono il recupero, la scrittura, l'enumerazione dei dati o la chiamata di metodi.

## <a name="members"></a>Membri

L'oggetto **WSMan** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'oggetto **WSMan** .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Metodo</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-createconnectionoptions.md"><strong>CreateConnectionOptions</strong></a></td>
<td style="text-align: left;">Crea un oggetto <a href="connectionoptions.md"><strong>ConnectionOptions</strong></a> che specifica il nome utente e la password utilizzati durante la creazione di una sessione remota.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-createresourcelocator.md"><strong>CreateResourceLocator</strong></a></td>
<td style="text-align: left;">Crea un oggetto <a href="resourcelocator.md"><strong>resourceLocator</strong></a> che può specificare:<br/>
<ul>
<li>Percorso completo di una <a href="windows-remote-management-glossary.md"><em>risorsa</em></a> o di un singolo elemento di dati.</li>
<li><a href="windows-remote-management-glossary.md"><em>Selettore</em></a> per un'istanza specifica di una risorsa.</li>
<li><a href="windows-remote-management-glossary.md"><em>Opzione</em></a> che fornisce dati aggiuntivi al provider di risorse.</li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-createsession.md"><strong>CreateSession</strong></a></td>
<td style="text-align: left;">Crea un oggetto <a href="session.md"><strong>sessione</strong></a> che può quindi essere utilizzato per le operazioni di rete successive.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-enumerationflaghierarchydeep.md"><strong>WSMan. EnumerationFlagHierarchyDeep</strong></a></td>
<td style="text-align: left;">Restituisce il valore del flag di enumerazione <strong>EnumerationFlagHierarchyDeep</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="session-enumerate.md"><strong>Session. enumerate</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-enumerationflaghierarchydeepbasepropsonly.md"><strong>WSMan. EnumerationFlagHierarchyDeepBasePropsOnly</strong></a></td>
<td style="text-align: left;">Restituisce il valore del flag di enumerazione <strong>EnumerationFlagHierarchyDeepBasePropsOnly</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="session-enumerate.md"><strong>Session. enumerate</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-enumerationflaghierarchyshallow.md"><strong>WSMan. EnumerationFlagHierarchyShallow</strong></a></td>
<td style="text-align: left;">Restituisce il valore del flag di enumerazione <strong>EnumerationFlagHierarchyShallow</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="session-enumerate.md"><strong>Session. enumerate</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-enumerationflagnonxmltext.md"><strong>WSMan. EnumerationFlagNonXmlText</strong></a></td>
<td style="text-align: left;">Restituisce il valore della costante di enumerazione <strong>WSManFlagNonXmlText</strong> per l'utilizzo nel parametro <em>Flags</em> del metodo <a href="session-enumerate.md"><strong>Session. enumerate</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-enumerationflagreturnepr.md"><strong>WSMan. EnumerationFlagReturnEPR</strong></a></td>
<td style="text-align: left;">Restituisce il valore del flag di enumerazione <strong>EnumerationFlagReturnEPR</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="session-enumerate.md"><strong>Session. enumerate</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-enumerationflagreturnobject.md"><strong>WSMan. EnumerationFlagReturnObject</strong></a></td>
<td style="text-align: left;">Restituisce il valore del flag di enumerazione <strong>EnumerationFlagReturnObject</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="session-enumerate.md"><strong>Session. enumerate</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-enumerationflagreturnobjectandepr.md"><strong>WSMan. EnumerationFlagReturnObjectAndEPR</strong></a></td>
<td style="text-align: left;">Restituisce il valore del flag di enumerazione <strong>EnumerationFlagReturnObjectAndEPR</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="session-enumerate.md"><strong>Session. enumerate</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-geterrormessage.md"><strong>WSMan. GetErrorMessage</strong></a></td>
<td style="text-align: left;">Restituisce una stringa formattata contenente il testo di un numero di errore.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagcredusernamepassword.md"><strong>WSMan. SessionFlagCredUsernamePassword</strong></a></td>
<td style="text-align: left;">Restituisce il valore del flag di autenticazione <strong>WSManFlagCredUsernamePassword</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagenablespnserverport.md"><strong>WSMan. SessionFlagEnableSPNServerPort</strong></a></td>
<td style="text-align: left;">Restituisce il valore del flag di autenticazione <strong>WSManFlagEnableSPNServerPort</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagnoencryption.md"><strong>WSMan. SessionFlagNoEncryption</strong></a></td>
<td style="text-align: left;">Restituisce il valore del flag di autenticazione <strong>WSManFlagNoEncryption</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagskipcacheck.md"><strong>WSMan. SessionFlagSkipCACheck</strong></a></td>
<td style="text-align: left;">Restituisce il valore del flag di autenticazione <strong>WSManFlagSkipCACheck</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagskipcncheck.md"><strong>WSMan. SessionFlagSkipCNCheck</strong></a></td>
<td style="text-align: left;">Restituisce il valore del flag di autenticazione <strong>WSManFlagSkipCNCheck</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagusebasic.md"><strong>WSMan. SessionFlagUseBasic</strong></a></td>
<td style="text-align: left;">Restituisce il valore del flag di autenticazione <strong>WSManFlagUseBasic</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagusedigest.md"><strong>WSMan. SessionFlagUseDigest</strong></a></td>
<td style="text-align: left;">Restituisce il valore del flag di autenticazione <strong>WSManFlagUseDigest</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagusekerberos.md"><strong>WSMan. SessionFlagUseKerberos</strong></a></td>
<td style="text-align: left;">Restituisce il valore del flag di autenticazione <strong>WSManFlagUseKerberos</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagusenegotiate.md"><strong>WSMan. SessionFlagUseNegotiate</strong></a></td>
<td style="text-align: left;">Restituisce il valore del flag di autenticazione <strong>WSManFlagUseNegotiate</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagusenoauthentication.md"><strong>WSMan. SessionFlagUseNoAuthentication</strong></a></td>
<td style="text-align: left;">Restituisce il valore del flag di autenticazione <strong>WSManFlagUseNoAuthentication</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagutf8.md"><strong>WSMan. SessionFlagUTF8</strong></a></td>
<td style="text-align: left;">Restituisce il valore del flag di autenticazione <strong>WSManFlagUTF8</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Proprietà

L'oggetto **WSMan** presenta queste proprietà.



| Proprietà                                            | Tipo di accesso          | Descrizione                                                                   |
|:----------------------------------------------------|:---------------------|:------------------------------------------------------------------------------|
| [**CommandLine**](wsman-commandline.md)<br/> | Sola lettura<br/> | Ottiene la riga di comando non elaborata per il processo di hosting corrente.<br/> |
| [**Errore**](wsman-error.md)<br/>             | Sola lettura<br/> | Ottiene le informazioni sull'errore.<br/>                                            |



 

## <a name="remarks"></a>Commenti

L'oggetto **WSMan** corrisponde alle interfacce [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) e [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) . **WSMan** è l'unico oggetto che può essere creato direttamente usando [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato come creare un'istanza di un oggetto **WSMan** .


```VB
Dim objWsman
Dim Session, Resource 
Set objWsman = CreateObject( "WSMAN.Automation" )
Set Session = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/Root/CIMv2/Win32_OperatingSystem"
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[API di scripting WinRM](winrm-scripting-api.md)
</dt> <dt>

[Informazioni su Gestione remota Windows](about-windows-remote-management.md)
</dt> <dt>

[Utilizzo di Gestione remota Windows](using-windows-remote-management.md)
</dt> <dt>

[Creazione di script in Gestione remota Windows](scripting-in-windows-remote-management.md)
</dt> <dt>

[Recupero di dati dal computer locale](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[Recupero di dati da un computer remoto](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

