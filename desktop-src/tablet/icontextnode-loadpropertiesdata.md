---
description: Ricrea i dati delle proprietà interne e specifici dell'applicazione per una matrice di byte creata in precedenza con IContextNode::SavePropertiesData.
ms.assetid: 2d24d0da-16f1-4ddc-8e2e-93c312ecfa42
title: Metodo IContextNode::LoadPropertiesData (IACom.h)
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
ms.openlocfilehash: 8d58c37dc91fac9704221fae13505f5e32c6e48d097133e3aad9154f5f2ec3e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719675"
---
# <a name="icontextnodeloadpropertiesdata-method"></a>Metodo IContextNode::LoadPropertiesData

Ricrea i dati delle proprietà interne e specifici dell'applicazione per una matrice di byte creata in precedenza con [**IContextNode::SavePropertiesData.**](icontextnode-savepropertiesdata.md)

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

*cbPropertiesDataSize* \[ Pollici\]
</dt> <dd>

Dimensione della matrice di dati delle proprietà.

</dd> <dt>

*pbPropertiesData* \[ Pollici\]
</dt> <dd>

Matrice di interi senza segno a 8 bit contenente le informazioni sulla proprietà da caricare.

</dd> <dt>

*pfSuccessful* \[ Cambio\]
</dt> <dd>

**VARIANT \_ TRUE** se i dati della proprietà sono stati caricati correttamente. in caso contrario, **VARIANT \_ FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

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

[**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IContextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




