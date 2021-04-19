---
description: Recupera una matrice contenente i dati della proprietà del pacchetto per il tratto specificato.
ms.assetid: 02db48b3-edc3-4ecb-8103-79312194937a
title: 'Metodo IContextNode:: GetStrokePacketDataById (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDataById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: be2e9326e2ecb20afc652776c006c8ae989c7396
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307432"
---
# <a name="icontextnodegetstrokepacketdatabyid-method"></a>Metodo IContextNode:: GetStrokePacketDataById

Recupera una matrice contenente i dati della proprietà del pacchetto per il tratto specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStrokePacketDataById(
  [in]      LONG  strokeId,
  [in, out] ULONG *pStrokePacketDataCount,
  [out]     LONG  **pplStrokePacketData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strokeId* \[ in\]
</dt> <dd>

Identificatore del tratto.

</dd> <dt>

*pStrokePacketDataCount* \[ in uscita\]
</dt> <dd>

Lunghezza della matrice di dati del pacchetto.

</dd> <dt>

*pplStrokePacketData* \[ out\]
</dt> <dd>

Puntatore ai dati del pacchetto per il tratto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *pplStrokePacketData* quando le informazioni non sono più necessarie.

 

*plStrokePacketData* contiene i dati dei pacchetti per tutti i punti del tratto. Per ottenere i tipi di dati dei pacchetti inclusi per ogni punto del tratto, utilizzare [**IContextNode:: GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md).

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

[**IContextNode::GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

