---
title: Interfaccia ITfContextRenderingMarkup
description: L'interfaccia ITfContextRenderingMarkup viene implementata da TSF Manager e utilizzata dalle applicazioni. Questa interfaccia può essere recuperata usando IQueryInterface dall'oggetto ITfContext. Questa interfaccia consente all'applicazione di enumerare le informazioni di rendering.
ms.assetid: 733d2db2-f9e9-4b78-af13-adc03825bf2b
keywords:
- Framework servizi di testo interfaccia ITfContextRenderingMarkup
- Framework dei servizi di testo dell'interfaccia ITfContextRenderingMarkup, descritto
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b71e977665a4b3a6e817ef782ee558064e0986a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872694"
---
# <a name="itfcontextrenderingmarkup-interface"></a>Interfaccia ITfContextRenderingMarkup

L'interfaccia **ITfContextRenderingMarkup** viene implementata da TSF Manager e utilizzata dalle applicazioni. Questa interfaccia può essere recuperata usando IQueryInterface dall'oggetto [ITfContext](/windows/desktop/api/Msctf/nn-msctf-itfcontext) . Questa interfaccia consente all'applicazione di enumerare le informazioni di rendering.



| Metodi ITfContextRenderingMarkup                                                | Descrizione                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [GetRenderingMarkup](itfcontextrenderingmarkup-getrenderingmarkup.md)           | Recupera un enumeratore dei markup di rendering per l'intervallo specificato. |
| [FindNextRenderingMarkup](itfcontextrenderingmarkup-findnextrenderingmarkup.md) | Questa funzione non è implementata. Restituisce sempre E \_ NOTIMPL.       |



 

## <a name="members"></a>Membri

L'interfaccia **ITfContextRenderingMarkup** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="remarks"></a>Commenti

> [!Note]  
> Questa interfaccia non è attualmente presente nei file di intestazione pubblici. Per usare questa API, è necessario compilare MIDL per il [prototipo](prototypes.md).

 

 

 