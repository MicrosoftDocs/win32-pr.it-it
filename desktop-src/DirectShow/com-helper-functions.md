---
description: Queste funzioni forniscono il supporto per l'implementazione dell'interfaccia IUnknown in DirectShow.
ms.assetid: 991e4c69-7d30-4ecf-9ccf-4920452c21d6
title: Funzioni helper COM (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COM
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa8558cd0d04258adf89cbacdd99952cf00c6d0aa5f24ee38cca2dceb4e5478f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084341"
---
# <a name="com-helper-functions"></a>Funzioni helper COM

Queste funzioni forniscono il supporto per l'implementazione **dell'interfaccia IUnknown** in DirectShow.



| Funzione                                               | Descrizione                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------|
| [**DECLARE \_ IUNKNOWN**](declare-iunknown.md)          | Dichiara i tre metodi dell'interfaccia di base per una nuova interfaccia. |
| [**GetInterface**](getinterface.md)                   | Recupera un puntatore a interfaccia al client richiesto.               |
| [**INonDelegatingUnknown**](inondelegatingunknown.md) | Versione non recapitante **dell'interfaccia IUnknown.**                  |
| [**LoadOLEAut32**](loadoleaut32.md)                   | Carica la DLL di automazione (OleAut32.dll).                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Combase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di utilità](utility-functions.md)
</dt> </dl>

 

 




