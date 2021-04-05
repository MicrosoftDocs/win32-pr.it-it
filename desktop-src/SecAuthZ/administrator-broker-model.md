---
description: L'applicazione è divisa in due programmi. Uno dei programmi viene eseguito come utente standard e l'altro viene eseguito con privilegi di amministratore.
ms.assetid: 1e661915-5797-421d-b96f-72949f441aba
title: Modello di broker amministratore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299d35c995fb56f969fc5983864cfc93b25b6c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882642"
---
# <a name="administrator-broker-model"></a>Modello di broker amministratore

Nel modello di broker di amministrazione, l'applicazione è divisa in due programmi. Uno dei programmi viene eseguito come utente standard e l'altro viene eseguito con privilegi di amministratore.

Utilizzando un manifesto dell'applicazione, contrassegnare il programma utente standard con un **requestedExecutionLevel** di **asInvoker** e contrassegnare il programma amministrativo con **requestedExecutionLevel** **requireAdministrator**. Un utente avvia prima il programma utente standard. Quando l'utente tenta di eseguire un'operazione che richiede un token di accesso amministratore completo, il programma utente standard chiama la funzione [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) per avviare il programma amministrativo. La funzione **ShellExecute** richiede l'approvazione dell'utente prima di eseguire l'applicazione con il token di accesso amministratore completo dell'utente. Il programma amministrativo può quindi eseguire attività che richiedono privilegi di amministratore.

Il programma di amministrazione non è completamente isolato dal programma utente standard. Il programma amministrativo può abilitare la comunicazione interprocesso con il programma utente standard. Tuttavia, tale comunicazione è limitata dai criteri di integrità obbligatori predefiniti. Per informazioni sulle considerazioni sull'integrità obbligatoria, vedere [progettazione di applicazioni per l'esecuzione a un livello di integrità basso](/previous-versions/dotnet/articles/bb625960(v=msdn.10)).

Di seguito sono riportati gli utilizzi possibili per il modello di broker amministratore:

-   Sviluppo di procedure guidate. Quando una procedura guidata hardware determina che un driver richiesto non è installato nel computer o che si trova nella posizione approvata dell'organizzazione, chiama un'applicazione con privilegi elevati con la possibilità di spostare un driver nell'archivio del computer.
-   Autorun.exe la chiamata di Setup.exe. Quando un utente esegue software da un CD, Autorun.exe, che viene eseguito come utente standard, avvia Setup.exe, che viene eseguito come amministratore, per installare il software nel computer.

Di seguito sono riportati gli svantaggi dell'utilizzo del modello di broker Administrator:

-   Le transizioni dall'applicazione all'applicazione possono confondere l'utente. Può essere difficile informare l'utente del motivo per cui viene visualizzata una nuova applicazione sul monitor.
-   Può essere difficile passare le informazioni sullo stato tra le due applicazioni. Non è ad esempio possibile usare questo modello per passare le informazioni sullo stato tra un pannello di controllo utente standard (CPL) e la relativa controparte amministratore semplicemente per consentire allo stesso CPL di avere funzionalità utente amministrative e standard. L'utente standard CPL avrebbe dovuto archiviare lo stato in un punto qualsiasi.
-   Quando si suddivide la funzionalità tra due programmi, può essere presente una grande quantità di codice replicato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di applicazioni che richiedono privilegi di amministratore](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Modello a oggetti COM dell'amministratore](administrator-com-object-model.md)
</dt> <dt>

[Modello di servizio del sistema operativo](operating-system-service-model.md)
</dt> <dt>

[Modello di attività con privilegi elevati](elevated-task-model.md)
</dt> </dl>

 

 
