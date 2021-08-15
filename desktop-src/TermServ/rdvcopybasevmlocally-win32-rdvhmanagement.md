---
title: Metodo RdvCopyBaseVmLocally della classe Win32_RdvhManagement
description: Copia una macchina virtuale di base locale in un server host RDV (Remote Desktop Virtualization) specificato.
ms.assetid: 13c0c629-42c6-4689-9740-f13f31688e42
ms.tgt_platform: multiple
keywords:
- Metodo RdvCopyBaseVmLocally Servizi Desktop remoto
- Metodo RdvCopyBaseVmLocally Servizi Desktop remoto , Win32_RdvhManagement classe
- Win32_RdvhManagement classe Servizi Desktop remoto , metodo RdvCopyBaseVmLocally
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvCopyBaseVmLocally
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76c260f8e9b659ac6e1316fc699ab832174a4aa0d0c24df26daecf5a4895ccd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118852626"
---
# <a name="rdvcopybasevmlocally-method-of-the-win32_rdvhmanagement-class"></a>Metodo RdvCopyBaseVmLocally della classe \_ RdvhManagement Win32

Copia una macchina virtuale di base locale in un server host RDV (Remote Desktop Virtualization) specificato.

## <a name="syntax"></a>Sintassi


```mof
uint32 RdvCopyBaseVmLocally(
  [in] string BaseVmLocation,
  [in] string FarmName,
  [in] string GoldCacheLocation
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*BaseVmLocation* \[ Pollici\]
</dt> <dd>

Percorso della macchina virtuale di base.

</dd> <dt>

*FarmName* \[ Pollici\]
</dt> <dd>

Nome della farm host in cui copiare.

</dd> <dt>

*GoldCacheLocation* \[ Pollici\]
</dt> <dd>

Posizione della cache gold.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Fare riferimento [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) per un elenco di questi valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                             |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost.mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RdvhManagement**](win32-rdvhmanagement.md)
</dt> </dl>

 

 





