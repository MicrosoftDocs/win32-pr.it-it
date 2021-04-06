---
title: Metodo RestoreDefaults della classe Win32_TSPermissionsSetting (Netfw. h)
description: Ripristina i valori predefiniti del set di autorizzazioni per il terminale.
ms.assetid: bdd01290-7c7c-4355-85dc-ade51b2abd94
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del Metodo RestoreDefaults
- Metodo RestoreDefaults Servizi Desktop remoto, classe Win32_TSPermissionsSetting
- Classe Win32_TSPermissionsSetting Servizi Desktop remoto, Metodo RestoreDefaults
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
ms.openlocfilehash: 073a8f8267ab9e7f7cbd50f15f4f3f20594d2e39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873617"
---
# <a name="restoredefaults-method-of-the-win32_tspermissionssetting-class"></a>Metodo RestoreDefaults della \_ classe TSPermissionsSetting Win32

Il metodo **RestoreDefaults** Ripristina i valori predefiniti del set di autorizzazioni per il terminale.

## <a name="syntax"></a>Sintassi


```mof
uint32 RestoreDefaults();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce l'esito positivo, in caso contrario.

## <a name="remarks"></a>Commenti

Le autorizzazioni predefinite sono le seguenti:

-   Gli account amministratori, di sistema e di Desktop remoto Assistant sono dotati di [autorizzazioni di Servizi Desktop remoto](terminal-services-permissions.md).
-   L'account utenti Desktop remoto dispone dell'autorizzazione di accesso, connessione, informazioni sulle query e invio del messaggio.
-   Gli account servizio locale e servizio di rete dispongono di informazioni sulle query e dell'autorizzazione Invia messaggio.

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>Netfw. h</dt> </dl>      |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSPermissionsSetting Win32**](win32-tspermissionssetting.md)
</dt> </dl>

 

