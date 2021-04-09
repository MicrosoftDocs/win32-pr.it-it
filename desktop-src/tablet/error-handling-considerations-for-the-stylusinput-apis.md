---
description: Panoramica della gestione degli errori quando si usano le API (Application Programming Interface) di StylusInput.
ms.assetid: 7d7ff5b2-3eda-4570-96fe-b3b8f41ff69b
title: Considerazioni sulla gestione degli errori per l'API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fa582a8dbf531588f6d3d0c142c4ec7b40a058
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966732"
---
# <a name="error-handling-considerations-for-the-stylusinput-api"></a>Considerazioni sulla gestione degli errori per l'API StylusInput

Le eccezioni non gestite generate da un plug-in vengono rilevate dall'oggetto [**RealTimeStylus**](realtimestylus-class.md) . Quando un plug-in genera un'eccezione, il flusso di dati normale viene interrotto. Oggetto **RealTimeStylus** :

1.  Crea un oggetto [ErrorData](/previous-versions/ms575221(v=vs.100)) (nel codice gestito).
2.  Chiama il metodo [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) (nel codice gestito, ovvero il metodo [Microsoft. StylusInput. IStylusSyncPlugin. Error](/previous-versions/ms824754(v=msdn.10)) o [Microsoft. StylusInput. IStylusAsyncPlugin. Error](/previous-versions/ms824771(v=msdn.10)) ) del plug-in che ha generato l'eccezione.
3.  Chiama il metodo [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) degli altri plug-in della raccolta.
4.  Se il plug-in che ha generato l'eccezione è un plug-in sincrono, l'oggetto [ErrorData](/previous-versions/ms575221(v=vs.100)) (in codice gestito) viene aggiunto alla coda di output.
5.  L'oggetto [**RealTimeStylus**](realtimestylus-class.md) riprende la normale elaborazione dei dati originali.

Se un plug-in genera un'eccezione dal relativo metodo [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) , l'oggetto [**RealTimeStylus**](realtimestylus-class.md) intercetta l'eccezione, ma non genera un nuovo oggetto [ErrorData](/previous-versions/ms575221(v=vs.100)) . Per ulteriori informazioni sulla modalità di aggiunta di ErrorData alla coda, vedere [dati plug-in e classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

L'oggetto [**RealTimeStylus**](realtimestylus-class.md) non interrompe l'elaborazione dei dati dal flusso di dati della penna del tablet quando uno dei relativi plug-in genera un'eccezione. A seconda della progettazione, è possibile che alcuni plug-in debbano sottoscrivere la notifica [ErrorData](/previous-versions/ms575221(v=vs.100)) e modificarne il comportamento quando si verifica un'eccezione.

 

 
