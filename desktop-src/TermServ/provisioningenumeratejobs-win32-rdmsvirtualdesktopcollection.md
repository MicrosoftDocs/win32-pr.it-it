---
title: Metodo ProvisioningEnumerateJobs della classe Win32_RDMSVirtualDesktopCollection
description: Enumera i processi di provisioning del desktop virtuale per questo servizio.
ms.assetid: 4bd2b03f-ba8c-483e-af09-270424f9b1ed
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ProvisioningEnumerateJobs
- Metodo ProvisioningEnumerateJobs Servizi Desktop remoto, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Servizi Desktop remoto, metodo ProvisioningEnumerateJobs
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
ms.openlocfilehash: aaa2b54a0599c2bbcaf6b0f9a9acb3ab3028389b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518999"
---
# <a name="provisioningenumeratejobs-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Metodo ProvisioningEnumerateJobs della \_ classe RDMSVirtualDesktopCollection Win32

Enumera i processi di provisioning del desktop virtuale per questo servizio.

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

*Tipoprocesso* \[ in\]
</dt> <dd>

Integer che specifica il tipo di processo da enumerare.

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

*CollectionAlias* \[ in\]
</dt> <dd>

Alias dell'insieme di desktop virtuali da enumerare. Il valore predefinito per questo parametro è FALSE, che specifica che tutti i processi in esecuzione devono essere enumerati.

</dd> <dt>

*JobGuids* \[ out\]
</dt> <dd>

Matrice contenente i **GUID** dei processi di provisioning da enumerare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ RDBMS<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_RDMSVirtualDesktopCollection Win32**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





