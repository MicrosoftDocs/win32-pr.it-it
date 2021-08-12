---
title: Interfaccia IMsRdpClient5
description: Fornisce i metodi e le proprietà necessari per configurare e usare il controllo client. Deriva dall'interfaccia IMsRdpClient4.
ms.assetid: d3fc5e67-f4d9-4d80-b572-8fc3e660571e
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClient5 Servizi Desktop remoto
- Interfaccia IMsRdpClient5 Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- IMsRdpClient5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7948d402219faa930ddc9087af1ba387bde3ce8d70752fd842a364e85b41abb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118609292"
---
# <a name="imsrdpclient5-interface"></a>Interfaccia IMsRdpClient5

Fornisce i metodi e le proprietà necessari per configurare e usare il controllo client. Deriva [**dall'interfaccia IMsRdpClient4.**](imsrdpclient4.md)

## <a name="members"></a>Membri

**L'interfaccia IMsRdpClient5** eredita da [**IMsRdpClient4.**](imsrdpclient4.md) **IMsRdpClient5** include anche questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia IMsRdpClient5** include questi metodi.



| Metodo                                                           | Descrizione                                              |
|:-----------------------------------------------------------------|:---------------------------------------------------------|
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md) | Recupera i codici di errore e i messaggi di errore.<br/> |



 

### <a name="properties"></a>Proprietà

Queste proprietà sono disponibili nell'interfaccia **IMsRdpClient5.**



| Proprietà                                                                | Tipo di accesso          | Descrizione                                                                                         |
|:------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------|
| [**Impostazioni avanzate6**](imsrdpclient5-advancedsettings6.md)<br/> | Sola lettura<br/> | Interfaccia di [**IMsRdpClientAdvancedSettings5.**](imsrdpclientadvancedsettings5.md)<br/> |
| [**MsRdpClientShell**](imsrdpclient5-msrdpclientshell.md)<br/>   | Sola lettura<br/> | Impostazioni client per l'utilità di avvio del portale Web.<br/>                                         |
| [**RemoteProgram**](imsrdpclient5-remoteprogram.md)<br/>         | Sola lettura<br/> | Impostazione remoteApp client.<br/>                                                            |
| [**TransportSettings**](imsrdpclient5-transportsettings.md)<br/> | Sola lettura<br/> | Impostazione di Gateway Desktop remoto client.<br/>                                                           |



 

## <a name="remarks"></a>Commenti

**L'interfaccia IMsRdpClient5** è stata estesa dalle interfacce seguenti, con ogni nuova interfaccia che eredita tutti i metodi e le proprietà delle interfacce precedenti:

-   [**IMsRdpClient6**](imsrdpclient6.md)
-   [**IMsRdpClient7**](imsrdpclient7.md)
-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient10**](imsrdpclient10.md)

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 è definito come C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting è definito come A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID MsRdpClient5 è definito come \_ 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2<br/> CLSID \_ MsRdpClient5NotSafeForScripting è definito come 4EB2F086-C818-447E-B32C-C51CE2B30D31<br/> CLSID MsRdpClient6 è definito come \_ 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> CLSID \_ MsRdpClient6NotSafeForScripting è definito come D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> CLSID \_ MsRdpClient7 è definito come A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting è definito come 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID MsRdpClient8 è definito come \_ 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting è definito come A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID MsRdpClient9 è definito come \_ 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting è definito come 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID IMsRdpClient5 è definito come \_ 4eb5335b-6429-477d-b922-e06a28ecd8bf<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

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

[Connessione Web Desktop remoto riferimento](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





