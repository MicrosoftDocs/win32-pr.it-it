---
title: Metodo ProvisioningJobGetReport della classe Win32_RDMSVirtualDesktopCollection
description: Ottiene un report sullo stato di un processo di provisioning di un desktop virtuale.
ms.assetid: 8fc03fed-0838-4530-9b0f-0f561d76769d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ProvisioningJobGetReport
- Metodo ProvisioningJobGetReport Servizi Desktop remoto, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Servizi Desktop remoto, metodo ProvisioningJobGetReport
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobGetReport
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6605402c6ed6c0269b9971922bdefd48f265c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301861"
---
# <a name="provisioningjobgetreport-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Metodo ProvisioningJobGetReport della \_ classe RDMSVirtualDesktopCollection Win32

Ottiene un report sullo stato di un processo di provisioning di un desktop virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 ProvisioningJobGetReport(
  [in]  string JobGuid,
  [out] string JobReportXml
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*JobGuid* \[ in\]
</dt> <dd>

**GUID** che identifica in modo univoco il processo di provisioning.

</dd> <dt>

*JobReportXml* \[ out\]
</dt> <dd>

Stringa che contiene il report in formato XML.

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

 

 





