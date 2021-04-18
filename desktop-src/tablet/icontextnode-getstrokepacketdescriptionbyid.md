---
description: Recupera una matrice contenente gli identificatori di proprietà del pacchetto per il tratto specificato.
ms.assetid: 169e3ce3-fb81-4ed6-b380-ef0d12444ba7
title: 'Metodo IContextNode:: GetStrokePacketDescriptionById (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDescriptionById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e1633cd2097e256d389a2c86e450bf221f0546f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307430"
---
# <a name="icontextnodegetstrokepacketdescriptionbyid-method"></a>Metodo IContextNode:: GetStrokePacketDescriptionById

Recupera una matrice contenente gli identificatori di proprietà del pacchetto per il tratto specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStrokePacketDescriptionById(
  [in]      LONG  lStrokeId,
  [in, out] ULONG *pulStrokePacketDescriptionCount,
  [out]     GUID  **ppStrokePacketDescriptionGuids
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lStrokeId* \[ in\]
</dt> <dd>

Identificatore del tratto.

</dd> <dt>

*pulStrokePacketDescriptionCount* \[ in uscita\]
</dt> <dd>

Numero di proprietà dei pacchetti in ogni pacchetto.

</dd> <dt>

*ppStrokePacketDescriptionGuids* \[ out\]
</dt> <dd>

Matrice contenente gli identificatori di proprietà del pacchetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *ppStrokePacketDescriptionGuids* quando le informazioni non sono più necessarie.

 

\**ppStrokePacketDescriptionGuids* contiene gli identificatori univoci globali (Guid) che descrivono i tipi di dati dei pacchetti inclusi per ogni punto del tratto. Per un elenco completo delle proprietà dei pacchetti disponibili, vedere [costanti PacketPropertyGuids](packetpropertyguids-constants.md).

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

[**IContextNode::GetStrokePacketDataById**](icontextnode-getstrokepacketdatabyid.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

