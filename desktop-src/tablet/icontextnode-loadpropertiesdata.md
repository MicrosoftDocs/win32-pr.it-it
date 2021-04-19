---
description: "Ricrea i dati delle proprietà specifiche dell'applicazione e interni per una matrice di byte creata in precedenza con IContextNode:: SavePropertiesData."
ms.assetid: 2d24d0da-16f1-4ddc-8e2e-93c312ecfa42
title: 'Metodo IContextNode:: LoadPropertiesData (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.LoadPropertiesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc495aaa52ebfbca088f954b34f22f9d6e1e53d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307422"
---
# <a name="icontextnodeloadpropertiesdata-method"></a>Metodo IContextNode:: LoadPropertiesData

Ricrea i dati delle proprietà specifiche dell'applicazione e interni per una matrice di byte creata in precedenza con [**IContextNode:: SavePropertiesData**](icontextnode-savepropertiesdata.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT LoadPropertiesData(
  [in]  ULONG        cbPropertiesDataSize,
  [in]  BYTE         *pbPropertiesData,
  [out] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cbPropertiesDataSize* \[ in\]
</dt> <dd>

Dimensioni della matrice di dati delle proprietà.

</dd> <dt>

*pbPropertiesData* \[ in\]
</dt> <dd>

Matrice Unsigned Integer a 8 bit contenente le informazioni sulle proprietà da caricare.

</dd> <dt>

*pfSuccessful* \[ out\]
</dt> <dd>

**Variante \_ TRUE** se i dati della proprietà sono stati caricati correttamente; in caso contrario, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IContextNode:: ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**IContextNode:: GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode:: RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode:: SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




