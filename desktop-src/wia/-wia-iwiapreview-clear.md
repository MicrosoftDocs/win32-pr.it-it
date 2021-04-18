---
description: "Rilascia l'immagine non filtrata memorizzata nella cache dal metodo IWiaPreview:: GetNewPreview. Rilascia anche il filtro di elaborazione delle immagini."
ms.assetid: af94d27f-9d93-40e1-8d1a-e5546531a176
title: 'Metodo IWiaPreview:: Clear (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.Clear
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 1ac2cc1f12cf6fd59111d0159684459c2500a854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307359"
---
# <a name="iwiapreviewclear-method"></a>Metodo IWiaPreview:: Clear

Rilascia l'immagine non filtrata memorizzata nella cache dal metodo [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) . Rilascia anche il filtro di elaborazione delle immagini.

## <a name="syntax"></a>Sintassi


```C++
void Clear();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

In **IWiaPreview:: Clear** il componente Windows Image Acquisition (WIA) 2,0 Preview rilascia tutti i puntatori di interfaccia archiviati. Il componente WIA 2,0 Preview mantiene i riferimenti a *pWiaItem2* e *PWiaTransferCallback* passati in [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md). Per essere precisi, il componente WIA 2,0 Preview mantiene un riferimento a *pWiaItem2* e al filtro di elaborazione delle immagini del driver, che a sua volta mantiene un riferimento a *pWiaTransferCallback*. In **IWiaPreview:: Clear**, il componente WIA 2,0 Preview rilascia anche il riferimento a *pWiaItem2* e al filtro di elaborazione dell'immagine, che a sua volta rilascia il riferimento a *pWiaTransferCallback*. Il componente WIA 2,0 Preview Elimina l'immagine memorizzata nella cache e non filtrata che archivia internamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




