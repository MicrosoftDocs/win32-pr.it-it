---
title: Considerazioni sulla programmazione (Utilità di pianificazione)
description: Quando si sviluppano applicazioni che usano la Utilità di pianificazione 1,0, tenere presenti i seguenti problemi di programmazione. L'applicazione deve verificare che il servizio Utilità di pianificazione sia in esecuzione prima di eseguire qualsiasi chiamata usando l'API Utilità di pianificazione. Quando si recuperano le stringhe, assicurarsi di chiamare CoTaskMemFree per rilasciare ogni stringa dopo che non è più necessaria. Quando si recuperano matrici di stringhe, assicurarsi prima di tutto di rilasciare ogni stringa nella matrice e quindi rilasciare la matrice stessa. Quando si crea o si modifica un elemento di lavoro, inclusi i trigger associati a un elemento di lavoro, assicurarsi di chiamare IPersistFile Save per salvare l'elemento di lavoro su disco. Dopo aver usato le interfacce fornite dall'API Utilità di pianificazione, assicurarsi di chiamare la versione IUnknown per rilasciare l'interfaccia. IUnknown è supportato da ogni oggetto Utilità di pianificazione.
ms.assetid: b9e1806c-acfa-4d44-a371-91bad788648c
keywords:
- avvio Utilità di pianificazione
- Considerazioni sulla programmazione Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599652f4a25f3d99020eda0846c41904ee76e5cf
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300754"
---
# <a name="programming-considerations-task-scheduler"></a>Considerazioni sulla programmazione (Utilità di pianificazione)

Quando si sviluppano applicazioni che usano la Utilità di pianificazione 1,0, tenere presenti i seguenti problemi di programmazione.

-   L'applicazione deve verificare che il servizio Utilità di pianificazione sia in esecuzione prima di eseguire qualsiasi chiamata usando l'API Utilità di pianificazione.
-   Quando si recuperano le stringhe, assicurarsi di chiamare [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare ogni stringa dopo che non è più necessaria. Quando si recuperano matrici di stringhe, assicurarsi prima di tutto di rilasciare ogni stringa nella matrice e quindi rilasciare la matrice stessa.
-   Quando si crea o si modifica un elemento di lavoro, inclusi i trigger associati a un elemento di lavoro, assicurarsi di chiamare [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) per salvare l'elemento di lavoro su disco.
-   Dopo aver usato le interfacce fornite dall'API di Utilità di pianificazione, assicurarsi di chiamare [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) per rilasciare l'interfaccia. [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) è supportato da ogni oggetto utilità di pianificazione.

Nella sezione using della documentazione Utilità di pianificazione sono disponibili numerosi esempi che seguono queste linee guida. Nella tabella seguente vengono forniti alcuni esempi.

| Per un esempio di         | Vedere                                                                                        |
|---------------------------|--------------------------------------------------------------------------------------------|
| Rilascio di stringhe         | [Recupero degli esempi di proprietà degli elementi di lavoro](retrieving-work-item-property-examples.md)       |
| Salvataggio degli elementi di lavoro su disco | [Impostazione degli esempi di proprietà degli elementi di lavoro](setting-work-item-property-examples.md)             |
| Rilascio di interfacce      | [Esempio di creazione di un'attività con NewWorkItem](creating-a-task-using-newworkitem-example.md) |



 

 

 
