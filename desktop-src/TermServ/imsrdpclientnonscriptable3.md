---
title: Interfaccia IMsRdpClientNonScriptable3
description: Fornisce l'accesso alle proprietà non disponibili per lo scripting della sessione remota di un client nel controllo ActiveX Desktop remoto. Deriva dall'interfaccia IMsRdpClientNonScriptable2.
ms.assetid: 40cfcd8e-5dd7-497d-8c57-da1f542136b8
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c456393ee00c06bcd16135a7fbc73b0f1686259f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964425"
---
# <a name="imsrdpclientnonscriptable3-interface"></a>Interfaccia IMsRdpClientNonScriptable3

Fornisce l'accesso alle proprietà non disponibili per lo scripting della sessione remota di un client nel controllo ActiveX Desktop remoto. Deriva dall'interfaccia [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) . È possibile accedere ai metodi di questa interfaccia solo tramite vtable; non sono disponibili per l'uso nei client con script.

## <a name="members"></a>Membri

L'interfaccia **IMsRdpClientNonScriptable3** eredita da [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md). **IMsRdpClientNonScriptable3** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IMsRdpClientNonScriptable3** ha queste proprietà.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Proprietà</th>
<th style="text-align: left;">Tipo di accesso</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-connectionbartext.md"><strong>ConnectionBarText</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Stringa di testo da visualizzare per la barra di connessione.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-devicecollection.md"><strong>Crea devicecollection</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Raccolta di dispositivi PnP disponibili per il reindirizzamento.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-drivecollection.md"><strong>Unitàcollection</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Raccolta di unità disco disponibili per il reindirizzamento.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>EnableCredSspSupport</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Specifica se CredSSP è abilitato per questa connessione.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-negotiatesecuritylayer.md"><strong>NegotiateSecurityLayer</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Specifica se l'impostazione NegotiateSecurityLayer è supportata per questa connessione.<br/>
<blockquote>
[!Note]<br />
Quando <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>CredSspSupport</strong></a> è abilitato e presente nel client o quando Secure Sockets Layer (SSL) è abilitato con l'autenticazione utente, NegotiateSecurityLayer viene ignorato.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-promptforcredentials.md"><strong>PromptForCredentials</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Specifica se la finestra di dialogo Richiedi credenziali deve essere visualizzata.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-redirectdynamicdevices.md"><strong>RedirectDynamicDevices</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Specifica se i dispositivi PnP collegati in modo dinamico enumerati durante una sessione sono disponibili per il reindirizzamento.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-redirectdynamicdrives.md"><strong>RedirectDynamicDrives</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Specifica se le unità PnP associate in modo dinamico enumerate in una sessione sono disponibili per il reindirizzamento.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-showredirectionwarningdialog.md"><strong>ShowRedirectionWarningDialog</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Specifica se la finestra di dialogo di avviso di sicurezza del reindirizzamento deve essere visualizzata prima di avviare una sessione.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-warnaboutclipboardredirection.md"><strong>WarnAboutClipboardRedirection</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Specifica se la finestra di dialogo avviso di sicurezza deve includere un avviso relativo al reindirizzamento degli Appunti prima di avviare una sessione.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-warnaboutsendingcredentials.md"><strong>WarnAboutSendingCredentials</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Specifica se l'avviso di sicurezza deve includere un avviso sull'invio di credenziali al server remoto prima di avviare una sessione.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 è definito come C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting è definito come A0C63C30-F08D-4ab4-907c-34905D770C7D<br/> CLSID \_ MsRdpClient5 è definito come 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2<br/> CLSID \_ MsRdpClient5NotSafeForScripting è definito come 4EB2F086-C818-447E-B32C-C51CE2B30D31<br/> CLSID \_ MsRdpClient6 è definito come 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> CLSID \_ MsRdpClient6NotSafeForScripting è definito come D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> CLSID \_ MsRdpClient7 è definito come A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting è definito come 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID \_ MsRdpClient8 è definito come 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting è definito come A3BC03A0-041d-42e3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9 è definito come 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting è definito come 8B918B82-7985-4c24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable3 è definito come b3378d90-0728-45c7-8ed7-b6159fb92219<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> <dt>

[Riferimento Connessione Web Desktop remoto](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





