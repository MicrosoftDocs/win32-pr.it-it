---
description: L'interfaccia IKsPin fornisce un metodo per recuperare i medie supportati da un pin in un filtro in modalità kernel. IKsPin dispone di metodi aggiuntivi oltre a quello illustrato qui, ma non sono supportati per DirectShow.
ms.assetid: 14d9bef2-e8f0-49d5-bd89-69a95814cf8c
title: Interfaccia IKsPin (Ksproxy.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 8855378544bcc2ea7357af220b5d80d32edde74a50c304e973c9821aa8e9a41c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792331"
---
# <a name="ikspin-interface"></a>Interfaccia IKsPin

`IKsPin`L'interfaccia fornisce un metodo per recuperare i medie supportati da un pin in un filtro in modalità kernel. `IKsPin`dispone di metodi aggiuntivi oltre a quello illustrato qui, ma non sono supportati per DirectShow.

## <a name="members"></a>Membri

**L'interfaccia IKsPin** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IKsPin** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IKsPin** include questi metodi.



| Metodo                                          | Descrizione                                          |
|:------------------------------------------------|:-----------------------------------------------------|
| [**KsQueryMediums**](ikspin-ksquerymediums.md) | Recupera i medie supportati da un pin.<br/> |



 

## <a name="remarks"></a>Commenti

È necessario includere Ks.h prima di Ksproxy.h.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Ksproxy.h</dt> </dl>    |
| Libreria<br/>                  | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
