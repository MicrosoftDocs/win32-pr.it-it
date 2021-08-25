---
description: Arresta il passaggio di codifica corrente o verifica se il passaggio di codifica corrente è l'ultimo.
ms.assetid: 847f638f-9ab9-42ca-8e39-82c113cee92f
title: Proprietà AVEncCommonPassEnd (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02faeb9d78f10b962b7134fd316bda348b0f03e1a82ace210956c2243231df19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873371"
---
# <a name="avenccommonpassend-property"></a>AVEncCommonPassEnd - proprietà

Arresta il passaggio di codifica corrente o verifica se il passaggio di codifica corrente è l'ultimo.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncCommonPassEnd**

## <a name="remarks"></a>Commenti

L'impostazione di questa **proprietà su VARIANT \_ TRUE** termina il passaggio di codifica corrente. L'impostazione di questa proprietà **su VARIANT \_ FALSE** termina la codifica multipass.

La lettura di questa proprietà esegue una query per determinare se il passaggio di codifica corrente è l'ultimo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[ app desktop \| UWP\]<br/>                     |
| Server minimo supportato<br/> | app \[ desktop UWP di Windows 2000 Server \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API Codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




