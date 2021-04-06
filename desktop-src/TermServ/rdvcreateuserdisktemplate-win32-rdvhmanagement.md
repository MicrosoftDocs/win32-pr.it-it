---
title: Metodo RdvCreateUserDiskTemplate della classe Win32_RdvhManagement
description: Crea un modello di disco utente, con la dimensione massima specificata, nella posizione specificata.
ms.assetid: b8ca8b8c-58fd-44fc-9a88-5d7d41ef96a2
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RdvCreateUserDiskTemplate
- Metodo RdvCreateUserDiskTemplate Servizi Desktop remoto, classe Win32_RdvhManagement
- Classe Win32_RdvhManagement Servizi Desktop remoto, metodo RdvCreateUserDiskTemplate
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvCreateUserDiskTemplate
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cdc7fec869fa4ffde9ac0a5a724f73b04b84351
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743287"
---
# <a name="rdvcreateuserdisktemplate-method-of-the-win32_rdvhmanagement-class"></a>Metodo RdvCreateUserDiskTemplate della \_ classe RdvhManagement Win32

Crea un modello di disco utente, con la dimensione massima specificata, nella posizione specificata.

## <a name="syntax"></a>Sintassi


```mof
uint32 RdvCreateUserDiskTemplate(
  [in] string UserDisksStorageUrl,
  [in] uint32 UserDiskMaxSizeInGB
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*UserDisksStorageUrl* \[ in\]
</dt> <dd>

Percorso dell'archiviazione su disco dell'utente.

</dd> <dt>

*UserDiskMaxSizeInGB* \[ in\]
</dt> <dd>

Dimensioni massime del disco utente, in GB.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Commenti

Tutti i dischi utente creati con questo modello avranno le stesse dimensioni massime del modello.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                             |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_RdvhManagement Win32**](win32-rdvhmanagement.md)
</dt> </dl>

 

 





