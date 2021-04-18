---
title: Interfaccia IMsTscNonScriptable
description: Contiene proprietà e metodi correlati all'applicazione di una password per il controllo ActiveX Desktop remoto.
ms.assetid: b4a68e02-cce6-4fbe-98b4-0627c10f3f37
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsTscNonScriptable Servizi Desktop remoto
- Interfaccia IMsTscNonScriptable Servizi Desktop remoto, descritta
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
ms.openlocfilehash: 92372f7ea9479f7fcdd632546a0bd7dd2f0b465e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301109"
---
# <a name="imstscnonscriptable-interface"></a>Interfaccia IMsTscNonScriptable

Contiene proprietà e metodi correlati all'applicazione di una password per il controllo ActiveX Desktop remoto.

L'uso principale dell'interfaccia **IMsTscNonScriptable** consiste nel configurare l'accesso automatico alle password ai server Host sessione Desktop remoto (host sessione Desktop remoto) negli scenari in cui il controllo ActiveX Desktop remoto è ospitato in un contenitore scritto in modo personalizzato. Quando si configura l'accesso automatico, l'utente non riceve la finestra di dialogo di accesso di Windows in fase di connessione.

In alcune piattaforme, i metodi dell'interfaccia **IMsTscNonScriptable** possono essere usati per specificare le password in uno dei tre formati supportati:

-   Testo non crittografato
-   Codifica portatile
-   Codificata (non portabile) binaria

Si noti che una password in un formato codificato è costituita da due parti:

-   Parte della password codificata.
-   Parte valore salt.

Per impostare una password codificata, sono necessarie entrambe le parti. Né la parte della password codificata né la parte del valore salt devono essere considerate crittografate in modo sicuro.

L'accesso tramite script alle password in testo non crittografato è disponibile tramite la proprietà [**ClearTextPassword**](imsrdpclientadvancedsettings-cleartextpassword.md) dell'interfaccia generabile tramite script [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md).

È possibile accedere all'interfaccia **IMsTscNonScriptable** solo tramite vtable.

## <a name="members"></a>Membri

L'interfaccia **IMsTscNonScriptable** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMsTscNonScriptable** dispone anche di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IMsTscNonScriptable** dispone di questi metodi.



| Metodo                                                     | Descrizione                                           |
|:-----------------------------------------------------------|:------------------------------------------------------|
| [**ResetPassword**](imstscnonscriptable-resetpassword.md) | Reimposta tutti gli Stati delle password nel controllo.<br/> |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IMsTscNonScriptable** ha queste proprietà.



| Proprietà                                                                      | Tipo di accesso           | Descrizione                                                                  |
|:------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------|
| [**BinaryPassword**](imstscnonscriptable-binarypassword.md)<br/>       | Lettura/Scrittura<br/> | Questa proprietà non è supportata.<br/>                                   |
| [**BinarySalt**](imstscnonscriptable-binarysalt.md)<br/>               | Lettura/Scrittura<br/> | Questa proprietà non è supportata.<br/>                                   |
| [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md)<br/> | Sola scrittura<br/> | Password del controllo ActiveX Desktop remoto in formato testo non crittografato.<br/> |
| [**PortablePassword**](imstscnonscriptable-portablepassword.md)<br/>   | Lettura/Scrittura<br/> | Questa proprietà non è supportata.<br/>                                   |
| [**PortableSalt**](imstscnonscriptable-portablesalt.md)<br/>           | Lettura/Scrittura<br/> | Questa proprietà non è supportata.<br/>                                   |



 

## <a name="remarks"></a>Commenti

La specifica di una password per il controllo ActiveX Desktop remoto è facoltativa. Se si specifica una password per il controllo, è necessario applicare al controllo solo uno dei tre formati precedenti prima di avviare la connessione con una chiamata al metodo [**Connect**](imstscax-connect.md) .

> [!Note]  
> È inoltre possibile abilitare l'accesso automatico al server con lo strumento di configurazione Servizi Desktop remoto (TSCC. msc). un amministratore può utilizzare questo strumento per assegnare una password specifica a una connessione in una situazione in cui è necessario un accesso automatizzato.

 

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

L'interfaccia **IMsTscNonScriptable** è stata estesa dalle interfacce seguenti, in cui ogni nuova interfaccia eredita tutti i metodi e le proprietà delle interfacce precedenti:

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
| CLSID<br/>                    | CLSID \_ MsRdpClient è definito come 791fa017-2de3-492e-acc5-53c67a2b94d0<br/> CLSID \_ MsRdpClient10 è definito come C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting è definito come A0C63C30-F08D-4ab4-907c-34905D770C7D<br/> CLSID \_ MsRdpClient2 è definito come 9059F30F-4EB1-4bd2-9FDC-36F43A218F4A<br/> CLSID \_ MsRdpClient2a è definito come 971127BB-259F-48C2-BD75-5F97A3331551<br/> CLSID \_ MsRdpClient2NotSafeForScripting è definito come 3523C2FB-4031-44E4-9A3B-F1E94986EE7F<br/> CLSID \_ MsRdpClient3 è definito come 7584c670-2274-4efb-b00b-d6aaba6d3850<br/> CLSID \_ MsRdpClient3a è definito come 6A6F4B83-45C5-4CA9-BDD9-0D81C12295E4<br/> CLSID \_ MsRdpClient3NotSafeForScripting è definito come ACE575FD-1FCF-4074-9401-EBAB990FA9DE<br/> CLSID \_ MsRdpClient4 è definito come 4EDCB26C-D24C-4e72-AF07-B576699AC0DE<br/> CLSID \_ MsRdpClient4a è definito come 54CE37E0-9834-41AE-9896-4DAB69DC022B<br/> CLSID \_ MsRdpClient4NotSafeForScripting è definito come 6AE29350-321B-42BE-BBE5-12FB5270C0DE<br/> CLSID \_ MsRdpClient5 è definito come 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2<br/> CLSID \_ MsRdpClient5NotSafeForScripting è definito come 4EB2F086-C818-447E-B32C-C51CE2B30D31<br/> CLSID \_ MsRdpClient6 è definito come 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> CLSID \_ MsRdpClient6NotSafeForScripting è definito come D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> CLSID \_ MsRdpClient7 è definito come A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting è definito come 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID \_ MsRdpClient8 è definito come 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting è definito come A3BC03A0-041d-42e3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9 è definito come 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting è definito come 8B918B82-7985-4c24-89DF-C33AD2BBFBCD<br/> CLSID \_ MsRdpClientNotSafeForScripting è definito come 7CACBD7B-0D99-468f-AC33-22E495C0AFE5<br/> CLSID \_ MsTscAx è definito come 1FB464C8-09bb-4017-a2f5-EB742F04392F<br/> CLSID \_ MsTscAxNotSafeForScripting è definito come A41A4187-5A86-4e26-B40A-856F9035D9CB<br/> |
| IID<br/>                      | IID \_ IMsTscNonScriptable è definito come C1E6743A-41C1-4A74-832A-0DD06C1C7A0E<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Riferimento Connessione Web Desktop remoto](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsTscAx:: Connect**](imstscax-connect.md)
</dt> </dl>

 

