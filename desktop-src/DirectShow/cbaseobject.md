---
description: La classe CBaseObject è una classe astratta per l'implementazione di oggetti DirectShow. Per implementare oggetti Component Object Model (COM), usare la classe CUnknown che deriva da CBaseObject.
ms.assetid: 4b651d43-b177-4081-8c76-f6615ff2830c
title: Classe CBaseObject (ComBase. h)
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
ms.openlocfilehash: bbc3e072c31618dab6a7bc07048728f60dbcf0d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326430"
---
# <a name="cbaseobject-class"></a>Classe CBaseObject

La classe **CBaseObject** è una classe astratta per l'implementazione di oggetti DirectShow. Per implementare oggetti Component Object Model (COM), usare la classe [**CUnknown**](cunknown.md) che deriva da **CBaseObject**.



| Metodi della classe                                      | Descrizione                            |
|----------------------------------------------------|----------------------------------------|
| [**CBaseObject**](cbaseobject-cbaseobject.md)     | Metodo del costruttore.                    |
| [**~ CBaseObject**](cbaseobject--cbaseobject.md)   | Metodo del distruttore.                     |
| [**ObjectsActive**](cbaseobject-objectsactive.md) | Recupera il numero di oggetti attivi. |



 

## <a name="remarks"></a>Commenti

La maggior parte delle classi base di DirectShow derivano da **CBaseObject**. Questa classe fornisce assistenza per il debug mantenendo un conteggio di tutti gli oggetti DirectShow attivi in fase di esecuzione. Il numero di oggetti viene archiviato in una variabile membro statica della classe:


```
class CBaseObject
{
private:
    static LONG m_cObjects;  // Total number of objects active. 
/* ... */
};
```



Nelle build di debug, la DLL asserirà se viene scaricata mentre il conteggio oggetti è maggiore di zero. In questo modo è più semplice rilevare le perdite dovute a problemi di conteggio dei riferimenti.

Il costruttore **CBaseObject** accetta un argomento, un nome di debug per l'oggetto. Questo nome viene archiviato in una tabella globale della DLL. La funzione [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) formatta un elenco degli oggetti attivi nella dll e li invia all'output di debug.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>ComBase. h (Includi Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi base di DirectShow](directshow-base-classes.md)
</dt> </dl>

 

 




