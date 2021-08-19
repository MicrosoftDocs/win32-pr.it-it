---
description: Specifica il metodo usato per codificare le informazioni sul vettore di movimento.
ms.assetid: 22ffdb77-9266-42e5-be41-fc7457141bba
title: MFPKEY_DELTAMVRANGEINDEX proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a21ac1a0bdaf859c93bca800d72f5e9ed155919bb07a24f5287b2436e57f94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113341"
---
# <a name="mfpkey_deltamvrangeindex-property"></a>Proprietà MFPKEY \_ DELTAMVRANGEINDEX

Specifica il metodo usato per codificare le informazioni sul vettore di movimento.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCDeltaMVRangeIndex

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

Se questa proprietà è impostata, il codificatore aumenta l'intervallo del vettore di movimento delta nei campi. Le informazioni sul vettore di movimento sono valide solo per i campi interlacciati.

Questa proprietà può essere impostata su uno dei valori seguenti:



| Valore | Descrizione                                                                          |
|-------|--------------------------------------------------------------------------------------|
| 0     | Usare l'intervallo del vettore di movimento delta esistente.                                          |
| 1     | Raddoppiare l'intervallo del vettore di movimento delta nella direzione orizzontale.                    |
| 2     | Raddoppiare l'intervallo del vettore di movimento delta nella direzione verticale.                      |
| 3     | Raddoppiare l'intervallo del vettore di movimento delta in entrambe le direzioni orizzontale e verticale. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




