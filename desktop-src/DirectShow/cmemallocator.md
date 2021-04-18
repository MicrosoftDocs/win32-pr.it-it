---
description: Implementa un allocatore che supporta l'interfaccia IMemAllocator.
ms.assetid: c40eccef-d915-4bf3-81b2-b20e000718fb
title: Classe CMemAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5adf390b7abf8fcbdb017ecde04bde76bf4bc001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328841"
---
# <a name="cmemallocator-class"></a>Classe CMemAllocator

![gerarchia di classi cmemallocator](images/filter10.png)

Implementa un allocatore che supporta l'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .

Questa classe deriva da [**CBaseAllocator**](cbaseallocator.md). Per ulteriori informazioni sugli allocatori, vedere la documentazione relativa a [**CBaseAllocator**](cbaseallocator.md).



| Variabili membro protette                              | Descrizione                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [**\_pbuffer m**](cmemallocator-m-pbuffer.md)           | Puntatore al blocco di memoria che contiene i buffer.                   |
| Metodi protetti                                       | Descrizione                                                              |
| [**Libero**](cmemallocator-free.md)                      | Metodo segnaposto; chiamato durante un'operazione di decommit.                  |
| [**ReallyFree**](cmemallocator-reallyfree.md)          | Rilascia la memoria per i buffer.                                     |
| [**Alloc**](cmemallocator-alloc.md)                    | Alloca memoria per i buffer.                                        |
| Metodi pubblici                                          | Descrizione                                                              |
| [**CMemAllocator**](cmemallocator-cmemallocator.md)    | Metodo del costruttore.                                                      |
| [**~ CMemAllocator**](cmemallocator--cmemallocator.md) | Metodo del distruttore.                                                       |
| [**CreateInstance**](cmemallocator-createinstance.md)  | Crea una nuova istanza della classe **CMemAllocator** .                   |
| Metodi IMemAllocator                                   | Descrizione                                                              |
| [**SetProperties**](cmemallocator-setproperties.md)    | Specifica il numero di buffer da allocare e le dimensioni di ogni buffer. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Fornire un allocatore personalizzato](providing-a-custom-allocator.md)
</dt> </dl>

 

 




