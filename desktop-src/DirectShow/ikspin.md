---
description: L'interfaccia IKsPin fornisce un metodo per recuperare i supporti supportati da un pin in un filtro in modalità kernel. IKsPin dispone di metodi aggiuntivi oltre a quello illustrato di seguito, ma non sono supportati per DirectShow.
ms.assetid: 14d9bef2-e8f0-49d5-bd89-69a95814cf8c
title: Interfaccia IKsPin (ksproxy. h)
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
ms.openlocfilehash: 3d65e5ba5525b977ebae27da9964579614a1d653
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303999"
---
# <a name="ikspin-interface"></a>Interfaccia IKsPin

L' `IKsPin` interfaccia fornisce un metodo per recuperare i supporti supportati da un pin in un filtro in modalità kernel. `IKsPin` dispone di metodi aggiuntivi oltre a quelli illustrati in questo argomento, ma non sono supportati per DirectShow.

## <a name="members"></a>Membri

L'interfaccia **IKsPin** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IKsPin** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IKsPin** dispone di questi metodi.



| Metodo                                          | Descrizione                                          |
|:------------------------------------------------|:-----------------------------------------------------|
| [**KsQueryMediums**](ikspin-ksquerymediums.md) | Recupera i supporti supportati da un PIN.<br/> |



 

## <a name="remarks"></a>Commenti

Prima di ksproxy. h, è necessario includere KS. h.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Ksproxy. h</dt> </dl>    |
| Libreria<br/>                  | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
