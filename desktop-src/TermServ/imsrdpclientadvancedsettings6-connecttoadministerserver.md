---
title: Proprietà ConnectToAdministerServer di IMsRdpClientAdvancedSettings6
description: Recupera o specifica se il controllo ActiveX deve tentare di connettersi al server per scopi amministrativi.
ms.assetid: b98f9b9b-a3e7-4a3c-a7e3-e388ce53c5c9
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà ConnectToAdministerServer
- Servizi Desktop remoto proprietà ConnectToAdministerServer, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà ConnectToAdministerServer
- Servizi Desktop remoto proprietà ConnectToAdministerServer, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà ConnectToAdministerServer
- Servizi Desktop remoto proprietà ConnectToAdministerServer, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà ConnectToAdministerServer
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings6.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings6.put_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.put_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.put_ConnectToAdministerServer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9cad8d50e2e0a4c1ec18fbd33733dc394101a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048370"
---
# <a name="imsrdpclientadvancedsettings6connecttoadministerserver-property"></a>Proprietà IMsRdpClientAdvancedSettings6:: ConnectToAdministerServer

Recupera o specifica se il controllo ActiveX deve tentare di connettersi al server per scopi amministrativi.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_ConnectToAdministerServer(
  [in]  VARIANT_BOOL connectToAdministerServer
);

HRESULT get_ConnectToAdministerServer(
  [out] VARIANT_BOOL *pConnectToAdministerServer
);
```



## <a name="property-value"></a>Valore proprietà

**Variante \_ TRUE** per fare in modo che il controllo ActiveX tenti di connettersi al server per scopi amministrativi. in caso contrario, **Variant \_ false**. Il valore predefinito è **Variant \_ false**.

## <a name="remarks"></a>Commenti

Per utilizzare **ConnectToAdministerServer**, è necessario eseguire Connessione desktop remoto (RDC) client versione 6,1 o successiva.

> [!Note]  
> La versione RDC 6,1 (6.0.6001) supporta Remote Desktop Protocol 6,1. RDC 6,1 è incluso in Windows Server 2008 e Windows Vista con Service Pack 1 (SP1).

 

**ConnectToAdministerServer** consente di connettersi a una sessione di utilizzata a scopo amministrativo sul server remoto. Se il servizio ruolo host sessione Desktop remoto (host sessione Desktop remoto) è installato nel server remoto, **ConnectToAdministerServer** esegue le operazioni seguenti:

-   Disabilita Servizi Desktop remoto licenze di accesso client per la sessione.
-   Disabilita il reindirizzamento del fuso orario per la sessione.
-   Disabilita il reindirizzamento di Connessione Desktop remoto broker (gestore connessione Desktop remoto) per la sessione.
-   Disabilita il reindirizzamento del dispositivo Plug and Play per la sessione.
-   Consente di modificare il tema della sessione remota in Windows classico per la sessione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                         |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                   |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 è definito come 222c4b5d-45D9-4DF0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





