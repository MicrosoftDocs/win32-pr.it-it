---
title: Metodo TSGStoreAdminMsg della classe Win32_TSGatewayServerSettings
description: Aggiorna il messaggio amministrativo per il server gateway.
ms.assetid: 84e5b967-12fd-47a7-93e4-2550c15c4491
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo TSGStoreAdminMsg
- Metodo TSGStoreAdminMsg Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo TSGStoreAdminMsg
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGStoreAdminMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 398a027d28970b28b4a1e7db37b5fbfee06e881e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873921"
---
# <a name="tsgstoreadminmsg-method-of-the-win32_tsgatewayserversettings-class"></a>Metodo TSGStoreAdminMsg della \_ classe TSGatewayServerSettings Win32

Aggiorna il messaggio amministrativo per il server gateway.

## <a name="syntax"></a>Sintassi


```mof
uint32 TSGStoreAdminMsg(
  [in] string TSGAdmMsg,
  [in] string MsgStartTime,
  [in] string MsgEndTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TSGAdmMsg* \[ in\]
</dt> <dd>

Tipo: **stringa**

Testo del messaggio amministrativo.

</dd> <dt>

*MsgStartTime* \[ in\]
</dt> <dd>

Tipo: **stringa**

Ora di inizio del messaggio amministrativo.

</dd> <dt>

*MsgEndTime* \[ in\]
</dt> <dd>

Tipo: **stringa**

Ora di fine del messaggio amministrativo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                        |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

