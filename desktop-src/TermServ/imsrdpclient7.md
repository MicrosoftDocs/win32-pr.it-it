---
title: Interfaccia IMsRdpClient7
description: Fornisce i metodi e le proprietà necessari per configurare e usare il controllo client. Deriva dall'interfaccia IMsRdpClient6.
ms.assetid: f6bc5d50-f16a-44be-8244-5aec13c52066
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClient7 Servizi Desktop remoto
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpClient7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e16375f9f1281f2cc34dac440373f95b828392f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302745"
---
# <a name="imsrdpclient7-interface"></a>Interfaccia IMsRdpClient7

Fornisce i metodi e le proprietà necessari per configurare e usare il controllo client. Deriva dall'interfaccia [**IMsRdpClient6**](imsrdpclient6.md) .

## <a name="members"></a>Membri

L'interfaccia **IMsRdpClient7** eredita da [**IMsRdpClient6**](imsrdpclient6.md). **IMsRdpClient7** dispone anche di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IMsRdpClient7** dispone di questi metodi.



| Metodo                                               | Descrizione                                                         |
|:-----------------------------------------------------|:--------------------------------------------------------------------|
| [**GetStatusText**](imsrdpclient7-getstatustext.md) | Recupera il testo di stato per il codice di stato specificato.<br/> |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IMsRdpClient7** ha queste proprietà.



| Proprietà                                                                  | Tipo di accesso          | Descrizione                                                                                                                |
|:--------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings8**](imsrdpclient7-advancedsettings8.md)<br/>   | Sola lettura<br/> | Oggetto che supporta l'interfaccia [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) .<br/>   |
| [**RemoteProgram2**](imsrdpclient7-remoteprogram2.md)<br/>         | Sola lettura<br/> | Oggetto che supporta l'interfaccia [**ITSRemoteProgram2**](itsremoteprogram2.md) .<br/>                           |
| [**SecuredSettings3**](imsrdpclient7-securedsettings3.md)<br/>     | Sola lettura<br/> | Oggetto che supporta l'interfaccia [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) .<br/>     |
| [**TransportSettings3**](imsrdpclient7-transportsettings3.md)<br/> | Sola lettura<br/> | Oggetto che supporta l'interfaccia [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) .<br/> |



 

## <a name="remarks"></a>Commenti

L'interfaccia **IMsRdpClient7** è stata estesa dalle interfacce seguenti, in cui ogni nuova interfaccia eredita tutti i metodi e le proprietà delle interfacce precedenti:

-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient10**](imsrdpclient10.md)

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 è definito come C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting è definito come A0C63C30-F08D-4ab4-907c-34905D770C7D<br/> CLSID \_ MsRdpClient7 è definito come A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting è definito come 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID \_ MsRdpClient8 è definito come 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting è definito come A3BC03A0-041d-42e3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9 è definito come 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting è definito come 8B918B82-7985-4c24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClient7 è definito come b2a5b5ce-3461-444A-91D4-add26d070638<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[Riferimento Connessione Web Desktop remoto](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





