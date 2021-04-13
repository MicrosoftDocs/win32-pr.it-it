---
description: Specifica il metodo usato per codificare le informazioni sul vettore di movimento.
ms.assetid: 22ffdb77-9266-42e5-be41-fc7457141bba
title: Proprietà MFPKEY_DELTAMVRANGEINDEX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c72d923659e64c9a0dcab40811e31d7752924700
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528675"
---
# <a name="mfpkey_deltamvrangeindex-property"></a>\_Proprietà DELTAMVRANGEINDEX di MFPKEY

Specifica il metodo usato per codificare le informazioni sul vettore di movimento.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCDeltaMVRangeIndex

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

Se questa proprietà è impostata, il codificatore aumenta l'intervallo di vettori di movimento Delta nei campi. Le informazioni sul vettore di movimento sono valide solo per i campi interlacciati.

Questa proprietà può essere impostata su uno dei valori seguenti:



| Valore | Descrizione                                                                          |
|-------|--------------------------------------------------------------------------------------|
| 0     | Usare l'intervallo di vettori di movimento Delta esistente.                                          |
| 1     | Raddoppiare l'intervallo del vettore di movimento Delta nella direzione orizzontale.                    |
| 2     | Raddoppiare l'intervallo del vettore di movimento Delta nella direzione verticale.                      |
| 3     | Raddoppiare l'intervallo del vettore di movimento Delta nelle direzioni orizzontale e verticale. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




