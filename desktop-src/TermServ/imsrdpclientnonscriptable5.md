---
title: Interfaccia IMsRdpClientNonScriptable5
description: Fornisce l'accesso alle proprietà non disponibili per lo scripting della sessione remota di un client nel controllo ActiveX Desktop remoto. Deriva dall'interfaccia IMsRdpClientNonScriptable4.
ms.assetid: 41b8c624-0451-4a7e-bc80-d0bf269e33c6
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ec338dbe07c4733bf80207298f23f388bf8f77c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479283"
---
# <a name="imsrdpclientnonscriptable5-interface"></a>Interfaccia IMsRdpClientNonScriptable5

Fornisce l'accesso alle proprietà non disponibili per lo scripting della sessione remota di un client nel controllo ActiveX Desktop remoto. Deriva dall'interfaccia [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md) . È possibile accedere ai metodi di questa interfaccia solo tramite vtable; non sono disponibili per l'uso nei client con script.

Un'istanza di questa interfaccia viene ottenuta chiamando [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sull'oggetto [**IMsTscAx**](imstscax-interface.md) , passando l' **IID \_ IMsRdpClientNonScriptable5**.

## <a name="members"></a>Membri

L'interfaccia **IMsRdpClientNonScriptable5** eredita da [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md). **IMsRdpClientNonScriptable5** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IMsRdpClientNonScriptable5** ha queste proprietà.



| Proprietà                                                                                                         | Tipo di accesso           | Descrizione                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**AllowPromptingForCredentials**](imsrdpclientnonscriptable5-allowpromptingforcredentials.md)<br/>       | Lettura/Scrittura<br/> | Specifica se il controllo ActiveX Desktop remoto può richiedere le credenziali all'utente.<br/>                    |
| [**DisableConnectionBar**](imsrdpclientnonscriptable5-disableconnectionbar.md)<br/>                       | Sola scrittura<br/> | Specifica se il controllo ActiveX Desktop remoto deve disabilitare la barra di connessione.<br/>                      |
| [**DisableRemoteAppCapsCheck**](imsrdpclientnonscriptable5-disableremoteappcapscheck.md)<br/>             | Lettura/Scrittura<br/> | Specifica se il controllo ActiveX Desktop remoto non deve controllare il server per le funzionalità di RemoteApp.<br/> |
| [**GetRemoteMonitorsBoundingBox**](imsrdpclientnonscriptable5-getremotemonitorsboundingbox.md)<br/>       | Sola lettura<br/>  | Specifica il rettangolo di delimitazione del monitor remoto.<br/>                                                      |
| [**RemoteMonitorCount**](imsrdpclientnonscriptable5-remotemonitorcount.md)<br/>                           | Sola lettura<br/>  | Specifica il numero di monitoraggi remoti.<br/>                                                                     |
| [**RemoteMonitorLayoutMatchesLocal**](imsrdpclientnonscriptable5-remotemonitorlayoutmatcheslocal.md)<br/> | Sola lettura<br/>  | Specifica se il layout di monitoraggio remoto è identico a quello del monitoraggio locale.<br/>                             |
| [**UseMultimon**](imsrdpclientnonscriptable5-usemultimon.md)<br/>                                         | Lettura/Scrittura<br/> | Specifica se il controllo ActiveX Desktop remoto deve usare più monitor.<br/>                           |
| [**WarnAboutDirectXRedirection**](imsrdpclientnonscriptable5-warnaboutdirectxredirection.md)<br/>         | Lettura/Scrittura<br/> | Questa proprietà non viene utilizzata.<br/>                                                                                   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 è definito come C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting è definito come A0C63C30-F08D-4ab4-907c-34905D770C7D<br/> CLSID \_ MsRdpClient7 è definito come A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting è definito come 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID \_ MsRdpClient8 è definito come 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting è definito come A3BC03A0-041d-42e3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9 è definito come 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting è definito come 8B918B82-7985-4c24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 è definito come 4f6996d5-d7b1-412C-b0ff-063718566907<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

