---
title: Interfaccia IMsTscNonScriptable
description: Contiene proprietà e metodi correlati all'applicazione di una password Desktop remoto ActiveX controllo .
ms.assetid: b4a68e02-cce6-4fbe-98b4-0627c10f3f37
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsTscNonScriptable Servizi Desktop remoto
- Interfaccia IMsTscNonScriptable Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- IMsTscNonScriptable
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86ce3b1e921635850e9ffa713c55a812a806ac4e757e772569e7db817410ad3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770651"
---
# <a name="imstscnonscriptable-interface"></a>Interfaccia IMsTscNonScriptable

Contiene proprietà e metodi correlati all'applicazione di una password Desktop remoto ActiveX controllo .

L'uso principale **dell'interfaccia IMsTscNonScriptable** è la configurazione dell'accesso automatico tramite password ai server host sessione Desktop remoto negli scenari in cui il controllo Desktop remoto ActiveX è ospitato in un contenitore scritto personalizzato. Quando è configurato l'accesso automatico, l'utente non riceve la Windows di dialogo Accesso automatico in fase di connessione.

In alcune piattaforme è possibile usare i metodi **dell'interfaccia IMsTscNonScriptable** per specificare le password in uno dei tre formati supportati:

-   Testo non crittografato
-   Codificato portabile
-   Codificato binario (non portabile)

Si noti che una password in un formato codificato è costituita da due parti:

-   Parte della password codificata.
-   Parte del valore salt.

Entrambe le parti sono necessarie per impostare una password codificata. Né la parte della password codificata né la parte del valore salt devono essere considerate crittografate in modo sicuro.

L'accesso tramite script alle password in testo non crittografato è disponibile tramite la [**proprietà ClearTextPassword**](imsrdpclientadvancedsettings-cleartextpassword.md) dell'interfaccia [**IMsRdpClientAdvancedSettings.**](imsrdpclientadvancedsettings-interface.md)

**L'interfaccia IMsTscNonScriptable** è accessibile solo tramite vtable.

## <a name="members"></a>Membri

**L'interfaccia IMsTscNonScriptable** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMsTscNonScriptable** include anche questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia IMsTscNonScriptable** include questi metodi.



| Metodo                                                     | Descrizione                                           |
|:-----------------------------------------------------------|:------------------------------------------------------|
| [**Resetpassword**](imstscnonscriptable-resetpassword.md) | Reimposta tutti gli stati della password nel controllo .<br/> |



 

### <a name="properties"></a>Proprietà

Queste proprietà sono disponibili nell'interfaccia **IMsTscNonScriptable.**



| Proprietà                                                                      | Tipo di accesso           | Descrizione                                                                  |
|:------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------|
| [**BinaryPassword**](imstscnonscriptable-binarypassword.md)<br/>       | Lettura/Scrittura<br/> | Questa proprietà non è supportata.<br/>                                   |
| [**BinarySalt**](imstscnonscriptable-binarysalt.md)<br/>               | Lettura/Scrittura<br/> | Questa proprietà non è supportata.<br/>                                   |
| [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md)<br/> | Sola scrittura<br/> | La Desktop remoto ActiveX password di controllo, in formato testo non crittografato.<br/> |
| [**PortablePassword**](imstscnonscriptable-portablepassword.md)<br/>   | Lettura/Scrittura<br/> | Questa proprietà non è supportata.<br/>                                   |
| [**PortableSalt**](imstscnonscriptable-portablesalt.md)<br/>           | Lettura/Scrittura<br/> | Questa proprietà non è supportata.<br/>                                   |



 

## <a name="remarks"></a>Commenti

Fornire una password al controllo Desktop remoto ActiveX è facoltativo. Se si fornisce una password al controllo, è necessario applicare al controllo solo uno dei tre formati precedenti prima di avviare la connessione con una chiamata al [**metodo Connessione.**](imstscax-connect.md)

> [!Note]  
> È anche possibile abilitare l'accesso automatico nel server con lo strumento di configurazione Servizi Desktop remoto (Tscc.msc.) Un amministratore può usare questo strumento per assegnare una password specifica a una connessione in una situazione in cui è necessario un accesso automatico.

 

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

**L'interfaccia IMsTscNonScriptable** è stata estesa dalle interfacce seguenti, con ogni nuova interfaccia che eredita tutti i metodi e le proprietà delle interfacce precedenti:

-   [**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
-   [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
-   [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
-   [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| CLSID<br/>                    | CLSID MsRdpClient è definito come \_ 791fa017-2de3-492e-acc5-53c67a2b94d0<br/> CLSID \_ MsRdpClient10 è definito come C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting è definito come A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID MsRdpClient2 è definito come \_ 9059F30F-4EB1-4BD2-9FDC-36F43A218F4A<br/> CLSID MsRdpClient2a è definito come \_ 971127BB-259F-48C2-BD75-5F97A3331551<br/> CLSID \_ MsRdpClient2NotSafeForScripting è definito come 3523C2FB-4031-44E4-9A3B-F1E94986EE7F<br/> CLSID MsRdpClient3 è definito come \_ 7584C670-2274-4EFB-B00B-D6AABA6D3850<br/> CLSID MsRdpClient3a è definito come \_ 6A6F4B83-45C5-4CA9-BDD9-0D81C12295E4<br/> CLSID \_ MsRdpClient3NotSafeForScripting è definito come ACE575FD-1FCF-4074-9401-EBAB990FA9DE<br/> CLSID MsRdpClient4 è definito come \_ 4EDCB26C-D24C-4E72-AF07-B576699AC0DE<br/> CLSID MsRdpClient4a è definito come \_ 54CE37E0-9834-41AE-9896-4DAB69DC022B<br/> CLSID \_ MsRdpClient4NotSafeForScripting è definito come 6AE29350-321B-42BE-BBE5-12FB5270C0DE<br/> CLSID MsRdpClient5 è definito come \_ 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2<br/> CLSID \_ MsRdpClient5NotSafeForScripting è definito come 4EB2F086-C818-447E-B32C-C51CE2B30D31<br/> CLSID MsRdpClient6 è definito come \_ 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> CLSID \_ MsRdpClient6NotSafeForScripting è definito come D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> CLSID \_ MsRdpClient7 è definito come A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting è definito come 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID MsRdpClient8 è definito come \_ 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting è definito come A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID MsRdpClient9 è definito come \_ 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting è definito come 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> CLSID \_ MsRdpClientNotSafeForScripting è definito come 7CACBD7B-0D99-468F-AC33-22E495C0AFE5<br/> CLSID MsTscAx è definito come \_ 1FB464C8-09BB-4017-A2F5-EB742F04392F<br/> CLSID \_ MsTscAxNotSafeForScripting è definito come A41A4187-5A86-4E26-B40A-856F9035D9CB<br/> |
| IID<br/>                      | IMsTscNonScriptable IID è definito \_ come C1E6743A-41C1-4A74-832A-0DD06C1C7A0E<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Connessione Web Desktop remoto di riferimento](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsTscAx::Connessione**](imstscax-connect.md)
</dt> </dl>

 

