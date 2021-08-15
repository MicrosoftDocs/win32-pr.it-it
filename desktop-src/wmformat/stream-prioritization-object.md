---
title: Oggetto di definizione delle priorità dei flussi
description: Oggetto di definizione delle priorità dei flussi
ms.assetid: cb0345ce-6847-435b-8cbb-f8b93856af9f
keywords:
- Windows Media Format SDK, oggetti di definizione delle priorità dei flussi
- Advanced Systems Format (ASF), oggetti di definizione delle priorità dei flussi
- ASF (Advanced Systems Format),stream prioritization objects
- oggetti,oggetti di definizione della priorità del flusso
- oggetti di definizione delle priorità dei flussi
- streams,stream prioritization objects
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a0d8ce386dfa6d3eed64361d77326c515feadb2a6aa05eb697e402d120a55ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699968"
---
# <a name="stream-prioritization-object"></a>Oggetto di definizione delle priorità dei flussi

Un oggetto di priorità del flusso viene usato per specificare un ordine di importanza per i flussi in un profilo. Quando la riproduzione completa non è possibile a causa di limitazioni della velocità in bit, i flussi con priorità più bassa saranno i primi a essere eliminati.

Gli oggetti di definizione delle priorità dei flussi possono essere creati per i dati di priorità del flusso esistenti in un profilo o possono essere creati vuoti, pronti per ricevere nuovi dati. Gli oggetti di priorità del flusso non possono esistere indipendentemente da un oggetto profilo. Per salvare il contenuto di un oggetto di priorità del flusso, è necessario chiamare [**IWMProfile3::SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization). Per creare un oggetto di priorità del flusso, usare uno dei metodi seguenti.



| Metodo                                                                                          | Descrizione                                                                  |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**IWMProfile3::CreateNewStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization) | Crea un oggetto di priorità del flusso senza dati.                     |
| [**IWMProfile3::GetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)             | Crea un oggetto di priorità del flusso popolato con i dati del profilo. |



 

Entrambi i metodi nella tabella precedente impostano un puntatore a **un'interfaccia IWMStreamPrioritization.** Si tratta dell'unica interfaccia supportata dall'oggetto di definizione delle priorità del flusso.



| Interfaccia                                                  | Descrizione                                                          |
|------------------------------------------------------------|----------------------------------------------------------------------|
| [**IWMStreamPrioritization**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization) | Gestisce l'elenco di flussi all'interno dell'oggetto di priorità del flusso. |



 

## <a name="remarks"></a>Commenti

Per un determinato profilo può esistere una sola priorità del flusso. Se si crea una nuova priorità del flusso per un profilo che contiene già una priorità di flusso, quella precedente verrà eliminata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Oggetto Profile**](profile-object.md)
</dt> <dt>

[**Uso della priorità del flusso**](using-stream-prioritization.md)
</dt> </dl>

 

 




