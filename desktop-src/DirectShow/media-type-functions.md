---
description: Le classi base di DirectShow forniscono funzioni di supporto per la gestione della \_ struttura del tipo di supporto am \_ .
ms.assetid: 4dbea5b4-bf78-4253-be48-d81b77be6e77
title: Funzioni di tipo supporto (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Media
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a39fe9a9599a1d85c14a226106f5c8d7080b721f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323999"
---
# <a name="media-type-functions"></a>Funzioni di tipo multimediale

Le classi base di DirectShow forniscono funzioni di supporto per la gestione della struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

La struttura del **\_ \_ tipo di supporto am** contiene un puntatore (membro **pbFormat** ) a un altro blocco di memoria, denominato *blocco di formato*. Quando si lavora con questa struttura, è necessario prestare attenzione all'allocazione di memoria per evitare perdite di memoria.

Le funzioni seguenti allocano memoria:

-   **CreateMediaType** alloca una nuova struttura **del \_ \_ tipo di supporto am** e il blocco di formato.
-   **CopyMediaType** copia in una struttura **del \_ \_ tipo di supporto am** esistente, ma alloca il blocco di formato.
-   **CreateAudioMediaType** Inizializza una struttura **del \_ \_ tipo di supporto am** esistente e, facoltativamente, alloca il blocco di formato.

Le funzioni seguenti liberano memoria:

-   **FreeMediaType** rilascia il blocco di formato.
-   **DeleteMediaType** libera una struttura **del \_ \_ tipo di supporto am** , incluso il blocco di formato.



| Funzione                                             | Descrizione                                                                                                 |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**CopyMediaType**](copymediatype.md)               | Copia una struttura del **tipo di \_ supporto \_ am** allocato per le attività.                                                      |
| [**CreateAudioMediaType**](createaudiomediatype.md) | Inizializza una struttura del tipo di supporto data una struttura del formato Wave.                                           |
| [**CreateMediaType**](createmediatype.md)           | Alloca e Inizializza una struttura **del \_ \_ tipo di supporto am** da una struttura del **\_ \_ tipo di supporto am** esistente. |
| [**DeleteMediaType**](deletemediatype.md)           | Elimina una struttura del **tipo di \_ supporto \_ am** allocato per le attività.                                                     |
| [**FreeMediaType**](freemediatype.md)               | Libera una struttura del **\_ \_ tipo di supporto am** allocata per le attività dalla memoria.                                           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




