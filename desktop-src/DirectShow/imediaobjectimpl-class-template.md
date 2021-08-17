---
description: Il modello di classe IMediaObjectImpl fornisce un'implementazione di base per l'interfaccia IMediaObject. Per altre informazioni sull'uso di questo modello, vedere Uso del modello DMO classe.
ms.assetid: 81d45b8d-8373-4e42-b768-f6126feb935d
title: Modello di classe IMediaObjectImpl (Dmoimpl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b166836ff4da6100f61fca5d3a0c2887462b37adcbdd2ec61abeb919553a59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015579"
---
# <a name="imediaobjectimpl-class-template"></a>Modello di classe IMediaObjectImpl

Il `IMediaObjectImpl` modello di classe fornisce un'implementazione di base per [**l'interfaccia IMediaObject.**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) Per altre informazioni sull'uso di questo modello, vedere [Using the DMO Class Template](using-the-dmo-class-template.md).

Questo `IMediaObjectImpl` modello espone i membri seguenti.



| Classe annidata                              | Descrizione                                  |
|-------------------------------------------|----------------------------------------------|
| [**Lockit**](imediaobjectimpl-lockit.md) | Classe helper che blocca e sblocca il DMO. |



 



| Metodo                                                                      | Descrizione                                                          |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**CheckTypesSet**](/previous-versions/ms807621(v=msdn.10))                     | Determina se tutti i flussi non facoltativi hanno tipi di supporto. |
| [**InputType**](/previous-versions/ms807633(v=msdn.10))                             | Recupera il tipo di supporto corrente per un flusso di input specificato.       |
| [**InputTypeSet**](/previous-versions/ms807638(v=msdn.10))                       | Esegue una query per determinare se il tipo di supporto è stato impostato su un flusso di input.           |
| [**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))   | Esegue una query per determinare se un flusso di input può accettare più input.               |
| [**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))   | Esegue una query per determinare se un flusso di input può accettare un determinato tipo di supporto.       |
| [**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10)) | Esegue una query per determinare se un flusso di output può accettare un determinato tipo di supporto.      |
| [**Lock**](/previous-versions/ms809100(v=msdn.10))                                       | Blocca l'DMO                                                        |
| [**OutputType**](/previous-versions/ms807644(v=msdn.10))                           | Recupera il tipo di supporto corrente per un flusso di output specificato.      |
| [**OutputTypeSet**](/previous-versions/ms807649(v=msdn.10))                     | Esegue una query per determinare se il tipo di supporto è stato impostato su un flusso di output.          |
| [**Sblocca**](/previous-versions/ms809101(v=msdn.10))                                   | Sblocca il DMO                                                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Dmoimpl.h</dt> </dl>                                                                     |
| Libreria<br/> | <dl> <dt>Dmoguids.lib; </dt> <dt>Msdmo.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DMO Riferimento](dmo-reference.md)
</dt> <dt>

[Uso del modello DMO classe](using-the-dmo-class-template.md)
</dt> </dl>

 

 
