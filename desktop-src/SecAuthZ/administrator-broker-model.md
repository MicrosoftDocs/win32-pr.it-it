---
description: L'applicazione è suddivisa in due programmi. Uno dei programmi viene eseguito come utente standard e l'altro viene eseguito con privilegi di amministratore.
ms.assetid: 1e661915-5797-421d-b96f-72949f441aba
title: Modello broker amministratore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c67a68c823221226f56d01b750ab74a70ca30530f44cd174e333c3e4d7cbaa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784942"
---
# <a name="administrator-broker-model"></a>Modello broker amministratore

Nel modello di broker amministratore, l'applicazione è divisa in due programmi. Uno dei programmi viene eseguito come utente standard e l'altro viene eseguito con privilegi di amministratore.

Usando un manifesto dell'applicazione, contrassegnare il programma utente standard con **requestedExecutionLevel** **asInvoker** e contrassegnare il programma amministrativo con **requestedExecutionLevel** di **requireAdministrator**. Un utente avvia prima il programma utente standard. Quando l'utente tenta di eseguire un'operazione che richiede un token di accesso amministratore completo, il programma utente standard chiama la funzione [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) per avviare il programma amministrativo. La **funzione ShellExecute richiede** l'approvazione dell'utente prima di eseguire l'applicazione con il token di accesso amministratore completo dell'utente. Il programma amministrativo può quindi eseguire attività che richiedono privilegi di amministratore.

Il programma amministrativo non è completamente isolato dal programma utente standard. Il programma amministrativo può consentire la comunicazione interprocesso con il programma utente standard. Tuttavia, tale comunicazione è limitata dai criteri di integrità obbligatori predefiniti. Per informazioni sulle considerazioni sull'integrità obbligatoria, vedere [Progettazione di applicazioni da eseguire a un livello di integrità basso.](/previous-versions/dotnet/articles/bb625960(v=msdn.10))

Di seguito sono riportati i possibili usi per il modello di broker amministratore:

-   Sviluppo di procedure guidate. Quando una procedura guidata hardware determina che un driver richiesto non è installato nel computer o si trova nella posizione approvata dell'azienda, chiama un'applicazione con privilegi elevati con la possibilità di spostare un driver nell'archivio computer.
-   Autorun.exe chiamare Setup.exe. Quando un utente esegue il software da un CD, Autorun.exe, che viene eseguito come utente standard, avvia Setup.exe, che viene eseguito come amministratore, per installare il software nel computer.

Di seguito sono riportati alcuni svantaggi dell'uso del modello di broker amministratore:

-   Le transizioni da applicazione a applicazione possono generare confusione per l'utente. Può essere difficile informare l'utente del motivo per cui viene visualizzata una nuova applicazione sul monitor.
-   Può essere difficile passare informazioni sullo stato tra le due applicazioni. Ad esempio, questo modello non viene utilizzato per passare informazioni sullo stato tra un pannello di controllo utente standard (CPL) e la relativa controparte di amministratore semplicemente per consentire allo stesso CPL di disporre di funzionalità utente standard e amministrative. La libreria CPL dell'utente standard deve archiviarne lo stato in un punto qualsiasi.
-   Quando si suddivide la funzionalità tra due programmi, può essere presente una grande quantità di codice replicato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di applicazioni che richiedono privilegi di amministratore](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Modello a oggetti COM administrator](administrator-com-object-model.md)
</dt> <dt>

[Modello di servizio del sistema operativo](operating-system-service-model.md)
</dt> <dt>

[Modello di attività con privilegi elevati](elevated-task-model.md)
</dt> </dl>

 

 
