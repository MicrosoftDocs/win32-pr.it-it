---
description: La classe CBaseObject è una classe astratta per l'implementazione DirectShow oggetti. Per implementare Component Object Model (COM), usare la classe CUnknown, che deriva da CBaseObject.
ms.assetid: 4b651d43-b177-4081-8c76-f6615ff2830c
title: Classe CBaseObject (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7809ec53746730f02f9b095ede3ae00b53f1fe55c21116c22d854c3d4b193e97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910621"
---
# <a name="cbaseobject-class"></a>Classe CBaseObject

La **classe CBaseObject** è una classe astratta per l'implementazione DirectShow oggetti. Per implementare Component Object Model (COM), usare la [**classe CUnknown,**](cunknown.md) che deriva da **CBaseObject**.



| Metodi della classe                                      | Descrizione                            |
|----------------------------------------------------|----------------------------------------|
| [**CBaseObject**](cbaseobject-cbaseobject.md)     | Metodo del costruttore.                    |
| [**~CBaseObject**](cbaseobject--cbaseobject.md)   | Metodo del distruttore.                     |
| [**OggettiAttivi**](cbaseobject-objectsactive.md) | Recupera il numero di oggetti attivi. |



 

## <a name="remarks"></a>Commenti

La maggior parte delle DirectShow di base derivano da **CBaseObject**. Questa classe fornisce assistenza per il debug mantenendo attivo un conteggio di tutti DirectShow oggetti durante l'esecuzione. Il conteggio degli oggetti viene archiviato in una variabile membro class-static:


```
class CBaseObject
{
private:
    static LONG m_cObjects;  // Total number of objects active. 
/* ... */
};
```



Nelle build di debug, la DLL asserirà se viene scaricata mentre il numero di oggetti è maggiore di zero. In questo modo è più semplice rilevare le perdite causate da problemi di conteggio dei riferimenti.

Il **costruttore CBaseObject** accetta un argomento, un nome di debug per l'oggetto. Questo nome viene archiviato in una tabella globale nella DLL. La [**funzione DbgDumpObjectRegister**](dbgdumpobjectregister.md) formatta un elenco degli oggetti attivi nella DLL e lo invia all'output di debug.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Combase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DirectShow Classi di base](directshow-base-classes.md)
</dt> </dl>

 

 




