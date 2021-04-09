---
description: Aggiunge un elemento di dati specifici dell'applicazione.
ms.assetid: 86ba37ac-8e65-4397-8ed1-37463152bebd
title: 'Metodo IContextNode:: AddPropertyData (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ed318520b8ac83acbc8ed615002fababe2a4b12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129507"
---
# <a name="icontextnodeaddpropertydata-method"></a>Metodo IContextNode:: AddPropertyData

Aggiunge un elemento di dati specifici dell'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddPropertyData(
  [in] const GUID  *pPropertyDataId,
  [in]       ULONG ulPropertyDataSize,
  [in]       BYTE  *pbPropertiesData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPropertyDataId* \[ in\]
</dt> <dd>

Identificatore univoco globale (GUID) utilizzato per identificare il tipo di dati.

</dd> <dt>

*ulPropertyDataSize* \[ in\]
</dt> <dd>

Dimensioni dei dati in byte.

</dd> <dt>

*pbPropertiesData* \[ in\]
</dt> <dd>

\[in, Size \_ è (ulPropertyDataSize)\]

Matrice di Unsigned Integer a 8 bit contenente le informazioni sulle proprietà da aggiungere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Usare **IContextNode:: AddPropertyData** per associare i dati a un nodo di contesto. Per recuperare i dati in un secondo momento, utilizzare [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md).

Ink Analyzer può eliminare il nodo come parte dell'analisi dell'input penna, a meno che il nodo di contesto non sia confermato (vedere [**IContextNode:: Confirm**](icontextnode-confirm.md)). Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer**](iinkanalyzer.md), vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

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

[**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**IContextNode:: GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode:: ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**IContextNode:: LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**IContextNode:: RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode:: SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> </dl>

 

 




