---
title: Metodo AddResources della classe Win32_TSGatewayResourceGroup
description: Aggiunge risorse al gruppo di risorse.
ms.assetid: 3210b468-6b82-4edb-ac8b-95f66a7b9328
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo AddResources
- Metodo AddResources Servizi Desktop remoto, classe Win32_TSGatewayResourceGroup
- Classe Win32_TSGatewayResourceGroup Servizi Desktop remoto, metodo AddResources
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.AddResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a37498accf76b28f16e0de45565916c18ab8d9dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517463"
---
# <a name="addresources-method-of-the-win32_tsgatewayresourcegroup-class"></a>Metodo AddResources della \_ classe TSGatewayResourceGroup Win32

Aggiunge risorse al gruppo di risorse.

## <a name="syntax"></a>Sintassi


```mof
uint32 AddResources(
  [in] string Resources
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Risorse* \[ di in\]
</dt> <dd>

Elenco di risorse separate da punto e virgola da aggiungere al gruppo di risorse. " \* " Indica tutte le risorse.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Se più risorse si trovano nel parametro *Resources* e una delle risorse non può essere elaborata, nessuna delle risorse verrà elaborata.

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

 

