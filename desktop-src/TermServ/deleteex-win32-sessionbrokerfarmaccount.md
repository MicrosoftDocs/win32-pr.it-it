---
title: Metodo DeleteEx della classe Win32_SessionBrokerFarmAccount
description: La \_ classe Win32 SessionBrokerFarmAccount non è più disponibile per l'uso in Windows Server 2012. | Metodo DeleteEx della classe Win32_SessionBrokerFarmAccount
ms.assetid: d30c5d3e-f63c-4b21-85ae-a0b8d5868d64
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo DeleteEx
- Metodo DeleteEx Servizi Desktop remoto, classe Win32_SessionBrokerFarmAccount
- Classe Win32_SessionBrokerFarmAccount Servizi Desktop remoto, metodo DeleteEx
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount.DeleteEx
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdad7b1c7af85337ace59690bb44f4309254eb76
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321188"
---
# <a name="deleteex-method-of-the-win32_sessionbrokerfarmaccount-class"></a>Metodo DeleteEx della \_ classe SessionBrokerFarmAccount Win32

\[La classe [**Win32 \_ SessionBrokerFarmAccount**](win32-sessionbrokerfarmaccount.md) non è più disponibile per l'uso in Windows Server 2012.\]

Elimina l'account farm.

## <a name="syntax"></a>Sintassi


```mof
uint32 DeleteEx(
  [in] boolean DeleteComputerObject
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DeleteComputerObject* \[ in\]
</dt> <dd>

Indica se l'oggetto computer associato alla farm deve essere rimosso dal Active Directory.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                      |
| Fine del supporto client<br/>    | Nessuno supportato<br/>                                                              |
| Fine del supporto server<br/>    | Windows Server 2008 R2<br/>                                                      |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SessionBrokerFarmAccount Win32**](win32-sessionbrokerfarmaccount.md)
</dt> </dl>

 

 





