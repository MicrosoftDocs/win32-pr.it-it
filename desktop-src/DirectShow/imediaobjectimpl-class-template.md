---
description: Il modello di classe IMediaObjectImpl fornisce un'implementazione di base per l'interfaccia IMediaObject. Per ulteriori informazioni sull'utilizzo di questo modello, vedere Utilizzo del modello di classe DMO.
ms.assetid: 81d45b8d-8373-4e42-b768-f6126feb935d
title: Modello di classe IMediaObjectImpl (Dmoimpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ecfa1be82ffeaa9e05eb6460249e0c40bb2989c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330398"
---
# <a name="imediaobjectimpl-class-template"></a>Modello di classe IMediaObjectImpl

Il `IMediaObjectImpl` modello di classe fornisce un'implementazione di base per l'interfaccia [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) . Per ulteriori informazioni sull'utilizzo di questo modello, vedere [utilizzo del modello di classe DMO](using-the-dmo-class-template.md).

Questo `IMediaObjectImpl` modello espone i membri seguenti.



| Classe annidata                              | Descrizione                                  |
|-------------------------------------------|----------------------------------------------|
| [**LockIt**](imediaobjectimpl-lockit.md) | Classe helper che blocca e sblocca il DMO. |



 



| Metodo                                                                      | Descrizione                                                          |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**CheckTypesSet**](/previous-versions/ms807621(v=msdn.10))                     | Determina se tutti i flussi non facoltativi hanno tipi di supporto. |
| [**InputType**](/previous-versions/ms807633(v=msdn.10))                             | Recupera il tipo di supporto corrente per un flusso di input specificato.       |
| [**InputTypeSet**](/previous-versions/ms807638(v=msdn.10))                       | Esegue una query per determinare se il tipo di supporto è stato impostato su un flusso di input.           |
| [**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))   | Esegue una query per determinare se un flusso di input può accettare più input.               |
| [**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))   | Esegue una query per determinare se un flusso di input può accettare un determinato tipo di supporto.       |
| [**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10)) | Esegue una query per determinare se un flusso di output può accettare un determinato tipo di supporto.      |
| [**Lock**](/previous-versions/ms809100(v=msdn.10))                                       | Blocca DMO                                                        |
| [**OutputType**](/previous-versions/ms807644(v=msdn.10))                           | Recupera il tipo di supporto corrente per un flusso di output specificato.      |
| [**OutputTypeSet**](/previous-versions/ms807649(v=msdn.10))                     | Esegue una query per determinare se il tipo di supporto è stato impostato su un flusso di output.          |
| [**Sblocca**](/previous-versions/ms809101(v=msdn.10))                                   | Sblocca DMO                                                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Dmoimpl. h</dt> </dl>                                                                     |
| Libreria<br/> | <dl> <dt>Dmoguids. lib; </dt> <dt>Msdmo. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Guida di riferimento a DMO](dmo-reference.md)
</dt> <dt>

[Uso del modello di classe DMO](using-the-dmo-class-template.md)
</dt> </dl>

 

 
