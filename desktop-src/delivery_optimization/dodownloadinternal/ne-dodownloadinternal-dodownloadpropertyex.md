---
title: Enumerazione DODownloadPropertyEx
description: Specifica l'ID delle proprietà estese per l'operazione di download DO.
keywords:
- Enumerazione DODownloadPropertyEx, DODownloadPropertyEx
topic_type:
- apiref
api_name:
- DODownloadPropertyEx
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: f5ec26d845fd6df2bfe0e84fffed0979c39e1971244788c9dfe5ddd3a0c0beca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990381"
---
# <a name="dodownloadpropertyex-enumeration"></a>Enumerazione DODownloadPropertyEx

> [!IMPORTANT]
> **L'enumerazione DODownloadPropertyEx** è deprecata. Usare invece [l'enumerazione DODownloadProperty](../deliveryoptimizationdownloadtypes/ne-deliveryoptimizationdownloadtypes-dodownloadproperty.md) [con IDODownload::GetProperty](../do/nf-do-idodownload-getproperty.md) e [IDODownload::SetProperty](../do/nf-do-idodownload-setproperty.md).

**L'enumerazione DODownloadPropertyEx** specifica l'ID delle proprietà estese per l'operazione di download DO. Questa enumerazione viene usata **dall'interfaccia IDODownloadInternal** e un **valore VARIANT** viene usato per ottenere e impostare il valore della proprietà.

## <a name="syntax"></a>Sintassi

```cpp
typedef enum _DODownloadPropertyEx
{
  DODownloadPropertyEx_UpdateId = 0,
  DODownloadPropertyEx_CorrelationVector,
  DODownloadPropertyEx_DecryptionInfo,    
  DODownloadPropertyEx_IntegrityCheckInfo,   
  DODownloadPropertyEx_IntegrityCheckMandatory, 
  DODownloadPropertyEx_TotalSizeBytes, 
  DODownloadPropertyEx_TempLocalFileUsage 
} DODownloadPropertyEx;
```
## <a name="constants"></a>Costanti

| Requisito | Valore |
|-|-|
| DODownloadPropertyEx_UpdateId | Riservato. Non usare. |
| DODownloadPropertyEx_CorrelationVector | facoltativo. Imposta un vettore di correlazione specifico ai fini della telemetria. Il tipo VARIANT è VT_BSTR. |
| DODownloadPropertyEx_DecryptionInfo | Riservato. Non usare. |
| DODownloadPropertyEx_IntegrityCheckInfo | Sola scrittura facoltativa. Imposta il percorso del file hash del frammento (PHF), usato da DO per eseguire controlli di integrità di runtime sul contenuto scaricato. Il tipo VARIANT è VT_BSTR. |
| DODownloadPropertyEx_IntegrityCheckMandatory | facoltativo. Imposta un flag booleano che indica se l'utilizzo del file hash del frammento (PHF) è obbligatorio. Se VARIANT_TRUE, il download verrà interrotto dopo che il controllo di integrità non è riuscito. Il tipo VARIANT è VT_BOOL. |
| DODownloadPropertyEx_TotalSizeBytes | Riservato. Non usare. |
| DODownloadPropertyEx_TempLocalFileUsage | Riservato. Non usare. |

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | \[Windows 10, versione 1809 Solo applicazioni Win32\] |
| **Server minimo supportato** | Windows Server, solo applicazioni Win32 versione 1809 \[\] |
| **Intestazione** | DODownloadInternal.h |
