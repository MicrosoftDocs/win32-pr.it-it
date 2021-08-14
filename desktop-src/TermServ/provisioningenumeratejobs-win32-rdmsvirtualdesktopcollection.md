---
title: Metodo ProvisioningEnumerateJobs della Win32_RDMSVirtualDesktopCollection classe
description: Enumera i processi di provisioning di desktop virtuali per questo servizio.
ms.assetid: 4bd2b03f-ba8c-483e-af09-270424f9b1ed
ms.tgt_platform: multiple
keywords:
- Metodo ProvisioningEnumerateJobs Servizi Desktop remoto
- Metodo ProvisioningEnumerateJobs Servizi Desktop remoto , Win32_RDMSVirtualDesktopCollection classe
- Win32_RDMSVirtualDesktopCollection classe Servizi Desktop remoto , metodo ProvisioningEnumerateJobs
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningEnumerateJobs
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b24ef80acdb29c75327447f61db7dae1689a883f69c9e19ef199710de216fc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118350223"
---
# <a name="provisioningenumeratejobs-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Metodo ProvisioningEnumerateJobs della classe \_ WIN32 RDMSVirtualDesktopCollection

Enumera i processi di provisioning di desktop virtuali per questo servizio.

## <a name="syntax"></a>Sintassi


```mof
uint32 ProvisioningEnumerateJobs(
  [in]  uint32 JobType,
  [in]  string CollectionAlias,
  [out] string JobGuids[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tipo di processo* \[ Pollici\]
</dt> <dd>

Intero che specifica il tipo di processo da enumerare.

Questo parametro può essere impostato su uno dei valori seguenti:

<dt>

0
</dt> <dd>

Processi in esecuzione

</dd> <dt>

1
</dt> <dd>

Processi completati

</dd> </dl> </dd> <dt>

*CollectionAlias* \[ Pollici\]
</dt> <dd>

Alias dell'insieme di desktop virtuali da enumerare. Il valore predefinito per questo parametro è FALSE, che specifica che tutti i processi in esecuzione devono essere enumerati.

</dd> <dt>

*JobGuids* \[ Cambio\]
</dt> <dd>

Matrice che contiene i GUID **dei processi di** provisioning da enumerare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Root \\ CIMv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktopCollection**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





