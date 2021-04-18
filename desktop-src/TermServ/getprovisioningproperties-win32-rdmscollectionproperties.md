---
title: Metodo GetProvisioningProperties della classe Win32_RDMSCollectionProperties
description: Recupera le proprietà di provisioning dell'insieme di desktop virtuali.
ms.assetid: c314b7a5-8546-4711-833e-b47bb682aa53
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetProvisioningProperties
- Metodo GetProvisioningProperties Servizi Desktop remoto, classe Win32_RDMSCollectionProperties
- Classe Win32_RDMSCollectionProperties Servizi Desktop remoto, metodo GetProvisioningProperties
topic_type:
- apiref
api_name:
- Win32_RDMSCollectionProperties.GetProvisioningProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ca58f82d2918441e5da3cf53d442497c1a6a2eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301994"
---
# <a name="getprovisioningproperties-method-of-the-win32_rdmscollectionproperties-class"></a>Metodo GetProvisioningProperties della \_ classe RDMSCollectionProperties Win32

Recupera le proprietà di provisioning dell'insieme di desktop virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetProvisioningProperties(
  [out] string  PoolVhdType,
  [out] string  MasterVmLocation,
  [out] string  NamePrefix,
  [out] uint32  NameStartIndex,
  [out] string  LocalVmLocation,
  [out] string  LocalGoldVmLocation,
  [out] boolean RunFromSMB,
  [out] string  SMBLocation,
  [out] boolean SMBStreaming,
  [out] string  VmDomain,
  [out] string  VmOU,
  [out] string  ProductKey
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PoolVhdType* \[ out\]
</dt> <dd>

Specifica il formato del disco rigido virtuale (VHD) del pool di macchine virtuali nella raccolta.

<dt>

Clone
</dt> <dd>

VHD clonato.

</dd> <dt>

DiffDisk
</dt> <dd>

Disco rigido virtuale differenze.

</dd> </dl> </dd> <dt>

*MasterVmLocation* \[ out\]
</dt> <dd>

Riceve il percorso dell'immagine della macchina virtuale master.

</dd> <dt>

*NamePrefix* \[ out\]
</dt> <dd>

Riceve il prefisso del nome da accodare all'inizio dei nomi delle macchine virtuali.

</dd> <dt>

*NameStartIndex* \[ out\]
</dt> <dd>

Indice iniziale.

</dd> <dt>

*LocalVmLocation* \[ out\]
</dt> <dd>

Riceve il percorso locale delle macchine virtuali nei server Hyper-V. Se questo parametro è impostato su **null** o se è vuoto, verrà usata la directory predefinita della macchina virtuale.

</dd> <dt>

*LocalGoldVmLocation* \[ out\]
</dt> <dd>

Riceve il percorso locale dell'immagine del disco rigido virtuale dorato quando il parametro *PoolVhdTpe* è impostato su "DiffDisk". Se questo parametro è impostato su **null** o se è vuoto, verrà usata la directory predefinita della macchina virtuale.

</dd> <dt>

*RunFromSMB* \[ out\]
</dt> <dd>

Riceve un valore che indica se eseguire la raccolta da una condivisione SMB (Server Message Block). **True** per eseguire le macchine virtuali da una condivisione SBM; in caso contrario **False**.

</dd> <dt>

*SMBLocation* \[ out\]
</dt> <dd>

Riceve il percorso della condivisione SMB se è abilitata la condivisione SMB.

</dd> <dt>

*SMBStreaming* \[ out\]
</dt> <dd>

Riceve un valore che indica se il flusso SMB è abilitato. **True** se è abilitata la condivisione SMB. in caso contrario **False**.

</dd> <dt>

*VmDomain* \[ out\]
</dt> <dd>

Riceve il nome di dominio delle macchine virtuali nella raccolta.

</dd> <dt>

*VmOU* \[ out\]
</dt> <dd>

Riceve l'unità organizzativa Active Directory delle macchine virtuali nella raccolta.

</dd> <dt>

*ProductKey* \[ out\]
</dt> <dd>

Riceve i codici Product Key del sistema operativo per le macchine virtuali nella raccolta.

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

[**\_RDMSCollectionProperties Win32**](win32-rdmscollectionproperties.md)
</dt> </dl>

 

 





