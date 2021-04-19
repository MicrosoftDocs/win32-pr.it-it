---
description: Queste funzioni forniscono il supporto per l'implementazione dell'interfaccia IUnknown in DirectShow.
ms.assetid: 991e4c69-7d30-4ecf-9ccf-4920452c21d6
title: Funzioni helper COM (ComBase. h)
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
ms.openlocfilehash: 9522469ee1aa4f4efa63b4cff6ad73204973a622
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333434"
---
# <a name="com-helper-functions"></a>Funzioni helper COM

Queste funzioni forniscono il supporto per l'implementazione dell'interfaccia **IUnknown** in DirectShow.



| Funzione                                               | Descrizione                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------|
| [**DICHIARARE \_ IUnknown**](declare-iunknown.md)          | Dichiara i tre metodi dell'interfaccia di base per una nuova interfaccia. |
| [**GetInterface**](getinterface.md)                   | Recupera un puntatore di interfaccia al client richiesto.               |
| [**INonDelegatingUnknown**](inondelegatingunknown.md) | Versione non delegata dell'interfaccia **IUnknown** .                  |
| [**LoadOLEAut32**](loadoleaut32.md)                   | Carica la DLL di automazione (OleAut32.dll).                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>ComBase. h (Includi Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di utilità](utility-functions.md)
</dt> </dl>

 

 




