---
title: Interfaccia IMsRdpClientNonScriptable4
description: Fornisce l'accesso alle proprietà non disponibili per lo scripting della sessione remota di un client nel controllo ActiveX Desktop remoto. Deriva dall'interfaccia IMsRdpClientNonScriptable3.
ms.assetid: 570a5722-94b9-4195-846a-10233d56002d
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aedea56733a2a98db4b966bd91d9337e38e61d0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964978"
---
# <a name="imsrdpclientnonscriptable4-interface"></a>Interfaccia IMsRdpClientNonScriptable4

Fornisce l'accesso alle proprietà non disponibili per lo scripting della sessione remota di un client nel controllo ActiveX Desktop remoto. Deriva dall'interfaccia [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md) . È possibile accedere ai metodi di questa interfaccia solo tramite vtable; non sono disponibili per l'uso nei client con script.

## <a name="members"></a>Membri

L'interfaccia **IMsRdpClientNonScriptable4** eredita da [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md). **IMsRdpClientNonScriptable4** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IMsRdpClientNonScriptable4** ha queste proprietà.



| Proprietà                                                                                                         | Tipo di accesso           | Descrizione                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllowCredentialSaving**](imsrdpclientnonscriptable4-allowcredentialsaving.md)<br/>                     | Lettura/Scrittura<br/> | Specifica se nella finestra di dialogo credenziali viene visualizzata una casella di controllo che consente di salvare le credenziali.<br/>                                                                                        |
| [**LaunchedViaClientShellInterface**](imsrdpclientnonscriptable4-launchedviaclientshellinterface.md)<br/> | Lettura/Scrittura<br/> | Specifica se l'utente ha avviato il controllo client utilizzando l'interfaccia Accesso Web Desktop remoto.<br/>                                                                                                  |
| [**MarkRdpSettingsSecure**](imsrdpclientnonscriptable4-markrdpsettingssecure.md)<br/>                     | Lettura/Scrittura<br/> | Specifica se le impostazioni RDP sono contrassegnate come sicure.<br/>                                                                                                                                          |
| [**PromptForCredsOnClient**](imsrdpclientnonscriptable4-promptforcredsonclient.md)<br/>                   | Lettura/Scrittura<br/> | Specifica se il controllo client visualizza una finestra di dialogo in cui vengono richieste le credenziali.<br/>                                                                                                      |
| [**PublisherCertificateChain**](imsrdpclientnonscriptable4-publishercertificatechain.md)<br/>             | Lettura/Scrittura<br/> | Specifica la catena di certificati del server di pubblicazione. La catena è archiviata in una variante di tipo VT \_ ByRef che contiene un puntatore a una struttura del [**contesto della \_ catena \_ di certificati**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) .<br/> |
| [**RedirectionWarningType**](imsrdpclientnonscriptable4-redirectionwarningtype.md)<br/>                   | Lettura/Scrittura<br/> | Controlla la presenza e l'aspetto della finestra di dialogo di reindirizzamento.<br/>                                                                                                                           |
| [**TrustedZoneSite**](imsrdpclientnonscriptable4-trustedzonesite.md)<br/>                                 | Lettura/Scrittura<br/> | Specifica se il sito Web da cui l'utente ha avviato la connessione si trova nell'elenco dei siti attendibili del computer client.<br/>                                                                |
| [**WarnAboutPrinterRedirection**](imsrdpclientnonscriptable4-warnaboutprinterredirection.md)<br/>         | Lettura/Scrittura<br/> | Specifica se la finestra di dialogo Reindirizzamento Visualizza un messaggio sul reindirizzamento della stampante prima di avviare una sessione.<br/>                                                                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 è definito come C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting è definito come A0C63C30-F08D-4ab4-907c-34905D770C7D<br/> CLSID \_ MsRdpClient6 è definito come 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> CLSID \_ MsRdpClient6NotSafeForScripting è definito come D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> CLSID \_ MsRdpClient7 è definito come A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting è definito come 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID \_ MsRdpClient8 è definito come 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting è definito come A3BC03A0-041d-42e3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9 è definito come 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting è definito come 8B918B82-7985-4c24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable4 è definito come f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Riferimento Connessione Web Desktop remoto](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> </dl>

 

