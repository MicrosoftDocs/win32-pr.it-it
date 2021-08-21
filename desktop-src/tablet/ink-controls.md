---
description: Panoramica dei controlli input penna per Tablet PC.
ms.assetid: 03229b86-f59b-4946-8816-fa153af57630
title: Controlli input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f07a26d30746f99b291053276de20ef78c5ce4b4f0c7a14afce6633684b7b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032339"
---
# <a name="ink-controls"></a>Controlli input penna

La piattaforma Tablet PC offre due controlli, [InkEdit](inkedit-control.md) e [InkPicture,](inkpicture-control.md)che consentono di aggiungere facilmente il riconoscimento dell'input penna e della grafia alle applicazioni Tablet PC. Il controllo InkEdit [ha](/previous-versions/ms835842(v=msdn.10))gestito le [versioni , ActiveX](inkedit-control-reference.md) e Win32, mentre InkPicture ha solo le versioni [InkPicture](/previous-versions/ms583740(v=vs.100)) [e ActiveX](inkpicture-control-reference.md) gestite.

La differenza principale tra i controlli è la modalità di salvataggio dei dati. Il [controllo InkEdit](inkedit-control.md) salva l'input penna come testo per impostazione predefinita, mentre [InkPicture](inkpicture-control.md) salva l'input penna come input penna.

Il [controllo InkEdit](inkedit-control.md) è destinato all'immissione di testo tramite il riconoscimento della grafia. [InkPicture è progettato](inkpicture-control.md) per l'annotazione, ad esempio per contrassegnare una diapositiva di presentazione o un'altra immagine.

Nel codice gestito creare controlli input penna nello stesso thread del thread principale per il form. Se viene [creato un controllo InkEdit](inkedit-control.md) o [InkPicture](inkpicture-control.md) in un thread diverso, l'applicazione potrebbe non rispondere correttamente.

È necessario modificare in modo esplicito il modello di threading in apartment a thread singolo (STA) prima di creare un controllo input penna. In questo modo il controllo viene creato nel thread principale. È possibile usare il codice C++ gestito seguente per impostare in modo esplicito il modello di threading.


```C++
Thread::get_CurrentThread()->set_ApartmentState(ApartmentState::STA);
```



È possibile usare il codice seguente per eseguire la stessa operazione in C \# .


```C++
System.Threading.Thread.CurrentThread.ApartmentState = System.Threading.ApartmentState.STA;
```



Nel codice gestito, per evitare una perdita di memoria è necessario chiamare in modo esplicito il metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) su qualsiasi controllo Tablet PC a cui è stato associato un gestore eventi prima che il controllo eserne l'ambito.

Le sezioni seguenti descrivono i controlli input penna e l'uso dei controlli input penna nelle applicazioni:

-   [Aggiunta di controlli input penna a un Project](adding-ink-controls-to-a-project.md)
-   [Controllo InkEdit](inkedit-control.md)
-   [Controllo InkPicture](inkpicture-control.md)

 

 
