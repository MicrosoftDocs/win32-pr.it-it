---
title: Metodo ProvisioningJobCancel della classe Win32_RDMSVirtualDesktopCollection
description: Annulla un processo di provisioning di un desktop virtuale.
ms.assetid: 933ea0f3-b916-4e70-89de-597f9eb23976
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ProvisioningJobCancel
- Metodo ProvisioningJobCancel Servizi Desktop remoto, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Servizi Desktop remoto, metodo ProvisioningJobCancel
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobCancel
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f414bcdc264d682817898bae98fcf60a716452
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301862"
---
# <a name="provisioningjobcancel-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Metodo ProvisioningJobCancel della \_ classe RDMSVirtualDesktopCollection Win32

Annulla un processo di provisioning di un desktop virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 ProvisioningJobCancel(
  [in] string JobGuid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*JobGuid* \[ in\]
</dt> <dd>

**GUID** che identifica in modo univoco il processo di provisioning da annullare.

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

 

 





