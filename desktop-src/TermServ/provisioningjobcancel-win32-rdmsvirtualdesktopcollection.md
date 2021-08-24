---
title: Metodo ProvisioningJobCancel della classe Win32_RDMSVirtualDesktopCollection
description: Annulla un processo di provisioning di desktop virtuali.
ms.assetid: 933ea0f3-b916-4e70-89de-597f9eb23976
ms.tgt_platform: multiple
keywords:
- Metodo ProvisioningJobCancel Servizi Desktop remoto
- Metodo ProvisioningJobCancel Servizi Desktop remoto , Win32_RDMSVirtualDesktopCollection classe
- Win32_RDMSVirtualDesktopCollection classe Servizi Desktop remoto , metodo ProvisioningJobCancel
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
ms.openlocfilehash: 1e62e3305cdb544d0a45ee299c8bc5508bbef4915134fbf2d09f1c0b4884cc51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866081"
---
# <a name="provisioningjobcancel-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Metodo ProvisioningJobCancel della classe \_ WIN32 RDMSVirtualDesktopCollection

Annulla un processo di provisioning di desktop virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 ProvisioningJobCancel(
  [in] string JobGuid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*JobGuid* \[ Pollici\]
</dt> <dd>

GUID **che** identifica in modo univoco il processo di provisioning da annullare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Rdms \\ CIMv2 \\ radice<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktopCollection**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





