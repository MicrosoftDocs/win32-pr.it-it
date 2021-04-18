---
title: Metodo SynchronizePublishingData della classe Win32_RDMSManagementData
description: Sincronizza il set specificato di dati di pubblicazione per Desktop remoto Management Services (RDBMS).
ms.assetid: 0476ce12-9b08-418c-83c2-208275574f5b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SynchronizePublishingData
- Metodo SynchronizePublishingData Servizi Desktop remoto, classe Win32_RDMSManagementData
- Classe Win32_RDMSManagementData Servizi Desktop remoto, metodo SynchronizePublishingData
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData.SynchronizePublishingData
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d389ad08d81f39cab45502a42f4ebd95e16f36c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400573"
---
# <a name="synchronizepublishingdata-method-of-the-win32_rdmsmanagementdata-class"></a>Metodo SynchronizePublishingData della \_ classe RDMSManagementData Win32

Sincronizza il set specificato di dati di pubblicazione per Desktop remoto Management Services (RDBMS).

## <a name="syntax"></a>Sintassi


```mof
uint32 SynchronizePublishingData(
  [in] string Context
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Contesto* \[ in\]
</dt> <dd>

Informazioni di contesto dei dati di pubblicazione da sincronizzare.

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

[**\_RDMSManagementData Win32**](win32-rdmsmanagementdata.md)
</dt> </dl>

 

 





