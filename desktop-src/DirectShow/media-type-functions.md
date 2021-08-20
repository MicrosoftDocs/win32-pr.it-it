---
description: Le DirectShow di base forniscono funzioni helper per la gestione della struttura AM \_ MEDIA \_ TYPE.
ms.assetid: 4dbea5b4-bf78-4253-be48-d81b77be6e77
title: Funzioni del tipo di supporto (Mtype.h)
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
ms.openlocfilehash: ef47b944d5d445f57779f99cb8517a773a7efba19ae3f2133f896fcba7b86548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153159"
---
# <a name="media-type-functions"></a>Funzioni del tipo di supporto

Le DirectShow di base forniscono funzioni helper per la gestione della [**struttura AM \_ MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

La **struttura AM MEDIA \_ \_ TYPE** contiene un puntatore (il **membro pbFormat)** a un altro blocco di memoria, denominato *blocco di formato*. Quando si lavora con questa struttura, è quindi necessario prestare attenzione all'allocazione di memoria per evitare perdite di memoria.

Le funzioni seguenti allocano memoria:

-   **CreateMediaType** alloca una nuova **struttura AM MEDIA \_ \_ TYPE** e il blocco di formato.
-   **CopyMediaType** copia in una struttura **AM \_ MEDIA \_ TYPE** esistente, ma alloca il blocco di formato.
-   **CreateAudioMediaType** inizializza una struttura **AM \_ MEDIA \_ TYPE** esistente e facoltativamente alloca il blocco di formato.

Le funzioni seguenti liberano memoria:

-   **FreeMediaType rilascia** il blocco di formato.
-   **DeleteMediaType** libera una **struttura AM MEDIA \_ \_ TYPE,** incluso il blocco di formato.



| Funzione                                             | Descrizione                                                                                                 |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**CopyMediaType**](copymediatype.md)               | Copia una struttura **AM MEDIA \_ \_ TYPE** allocata dall'attività.                                                      |
| [**CreateAudioMediaType**](createaudiomediatype.md) | Inizializza una struttura del tipo di supporto in base a una struttura del formato wave.                                           |
| [**CreateMediaType**](createmediatype.md)           | Alloca e inizializza una **struttura AM MEDIA \_ \_ TYPE** da una struttura **AM MEDIA \_ \_ TYPE** esistente. |
| [**DeleteMediaType**](deletemediatype.md)           | Elimina una struttura **AM MEDIA \_ \_ TYPE** allocata dall'attività.                                                     |
| [**FreeMediaType**](freemediatype.md)               | Libera dalla memoria una struttura **AM \_ MEDIA TYPE \_ allocata** dall'attività.                                           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype.h (includere Flussi.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




