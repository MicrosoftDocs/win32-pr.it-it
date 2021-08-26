---
description: Recupera una raccolta di oggetti IContextLink che rappresenta le relazioni con altri oggetti IContextNode.
ms.assetid: 0fe56e6d-c779-4916-9c80-6f18cf6f1b09
title: Metodo IContextNode::GetContextLinks (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2c3b63e50cf43f06f6065a61dacfbbbd8a00fe7959bb5133407a6c2a980a1a20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057840"
---
# <a name="icontextnodegetcontextlinks-method"></a>Metodo IContextNode::GetContextLinks

Recupera una raccolta di oggetti [**IContextLink**](icontextlink.md) che rappresenta le relazioni con altri [**oggetti IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetContextLinks(
  [out] IContextLinks **ppContextLinks
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppContextLinks* \[ Cambio\]
</dt> <dd>

Puntatore a una raccolta di [**oggetti IContextLink**](icontextlink.md) che rappresenta le relazioni con altri [**oggetti IContextNode.**](icontextnode.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppContextLinks* quando non è più necessario usare la raccolta di collegamenti di contesto.

 

Per ottenere informazioni sulle relazioni tra nodi padre o figlio, usare [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) o [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md).

Per altre informazioni sui tipi di relazioni descritte dai collegamenti, vedere [**IContextLink**](icontextlink.md) e [**ContextLinkDirection.**](contextlinkdirection.md)

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

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[**IContextNode::AddContextLink**](icontextnode-addcontextlink.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

