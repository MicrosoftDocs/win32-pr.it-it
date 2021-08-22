---
title: Interfaccia IMsRdpClient6
description: Fornisce i metodi e le proprietà necessari per configurare e usare il controllo client. Deriva dall'interfaccia IMsRdpClient5.
ms.assetid: 97ec885f-1c55-4293-84d0-2d1d804a9df8
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClient6 Servizi Desktop remoto
- Interfaccia IMsRdpClient6 Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- IMsRdpClient6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4bbf8fb9cc532b1968b8fba99b62e49feaf4538fd618018666d0338736cc04d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138914"
---
# <a name="imsrdpclient6-interface"></a>Interfaccia IMsRdpClient6

Fornisce i metodi e le proprietà necessari per configurare e usare il controllo client. Deriva [**dall'interfaccia IMsRdpClient5.**](imsrdpclient5.md)

## <a name="members"></a>Membri

**L'interfaccia IMsRdpClient6** eredita da [**IMsRdpClient5.**](imsrdpclient5.md) **IMsRdpClient6** include anche questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

Queste proprietà sono disponibili nell'interfaccia **IMsRdpClient6.**



| Proprietà                                                                  | Tipo di accesso          | Descrizione                                                                                           |
|:--------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------|
| [**Impostazioni avanzate7**](imsrdpclient6-advancedsettings7.md)<br/>   | Sola lettura<br/> | Interfaccia di [**IMsRdpClientAdvancedSettings6.**](imsrdpclientadvancedsettings6.md)<br/>   |
| [**TransportSettings2**](imsrdpclient6-transportsettings2.md)<br/> | Sola lettura<br/> | Interfaccia di [**IMsRdpClientTransportSettings2.**](imsrdpclienttransportsettings2.md)<br/> |



 

## <a name="remarks"></a>Commenti

**L'interfaccia IMsRdpClient6** è stata estesa dalle interfacce seguenti, con ogni nuova interfaccia che eredita tutti i metodi e le proprietà delle interfacce precedenti:

-   [**IMsRdpClient7**](imsrdpclient7.md)
-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient10**](imsrdpclient10.md)

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista con SP1<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 è definito come C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting è definito come A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID MsRdpClient6 è definito come \_ 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> CLSID \_ MsRdpClient6NotSafeForScripting è definito come D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> CLSID \_ MsRdpClient7 è definito come A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting è definito come 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID MsRdpClient8 è definito come \_ 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting è definito come A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID MsRdpClient9 è definito come \_ 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting è definito come 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IMsRdpClient6 IID è definito come \_ d43b7d80-8517-4b6d-9eac-96ad6800d7f2<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

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

[Connessione Web Desktop remoto riferimento](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





