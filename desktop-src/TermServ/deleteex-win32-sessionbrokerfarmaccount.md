---
title: Metodo DeleteEx della classe Win32_SessionBrokerFarmAccount
description: La classe \_ Win32 SessionBrokerFarmAccount non è più disponibile per l'uso a Windows Server 2012. | Metodo DeleteEx della classe Win32_SessionBrokerFarmAccount
ms.assetid: d30c5d3e-f63c-4b21-85ae-a0b8d5868d64
ms.tgt_platform: multiple
keywords:
- Metodo DeleteEx Servizi Desktop remoto
- Metodo DeleteEx Servizi Desktop remoto , Win32_SessionBrokerFarmAccount classe
- Win32_SessionBrokerFarmAccount classe Servizi Desktop remoto , metodo DeleteEx
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
ms.openlocfilehash: aa891c874c9592ed11b2aa0840913e67daa7226a93f6f746cf74c45a0454a476
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080221"
---
# <a name="deleteex-method-of-the-win32_sessionbrokerfarmaccount-class"></a>Metodo DeleteEx della classe \_ SessionBrokerFarmAccount Win32

\[La [**classe \_ Win32 SessionBrokerFarmAccount**](win32-sessionbrokerfarmaccount.md) non è più disponibile per l'uso a Windows Server 2012.\]

Elimina l'account della farm.

## <a name="syntax"></a>Sintassi


```mof
uint32 DeleteEx(
  [in] boolean DeleteComputerObject
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DeleteComputerObject* \[ Pollici\]
</dt> <dd>

Indica se l'oggetto computer associato alla farm deve essere rimosso da Active Directory.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI. Per un [elenco Servizi Desktop remoto di questi valori,](terminal-services-wmi-provider-error-codes.md) fare riferimento Servizi Desktop remoto di errore del provider WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                      |
| Fine del supporto client<br/>    | Nessuno supportato<br/>                                                              |
| Fine del supporto server<br/>    | Windows Server 2008 R2<br/>                                                      |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ SessionBrokerFarmAccount**](win32-sessionbrokerfarmaccount.md)
</dt> </dl>

 

 





