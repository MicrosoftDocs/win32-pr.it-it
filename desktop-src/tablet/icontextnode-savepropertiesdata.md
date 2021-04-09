---
description: Recupera una matrice di byte che contiene i dati della proprietà interna e specifici dell'applicazione per questo IContextNode.
ms.assetid: f26d71a7-fe71-48a8-9c8f-9c4d99261df1
title: 'Metodo IContextNode:: SavePropertiesData (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SavePropertiesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f2ac064632eb9e5dd2b94f6e75b9b2836c75996d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966726"
---
# <a name="icontextnodesavepropertiesdata-method"></a>Metodo IContextNode:: SavePropertiesData

Recupera una matrice di byte che contiene i dati della proprietà interna e specifici dell'applicazione per questo [**IContextNode**](icontextnode.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT SavePropertiesData(
  [in, out] ULONG *pulPropertiesDataSize,
  [out]     BYTE  **ppbPropertiesData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pulPropertiesDataSize* \[ in uscita\]
</dt> <dd>

Dimensioni della matrice di dati contenente le informazioni sulla proprietà. Il valore passato non viene utilizzato.

</dd> <dt>

*ppbPropertiesData* \[ out\]
</dt> <dd>

Puntatore a una matrice di Unsigned Integer a 8 bit che contiene i dati della proprietà interna e specifici dell'applicazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *ppbPropertiesData* quando le informazioni non sono più necessarie.

 

Utilizzare questo metodo quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md). Questo metodo salva i dati della proprietà impostati da **IInkAnalyzer** in [**IContextNode**](icontextnode.md).

Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer**](iinkanalyzer.md), vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

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

[**IContextNode:: LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**IContextNode:: RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode:: GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode:: ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

