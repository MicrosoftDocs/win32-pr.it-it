---
title: Interfaccia IMsRdpClient
description: Fornisce i metodi e le proprietà necessari per configurare e usare il controllo client. Deriva dall'interfaccia IMsTscAx.
ms.assetid: 6698c1d7-94d2-453c-96db-366113b95dd4
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClient Servizi Desktop remoto
- Interfaccia IMsRdpClient Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpClient
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc6d3a1de6a6cd18004ff957ea0f8c4d7c23b14d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301000"
---
# <a name="imsrdpclient-interface"></a>Interfaccia IMsRdpClient

Fornisce i metodi e le proprietà necessari per configurare e usare il controllo client. Deriva dall'interfaccia [**IMsTscAx**](imstscax-interface.md) .

## <a name="members"></a>Membri

L'interfaccia **IMsRdpClient** eredita da [**IMsTscAx**](imstscax-interface.md). **IMsRdpClient** dispone anche di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IMsRdpClient** dispone di questi metodi.



| Metodo                                                                    | Descrizione                                                         |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md) | Recupera le opzioni impostate per un canale virtuale.<br/>         |
| [**RequestClose**](imsrdpclient-requestclose.md)                         | Richiede un arresto normale del controllo client.<br/>      |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md) | Imposta le opzioni del canale virtuale per il controllo client.<br/> |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IMsRdpClient** ha queste proprietà.



| Proprietà                                                                             | Tipo di accesso           | Descrizione                                                                                                                                                               |
|:-------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>               | Sola lettura<br/>  | Puntatore all'interfaccia [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) , utilizzata per impostare le impostazioni avanzate per il controllo client.<br/> |
| [**ColorDepth**](imsrdpclient-colordepth.md)<br/>                             | Lettura/Scrittura<br/> | Profondità di colore del controllo corrente.<br/>                                                                                                                            |
| [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md)<br/> | Sola lettura<br/>  | Informazioni estese sul motivo del controllo client per la disconnessione.<br/>                                                                                      |
| [**FullScreen**](imsrdpclient-fullscreen.md)<br/>                             | Lettura/Scrittura<br/> | Indica se il controllo è in modalità schermo intero.<br/>                                                                                                          |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                 | Sola lettura<br/>  | Puntatore all'interfaccia [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) , utilizzata per impostare le impostazioni protette per il controllo client.<br/>    |



 

## <a name="remarks"></a>Commenti

L'interfaccia **IMsRdpClient** è stata estesa dalle interfacce seguenti, in cui ogni nuova interfaccia eredita tutti i metodi e le proprietà delle interfacce precedenti:

-   [**IMsRdpClient2**](imsrdpclient2.md)
-   [**IMsRdpClient3**](imsrdpclient3.md)
-   [**IMsRdpClient4**](imsrdpclient4.md)
-   [**IMsRdpClient5**](imsrdpclient5.md)
-   [**IMsRdpClient6**](imsrdpclient6.md)
-   [**IMsRdpClient7**](imsrdpclient7.md)
-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient10**](imsrdpclient10.md)

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| CLSID<br/>                    | CLSID \_ MsRdpClient è definito come 791fa017-2de3-492e-acc5-53c67a2b94d0<br/> CLSID \_ MsRdpClient10 è definito come C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting è definito come A0C63C30-F08D-4ab4-907c-34905D770C7D<br/> CLSID \_ MsRdpClient2 è definito come 9059F30F-4EB1-4bd2-9FDC-36F43A218F4A<br/> CLSID \_ MsRdpClient2a è definito come 971127BB-259F-48C2-BD75-5F97A3331551<br/> CLSID \_ MsRdpClient2NotSafeForScripting è definito come 3523C2FB-4031-44E4-9A3B-F1E94986EE7F<br/> CLSID \_ MsRdpClient3 è definito come 7584c670-2274-4efb-b00b-d6aaba6d3850<br/> CLSID \_ MsRdpClient3a è definito come 6A6F4B83-45C5-4CA9-BDD9-0D81C12295E4<br/> CLSID \_ MsRdpClient3NotSafeForScripting è definito come ACE575FD-1FCF-4074-9401-EBAB990FA9DE<br/> CLSID \_ MsRdpClient4 è definito come 4EDCB26C-D24C-4e72-AF07-B576699AC0DE<br/> CLSID \_ MsRdpClient4a è definito come 54CE37E0-9834-41AE-9896-4DAB69DC022B<br/> CLSID \_ MsRdpClient4NotSafeForScripting è definito come 6AE29350-321B-42BE-BBE5-12FB5270C0DE<br/> CLSID \_ MsRdpClient5 è definito come 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2<br/> CLSID \_ MsRdpClient5NotSafeForScripting è definito come 4EB2F086-C818-447E-B32C-C51CE2B30D31<br/> CLSID \_ MsRdpClient6 è definito come 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> CLSID \_ MsRdpClient6NotSafeForScripting è definito come D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> CLSID \_ MsRdpClient7 è definito come A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting è definito come 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID \_ MsRdpClient8 è definito come 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting è definito come A3BC03A0-041d-42e3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9 è definito come 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting è definito come 8B918B82-7985-4c24-89DF-C33AD2BBFBCD<br/> CLSID \_ MsRdpClientNotSafeForScripting è definito come 7CACBD7B-0D99-468f-AC33-22E495C0AFE5<br/> CLSID \_ MsTscAx è definito come 1FB464C8-09bb-4017-a2f5-EB742F04392F<br/> CLSID \_ MsTscAxNotSafeForScripting è definito come A41A4187-5A86-4e26-B40A-856F9035D9CB<br/> |
| IID<br/>                      | IID \_ IMsRdpClient è definito come 92b4a539-7115-4B7C-a5a9-e5d9efc2780a<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[Riferimento Connessione Web Desktop remoto](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





