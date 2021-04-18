---
description: L'oggetto divisore consente di accedere alle funzionalità di analisi del layout di Tablet PC.
ms.assetid: 9fa299fe-3713-4fa8-95c6-be15f144103a
title: Utilizzo dell'oggetto divisore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fd158f85d368d764bce17e8b481ebe625a4d6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306694"
---
# <a name="working-with-the-divider-object"></a>Utilizzo dell'oggetto divisore

L'oggetto [divisore](/previous-versions/ms583616(v=vs.100)) consente di accedere alle funzionalità di analisi del layout di Tablet PC.

Nel codice gestito, è possibile creare un'istanza dell'oggetto [divisore](/previous-versions/ms583616(v=vs.100)) chiamando uno dei costruttori del [divisore](/previous-versions/ms839465(v=msdn.10)) . In automazione, si tratta dell'oggetto [**InkDivider**](inkdivider-class.md) , di cui è possibile creare un'istanza chiamando il metodo [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.

È possibile ottenere uno snapshot del risultato dell'analisi corrente chiamando il metodo [divide](/previous-versions/ms839461(v=msdn.10)) dell'oggetto [divisore](/previous-versions/ms583616(v=vs.100)) . Il risultato dell'analisi viene restituito in un oggetto [DivisionResult](/previous-versions/ms839371(v=msdn.10)) . Ogni volta che si chiama il metodo divide, l'oggetto divisore crea un oggetto DivisionResult. Per ulteriori informazioni sull'oggetto DivisionResult, vedere [utilizzo dell'oggetto DivisionResult](working-with-the-divisionresult-object.md).

La raccolta [Strokes](/previous-versions/ms552701(v=vs.100)) analizzata dall'oggetto [divisore](/previous-versions/ms583616(v=vs.100)) è contenuta nella proprietà [Strokes](/previous-versions/ms839422(v=msdn.10)) dell'oggetto divisore. L'oggetto divisore analizza dinamicamente la raccolta Strokes durante l'aggiunta o l'eliminazione dalla raccolta. Per ulteriori informazioni sulla proprietà Strokes dell'oggetto divisore, vedere [utilizzo di una raccolta Strokes](working-with-a-strokes-collection.md).

L'oggetto [divisore](/previous-versions/ms583616(v=vs.100)) utilizza un contesto di riconoscimento per migliorare l'analisi dei segmenti di riconoscimento e generare testo di riconoscimento per gli elementi di grafia. È possibile impostare il contesto del riconoscimento utilizzando la proprietà [RecognizerContext](/previous-versions/ms839415(v=msdn.10)) dell'oggetto divisore. Non è possibile modificare la proprietà RecognizerContext dopo che sono stati assegnati Strokes all'oggetto divisore. Per ulteriori informazioni sulla proprietà RecognizerContext dell'oggetto divisore, vedere [utilizzo di un contesto del riconoscitore](working-with-a-recognizer-context.md).

> [!Caution]  
> Nel codice gestito, è necessario chiamare il metodo [Dispose](/previous-versions/ms839450(v=msdn.10)) sull'oggetto prima che esca dall'ambito. Questo oggetto gestisce le risorse non gestite. Basarsi sulla finalizzazione per questo oggetto può causare perdite di memoria ed eccezioni all'interno dell'applicazione.

 

 

 
