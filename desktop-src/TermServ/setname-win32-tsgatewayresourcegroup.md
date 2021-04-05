---
title: Metodo Sename della classe Win32_TSGatewayResourceGroup
description: Imposta la proprietà Name per il gruppo di risorse.
ms.assetid: 2c2fe1b6-5826-490e-aec2-479a0191e215
ms.tgt_platform: multiple
keywords:
- Metodo senamer Servizi Desktop remoto
- Metodo senamer Servizi Desktop remoto, classe Win32_TSGatewayResourceGroup
- Classe Win32_TSGatewayResourceGroup Servizi Desktop remoto, metodo SetValue
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac9ea16eb82896bb8fad67fff7ed849308100726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873809"
---
# <a name="setname-method-of-the-win32_tsgatewayresourcegroup-class"></a>Metodo Sename della classe Win32 \_ TSGatewayResourceGroup

Imposta la proprietà **Name** per il gruppo di risorse.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetName(
  [in] string Name
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome* \[ in\]
</dt> <dd>

Nome del gruppo di risorse. Il nome deve essere composto da un massimo di 64 caratteri, univoco (caso ignorato) e non può contenere i caratteri riservati seguenti:

<> :; " / \\ \| ? \*\[Scheda\]

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSGatewayResourceGroup Win32**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

