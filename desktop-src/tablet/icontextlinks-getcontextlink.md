---
description: Recupera IContextLink in corrispondenza dell'indice specificato.
ms.assetid: 46bb71b9-5ef3-4756-97f6-40e0aaa82826
title: Metodo IContextLinks::GetContextLink (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks.GetContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 01cf3b971b8533f21185a9b6e65c3cfb25109e657e2c9e2a931253d86c51dbdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940311"
---
# <a name="icontextlinksgetcontextlink-method"></a>Metodo IContextLinks::GetContextLink

Recupera [**IContextLink in**](icontextlink.md) corrispondenza dell'indice specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetContextLink(
  [in]  ULONG        ulIndex,
  [out] IContextLink **ppContextLink
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ulIndex* \[ Pollici\]
</dt> <dd>

Indice in base zero [**dell'oggetto IContextLink**](icontextlink.md) da ottenere.

</dd> <dt>

*ppContextLink* \[ Cambio\]
</dt> <dd>

Puntatore [**all'oggetto IContextLink**](icontextlink.md) in corrispondenza dell'indice specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su ppContextLink quando non è più necessario \*  usare il collegamento di contesto.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextLinks**](icontextlinks.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

