---
description: Recupera il tipo di relazione rappresentato da IContextLink.
ms.assetid: 03c13eba-1493-4fb7-b684-f15147e5a0eb
title: Metodo IContextLink::GetContextLinkDirection (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetContextLinkDirection
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 96506836e89f4bb2f8b202373df09b5cc6ee1c7f6e9e01f3b68bb2bbe2c8b56a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057911"
---
# <a name="icontextlinkgetcontextlinkdirection-method"></a>Metodo IContextLink::GetContextLinkDirection

Recupera il tipo di relazione rappresentato da [**IContextLink.**](icontextlink.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetContextLinkDirection(
  [out] ContextLinkDirection *pContextLinkDirection
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pContextLinkDirection* \[ Cambio\]
</dt> <dd>

Direzione rappresentato [**da IContextLink.**](icontextlink.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




