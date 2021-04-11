---
description: Poiché in molti casi sarà possibile eseguire il debug solo di una parte della funzionalità dei componenti all'interno dell'ambiente Microsoft Visual Basic, in alcune situazioni sarà necessario eseguire il debug dei componenti compilati con Visual Basic dopo che sono stati compilati. Poiché l'ambiente Visual Basic non lo Abilita, è necessario usare invece l'ambiente Microsoft Visual C++.
ms.assetid: a58c5884-3c2d-4699-8b19-277003912dfd
title: Debug di componenti Visual Basic compilati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b32a39f0f1c50e1da4c9534b40658838361225
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126711"
---
# <a name="debugging-compiled-visual-basic-components"></a>Debug di componenti Visual Basic compilati

Poiché in molti casi sarà possibile eseguire il debug solo di una parte delle funzionalità del componente all'interno dell'ambiente Microsoft Visual Basic, in alcune situazioni sarà necessario eseguire il debug dei componenti compilati con Visual Basic dopo che sono stati compilati. Poiché l'ambiente Visual Basic non lo Abilita, è necessario usare invece l'ambiente Microsoft Visual C++.

**Per eseguire il debug di un componente Visual Basic nell'ambiente Visual C++**

1.  In Visual Basic 6,0 aprire il progetto Visual Basic di cui si desidera eseguire il debug.

2.  Scegliere **Make YourProject.dll** dal menu **file** .

3.  Nella finestra di dialogo **Crea progetto** fare clic su **Opzioni**.

4.  Nella scheda **Compila** della finestra di dialogo **Proprietà progetto** fare clic su **Compila in codice nativo** e **Nessuna ottimizzazione** , quindi selezionare la casella di controllo **Crea informazioni di debug simbolico** .

5.  Fare clic su **OK**, quindi fare di nuovo clic su **OK** per compilare il progetto.

6.  Spostare la DLL compilata nel percorso in cui sono normalmente installate le applicazioni COM+.

    > [!Note]  
    > Se la DLL non viene spostata, potrebbe essere presente un messaggio di errore che informa che non è stato possibile trovare le informazioni di debug simboliche per la DLL. Se si verificano problemi durante l'arresto del debugger in corrispondenza di punti di interruzione nel componente, verificare che la DLL si trovi nella directory dei pacchetti standard, eliminare il componente dal pacchetto e aggiungere nuovamente il componente.

     

7.  Avviare Visual C++.

8.  Scegliere **Apri area di lavoro** dal menu **file** .

9.  Nella finestra di dialogo **Apri area di lavoro** impostare **file di tipo** su **tutti i file ( \* . \* )**, selezionare il componente compilato e fare clic su **Apri**.

10. Dal menu **file** , fare clic su **Apri** (non **aprire area di lavoro**) e aprire il modulo Visual Basic (. Bas), il form (. frm) o la classe (. CLS) di cui si desidera eseguire il debug.

11. Scegliere **Impostazioni** dal menu **progetto** .

12. Nella scheda **debug** della finestra di dialogo **Impostazioni progetto** selezionare **generale** nella casella **categoria** .

13. Nella casella **eseguibile per la sessione di debug** immettere il percorso completo per Dllhost.exe, seguito da un argomento che specifica l'ID di processo dell'applicazione com+ contenente il componente. L'ID del processo è presente nella scheda **generale** della finestra di dialogo **Proprietà** dell'applicazione com+. Di seguito è riportato un esempio: C: \\ WinNT \\ system32 \\Dllhost.exe/ProcessId: { <processID> }.

14. Fare clic su **OK**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto per il debug di Visual Basic COM+ a differenza di MTS](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[Debug nell'IDE di Visual Basic](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 



