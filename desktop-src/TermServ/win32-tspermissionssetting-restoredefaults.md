---
title: Metodo RestoreDefaults della classe Win32_TSPermissionsSetting (Netfw.h)
description: Ripristina i valori predefiniti del set di autorizzazioni per il terminale.
ms.assetid: bdd01290-7c7c-4355-85dc-ade51b2abd94
ms.tgt_platform: multiple
keywords:
- Metodo RestoreDefaults Servizi Desktop remoto
- Metodo RestoreDefaults Servizi Desktop remoto , Win32_TSPermissionsSetting classe
- Win32_TSPermissionsSetting classe Servizi Desktop remoto , metodo RestoreDefaults
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.RestoreDefaults
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef81f4b3008f68129026a90d1b2e98e8c13c298537952175e116c9c8e02c4f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769451"
---
# <a name="restoredefaults-method-of-the-win32_tspermissionssetting-class"></a>Metodo RestoreDefaults della classe \_ TSPermissionsSetting Win32

Il **metodo RestoreDefaults** ripristina i valori predefiniti del set di autorizzazioni per il terminale.

## <a name="syntax"></a>Sintassi


```mof
uint32 RestoreDefaults();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce Success in caso di esito positivo, in caso contrario Failure.

## <a name="remarks"></a>Commenti

Le autorizzazioni predefinite sono le seguenti:

-   Gli account Administrators, System e Desktop remoto Help Assistant hanno tutte Servizi Desktop remoto [autorizzazioni](terminal-services-permissions.md).
-   L'account Desktop remoto Users dispone dell'autorizzazione Accesso, Connessione, Informazioni query e Invia messaggio.
-   Gli account Servizio locale e Servizio di rete dispongono dell'autorizzazione Query Information (Informazioni query) e Send Message (Invia messaggio).

Managed Object Format file MOF contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>Netfw.h</dt> </dl>      |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSPermissionsSetting**](win32-tspermissionssetting.md)
</dt> </dl>

 

