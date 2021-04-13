---
description: Panoramica dei controlli input penna per il Tablet PC.
ms.assetid: 03229b86-f59b-4946-8816-fa153af57630
title: Controlli Ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1206c5e77c12c31a80dcfbca0bebf317a28e0e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525968"
---
# <a name="ink-controls"></a>Controlli Ink

La piattaforma Tablet PC fornisce due controlli, [InkEdit](inkedit-control.md) e [InkPicture](inkpicture-control.md), che consentono di aggiungere facilmente il riconoscimento di input penna e grafia alle applicazioni Tablet PC. Il controllo InkEdit ha versioni [gestite](/previous-versions/ms835842(v=msdn.10)), [ActiveX](inkedit-control-reference.md) e Win32, mentre InkPicture include solo le versioni gestite [InkPicture](/previous-versions/ms583740(v=vs.100)) e [ActiveX](inkpicture-control-reference.md) .

La differenza principale tra i controlli è la modalità di salvataggio dei dati. Per impostazione predefinita, il controllo [InkEdit](inkedit-control.md) Salva l'input penna come testo, mentre [InkPicture](inkpicture-control.md) Salva l'input penna come input penna.

Il controllo [InkEdit](inkedit-control.md) è destinato alla voce di testo tramite il riconoscimento della grafia. [InkPicture](inkpicture-control.md) è progettato per l'annotazione, ad esempio per contrassegnare una diapositiva della presentazione o un'altra immagine.

Nel codice gestito, creare controlli Ink nello stesso thread del thread principale per il form. Se un controllo [InkEdit](inkedit-control.md) o [InkPicture](inkpicture-control.md) viene creato in un thread diverso, è possibile che l'applicazione non risponda correttamente.

È necessario modificare in modo esplicito il modello di threading in Apartment a thread singolo (STA) prima di creare un controllo Ink. In questo modo il controllo viene creato nel thread principale. È possibile utilizzare il codice C++ gestito seguente per impostare in modo esplicito il modello di Threading.


```C++
Thread::get_CurrentThread()->set_ApartmentState(ApartmentState::STA);
```



È possibile utilizzare il codice seguente per eseguire la stessa operazione in C \# .


```C++
System.Threading.Thread.CurrentThread.ApartmentState = System.Threading.ApartmentState.STA;
```



Nel codice gestito, per evitare una perdita di memoria, è necessario chiamare in modo esplicito il metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) su qualsiasi controllo Tablet PC a cui è stato collegato un gestore eventi prima che il controllo esca dall'ambito.

Le sezioni seguenti descrivono i controlli Ink e l'uso dei controlli Ink nelle applicazioni:

-   [Aggiunta di controlli Ink a un progetto](adding-ink-controls-to-a-project.md)
-   [Controllo InkEdit](inkedit-control.md)
-   [Controllo InkPicture](inkpicture-control.md)

 

 
