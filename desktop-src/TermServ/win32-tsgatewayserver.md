---
title: Classe Win32_TSGatewayServer
description: Usato per le operazioni specifiche del server Desktop remoto Gateway (Gateway Desktop remoto).
ms.assetid: ae24b7ff-2c26-43a5-ac11-52f83225f4ee
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSGatewayServer Servizi Desktop remoto
- Classe Win32_TSGatewayServer Servizi Desktop remoto, descritta
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
ms.openlocfilehash: b7dee009521c59b606010be085fcb0447558898d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476384"
---
# <a name="win32_tsgatewayserver-class"></a>Win32 \_ TSGatewayServer (classe)

Usato per le operazioni specifiche del server Desktop remoto Gateway (Gateway Desktop remoto).

## <a name="syntax"></a>Sintassi

``` syntax
[singleton, dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServer
{
};
```

## <a name="members"></a>Members

La classe **Win32 \_ TSGatewayServer** presenta questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La classe **Win32 \_ TSGatewayServer** presenta questi metodi.



| Metodo                                                                                   | Descrizione                                                                                                                    |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**CreateSelfSignedCertificate**](createselfsignedcertificate-win32-tsgatewayserver.md) | Crea un certificato autofirmato con un nome oggetto specificato e restituisce l'hash del certificato come parametro "out".<br/> |
| [**Esportazione**](export-win32-tsgatewayserver.md)                                           | Restituisce la configurazione del server Gateway Desktop remoto come stringa XML.<br/>                                                       |
| [**Importa**](import-win32-tsgatewayserver.md)                                           | Importa una determinata configurazione nel server Gateway Desktop remoto.<br/>                                                             |



 

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



 

