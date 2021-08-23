---
description: Aggiunge una porzione di dati specifici dell'applicazione.
ms.assetid: 86ba37ac-8e65-4397-8ed1-37463152bebd
title: Metodo IContextNode::AddPropertyData (IACom.h)
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
ms.openlocfilehash: 8c9988217aed21ff1142f0e2083bee568ed12c31d90530ac1f3e9f5719c46446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719695"
---
# <a name="icontextnodeaddpropertydata-method"></a>Metodo IContextNode::AddPropertyData

Aggiunge una porzione di dati specifici dell'applicazione.

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

*pPropertyDataId* \[ Pollici\]
</dt> <dd>

Identificatore univoco globale (GUID) utilizzato per identificare il tipo di dati.

</dd> <dt>

*ulPropertyDataSize* \[ Pollici\]
</dt> <dd>

Dimensioni dei dati in byte.

</dd> <dt>

*pbPropertiesData* \[ Pollici\]
</dt> <dd>

\[in, size \_ is(ulPropertyDataSize)\]

Matrice di interi senza segno a 8 bit contenente le informazioni sulla proprietà da aggiungere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

Usare **IContextNode::AddPropertyData** per associare i dati a un nodo di contesto. Per recuperare i dati in un secondo momento, usare [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).

L'analizzatore input penna può eliminare il nodo come parte dell'analisi input penna, a meno che il nodo di contesto non sia confermato (vedere [**IContextNode::Confirm).**](icontextnode-confirm.md) Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer,**](iinkanalyzer.md)vedere [Proxy dati con analisi input penna.](data-proxy-with-ink-analysis.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**IContextNode::LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**IContextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> </dl>

 

 




