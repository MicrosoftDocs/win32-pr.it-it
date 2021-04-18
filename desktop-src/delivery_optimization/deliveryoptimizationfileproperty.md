---
title: Enumerazione DeliveryOptimizationFileProperty (Deliveryoptimization. h)
description: L'enumerazione DeliveryOptimizationFileProperty specifica l'ID di una proprietà facoltativa per il file DO.
keywords:
- Enumerazione DeliveryOptimizationFileProperty
topic_type:
- apiref
api_name:
- DeliveryOptimizationFileProperty
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 01/18/2019
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 238ad815149f7d40dd1902b991608e0a3005eb35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301492"
---
# <a name="deliveryoptimizationfileproperty-enumeration"></a>Enumerazione DeliveryOptimizationFileProperty

L'enumerazione DeliveryOptimizationFileProperty specifica l'ID di una proprietà facoltativa per il file DO. Questa enumerazione viene utilizzata nell'interfaccia IDeliveryOptimizationFile2 in cui viene passato il valore della proprietà di tipo VARIANT

## <a name="syntax"></a>Sintassi

```C++
typedef enum _DeliveryOptimizationFileProperty {  
  DOFilePropertyId_DecryptionInfo,
  DOFilePropertyId_IntegrityCheckInfo,
  DOFilePropertyId_IntegrityCheckMandatory,
  DOFilePropertyId_DownloadSinkInterface,
  DOFilePropertyId_DownloadSinkFilePath,
  DOFilePropertyId_DownloadSinkMemoryStream,
  DOFilePropertyId_TotalSizeBytes
} DOFilePropertyId;
```

## <a name="constants"></a>Costanti

<dl> <dt>

DOFilePropertyId_DecryptionInfo
</dt> <dd>

L'ID di proprietà DOFilePropertyId_DecryptionInfo imposta le informazioni di decrittografia sotto forma di stringa JSON. DOFilePropertyId_DecryptionInfo è una proprietà di sola scrittura di tipo VT_BSTR.

</dd> <dt>

DOFilePropertyId_IntegrityCheckInfo
</dt> <dd>

Il DOFilePropertyId_IntegrityCheckInfo ID proprietà imposta il percorso del file hash della parte (PHF), che viene usato da DO per eseguire i controlli di integrità del runtime sul contenuto scaricato. DOFilePropertyId_IntegrityCheckInfo è una proprietà di sola scrittura di tipo VT_BSTR.

</dd> <dt>

DOFilePropertyId_IntegrityCheckMandatory
</dt> <dd>

Il DOFilePropertyId_IntegrityCheckMandatory ID proprietà imposta un flag booleano che indica se l'utilizzo di PHF è obbligatorio. Se TRUE, il download verrà interrotto dopo che il controllo di integrità non è riuscito. DOFilePropertyId_IntegrityCheckMandatory è una proprietà di lettura/scrittura di tipo VT_BOOL.

</dd> <dt>

DOFilePropertyId_DownloadSinkFilePath
</dt> <dd>

L'ID della proprietà DOFilePropertyId_DownloadSinkFilePath imposta un percorso file system completo in cui devono essere archiviate le parti scaricate. DOFilePropertyId_DownloadSinkFilePath è di tipo VT_BSTR.

</dd> <dt>

DOFilePropertyId_DownloadSinkMemoryStream
</dt> <dd>

L'ID di proprietà DOFilePropertyId_DownloadSinkMemoryStream è deprecato. Non usare.

</dd> <dt>

DOFilePropertyId_TotalSizeBytes
</dt> <dd>

Il DOFilePropertyId_TotalSizeBytes ID proprietà specifica la dimensione totale del download. DOFilePropertyId_TotalSizeBytes è di tipo VT_UI8.
</dd> </dl>

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------|----------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1803 \[\]<br/>      |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>  |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>               |
