---
description: Recupera una matrice di byte che contiene i dati delle proprietà interne e specifici dell'applicazione per questo IContextNode.
ms.assetid: f26d71a7-fe71-48a8-9c8f-9c4d99261df1
title: Metodo IContextNode::SavePropertiesData (IACom.h)
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
ms.openlocfilehash: 5b02f5df7526b429a65b2a0baf49bda4571dd718a9bff875c79b7e325de244ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719685"
---
# <a name="icontextnodesavepropertiesdata-method"></a>Metodo IContextNode::SavePropertiesData

Recupera una matrice di byte che contiene i dati delle proprietà interne e specifici dell'applicazione per [**questo oggetto IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT SavePropertiesData(
  [in, out] ULONG *pulPropertiesDataSize,
  [out]     BYTE  **ppbPropertiesData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pulPropertiesDataSize* \[ in, out\]
</dt> <dd>

Dimensione della matrice di dati contenente le informazioni sulla proprietà. Il valore passato non viene usato.

</dd> <dt>

*ppbPropertiesData* \[ Cambio\]
</dt> <dd>

Puntatore a una matrice di interi senza segno a 8 bit che contiene i dati delle proprietà interne e specifici dell'applicazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *ppbPropertiesData* quando non sono più necessarie le informazioni.

 

Usare questo metodo quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer.**](iinkanalyzer.md) Questo metodo salva i dati delle proprietà impostati da **IInkAnalyzer** in [**IContextNode.**](icontextnode.md)

Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer,**](iinkanalyzer.md)vedere [Proxy dati con l'analisi dell'input penna](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**IContextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

