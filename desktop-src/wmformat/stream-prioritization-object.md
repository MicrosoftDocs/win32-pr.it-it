---
title: Oggetto di assegnazione di priorità del flusso
description: Oggetto di assegnazione di priorità del flusso
ms.assetid: cb0345ce-6847-435b-8cbb-f8b93856af9f
keywords:
- Windows Media Format SDK, oggetti di assegnazione di priorità di flusso
- ASF (Advanced Systems Format), oggetti di assegnazione di priorità dei flussi
- ASF (formato avanzato dei sistemi), oggetti di assegnazione di priorità dei flussi
- oggetti, oggetti di assegnazione di priorità di flusso
- oggetti di assegnazione di priorità di flusso
- flussi, oggetti di assegnazione di priorità di flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cce4189f64e85cca4e0d649dbc00409cf9d7c06
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299436"
---
# <a name="stream-prioritization-object"></a>Oggetto di assegnazione di priorità del flusso

Un oggetto di assegnazione di priorità del flusso viene usato per specificare un ordine di importanza per i flussi in un profilo. Quando la riproduzione completa non è possibile a causa di limitazioni della velocità in bit, i flussi con priorità più bassa saranno il primo a essere eliminati.

È possibile creare oggetti di assegnazione di priorità del flusso per i dati di assegnazione di priorità del flusso esistenti in un profilo o crearli vuoti, pronti per la ricezione di nuovi dati. Gli oggetti di assegnazione di priorità dei flussi non possono esistere indipendentemente da un oggetto profilo. Per salvare il contenuto di un oggetto di assegnazione di priorità del flusso, è necessario chiamare [**IWMProfile3:: SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization). Per creare un oggetto di assegnazione di priorità del flusso, usare uno dei metodi seguenti.



| Metodo                                                                                          | Descrizione                                                                  |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**IWMProfile3::CreateNewStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization) | Crea un oggetto di assegnazione di priorità del flusso senza dati.                     |
| [**IWMProfile3::GetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)             | Crea un oggetto di assegnazione di priorità del flusso popolato con i dati del profilo. |



 

In entrambi i metodi della tabella precedente è stato impostato un puntatore a un'interfaccia **IWMStreamPrioritization** . Si tratta dell'unica interfaccia supportata dall'oggetto di assegnazione di priorità del flusso.



| Interfaccia                                                  | Descrizione                                                          |
|------------------------------------------------------------|----------------------------------------------------------------------|
| [**IWMStreamPrioritization**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization) | Gestisce l'elenco di flussi all'interno dell'oggetto di assegnazione di priorità del flusso. |



 

## <a name="remarks"></a>Commenti

Per un determinato profilo possono esistere solo una priorità di flusso. Se si crea una nuova priorità di flusso per un profilo che contiene già una priorità di flusso, quella precedente verrà eliminata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Oggetto profilo**](profile-object.md)
</dt> <dt>

[**Uso della priorità di flusso**](using-stream-prioritization.md)
</dt> </dl>

 

 




