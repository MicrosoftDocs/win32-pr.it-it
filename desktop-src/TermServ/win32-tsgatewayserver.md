---
title: Win32_TSGatewayServer classe
description: Usato per Desktop remoto specifiche del server Gateway Desktop remoto.
ms.assetid: ae24b7ff-2c26-43a5-ac11-52f83225f4ee
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayServer classe Servizi Desktop remoto
- Win32_TSGatewayServer classe Servizi Desktop remoto , descritto
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43cd6c24447e7ba3bc22788484b2ac9e437ee947243c17a676728d2a336bd326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603888"
---
# <a name="win32_tsgatewayserver-class"></a>Classe \_ TSGatewayServer Win32

Usato per Desktop remoto specifiche del server Gateway Desktop remoto.

## <a name="syntax"></a>Sintassi

``` syntax
[singleton, dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServer
{
};
```

## <a name="members"></a>Members

La **classe \_ Win32 TSGatewayServer** include questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La **classe \_ Win32 TSGatewayServer** include questi metodi.



| Metodo                                                                                   | Descrizione                                                                                                                    |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**CreateSelfSignedCertificate**](createselfsignedcertificate-win32-tsgatewayserver.md) | Crea un certificato autofirmato con un nome soggetto specificato e restituisce l'hash del certificato come parametro "out".<br/> |
| [**Esportazione**](export-win32-tsgatewayserver.md)                                           | Restituisce la configurazione del server Gateway Desktop remoto come stringa XML.<br/>                                                       |
| [**Importa**](import-win32-tsgatewayserver.md)                                           | Importa una determinata configurazione nel server Gateway Desktop remoto.<br/>                                                             |



 

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



 

