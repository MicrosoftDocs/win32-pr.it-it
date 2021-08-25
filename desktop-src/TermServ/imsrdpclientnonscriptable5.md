---
title: Interfaccia IMsRdpClientNonScriptable5
description: Fornisce l'accesso alle proprietà non scriptable della sessione remota di un client nel Desktop remoto ActiveX controllo . Deriva dall'interfaccia IMsRdpClientNonScriptable4.
ms.assetid: 41b8c624-0451-4a7e-bc80-d0bf269e33c6
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto , descritta
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
ms.openlocfilehash: ddb7f3407f0dc6b1bc8dc04c6c4a72cda95db6b6b1def088a18908a730b96600
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009801"
---
# <a name="imsrdpclientnonscriptable5-interface"></a>Interfaccia IMsRdpClientNonScriptable5

Fornisce l'accesso alle proprietà non scriptable della sessione remota di un client nel Desktop remoto ActiveX controllo . Deriva [**dall'interfaccia IMsRdpClientNonScriptable4.**](imsrdpclientnonscriptable4.md) I metodi di questa interfaccia sono accessibili solo tramite vtable. non sono disponibili per l'uso per i client che supportano lo script.

Un'istanza di questa interfaccia viene ottenuta chiamando [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) [**sull'oggetto IMsTscAx,**](imstscax-interface.md) passando **IID \_ IMsRdpClientNonScriptable5.**

## <a name="members"></a>Membri

**L'interfaccia IMsRdpClientNonScriptable5** eredita da [**IMsRdpClientNonScriptable4.**](imsrdpclientnonscriptable4.md) **IMsRdpClientNonScriptable5** include anche questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'interfaccia IMsRdpClientNonScriptable5** ha queste proprietà.



| Proprietà                                                                                                         | Tipo di accesso           | Descrizione                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**AllowPromptingForCredentials**](imsrdpclientnonscriptable5-allowpromptingforcredentials.md)<br/>       | Lettura/Scrittura<br/> | Specifica se il controllo Desktop remoto ActiveX può richiedere le credenziali all'utente.<br/>                    |
| [**DisableConnectionBar**](imsrdpclientnonscriptable5-disableconnectionbar.md)<br/>                       | Sola scrittura<br/> | Specifica se il controllo Desktop remoto ActiveX deve disabilitare la barra delle connessioni.<br/>                      |
| [**DisableRemoteAppCapsCheck**](imsrdpclientnonscriptable5-disableremoteappcapscheck.md)<br/>             | Lettura/Scrittura<br/> | Specifica se il Desktop remoto ActiveX controllo non deve verificare la presenza di funzionalità RemoteApp nel server.<br/> |
| [**GetRemoteMonitorsBoundingBox**](imsrdpclientnonscriptable5-getremotemonitorsboundingbox.md)<br/>       | Sola lettura<br/>  | Specifica il rettangolo di delimitazione del monitor remoto.<br/>                                                      |
| [**RemoteMonitorCount**](imsrdpclientnonscriptable5-remotemonitorcount.md)<br/>                           | Sola lettura<br/>  | Specifica il numero di monitoraggi remoti.<br/>                                                                     |
| [**RemoteMonitorLayoutMatchesLocal**](imsrdpclientnonscriptable5-remotemonitorlayoutmatcheslocal.md)<br/> | Sola lettura<br/>  | Specifica se il layout del monitor remoto è identico al layout del monitor locale.<br/>                             |
| [**UseMultimon**](imsrdpclientnonscriptable5-usemultimon.md)<br/>                                         | Lettura/Scrittura<br/> | Specifica se il Desktop remoto ActiveX deve utilizzare più monitor.<br/>                           |
| [**WarnAboutDirectXRedirection**](imsrdpclientnonscriptable5-warnaboutdirectxredirection.md)<br/>         | Lettura/Scrittura<br/> | Questa proprietà non viene utilizzata.<br/>                                                                                   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 è definito come C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting è definito come A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID \_ MsRdpClient7 è definito come A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting è definito come 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID \_ MsRdpClient8 è definito come 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting è definito come A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9 è definito come 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting è definito come 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 è definito come 4f6996d5-d7b1-412c-b0ff-063718566907<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

