---
title: Metodo sedescription della classe Win32_TSGatewayResourceGroup
description: Imposta la proprietà Description per il gruppo di risorse.
ms.assetid: ab1280c7-ce53-4807-9537-953b597dd636
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto metodo di descrizione
- Metodo sedescription Servizi Desktop remoto, classe Win32_TSGatewayResourceGroup
- Classe Win32_TSGatewayResourceGroup Servizi Desktop remoto, metodo sedescription
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetDescription
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d815cc5400a182f2dff3b982643d5e6bfd861002
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302595"
---
# <a name="setdescription-method-of-the-win32_tsgatewayresourcegroup-class"></a>Metodo sedescription della classe Win32 \_ TSGatewayResourceGroup

Imposta la proprietà **Description** per il gruppo di risorse.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetDescription(
  [in] string Description
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Descrizione* \[ di in\]
</dt> <dd>

Descrizione del gruppo di risorse.

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

 

