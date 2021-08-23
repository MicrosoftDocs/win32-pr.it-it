---
description: Recupera una matrice contenente i dati della proprietà del pacchetto per il tratto specificato.
ms.assetid: 02db48b3-edc3-4ecb-8103-79312194937a
title: Metodo IContextNode::GetStrokePacketDataById (IACom.h)
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
ms.openlocfilehash: f80ad2e4acc88f24a14e21f604eb17dbab51a5bdeca0fc90ffc3ca9beb99f1de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967379"
---
# <a name="icontextnodegetstrokepacketdatabyid-method"></a>Metodo IContextNode::GetStrokePacketDataById

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

*strokeId* \[ Pollici\]
</dt> <dd>

Identificatore per il tratto.

</dd> <dt>

*pStrokePacketDataCount* \[ in, out\]
</dt> <dd>

Lunghezza della matrice di dati del pacchetto.

</dd> <dt>

*pplStrokePacketData* \[ Cambio\]
</dt> <dd>

Puntatore ai dati del pacchetto per il tratto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *pplStrokePacketData* quando non sono più necessarie le informazioni.

 

*plStrokePacketData contiene* i dati dei pacchetti per tutti i punti nel tratto. Per ottenere i tipi di dati del pacchetto inclusi per ogni punto del tratto, usare [**IContextNode::GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md).

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

[**IContextNode::GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

