---
description: Dato che in molti casi sarà possibile eseguire il debug solo di una parte delle funzionalità dei componenti all'interno dell'ambiente Microsoft Visual Basic, in alcune situazioni sarà necessario eseguire il debug dei componenti compilati con Visual Basic dopo che sono stati compilati. Poiché l'Visual Basic non abilita questa funzionalità, è necessario usare l'ambiente Microsoft Visual C++.
ms.assetid: a58c5884-3c2d-4699-8b19-277003912dfd
title: Debug di componenti Visual Basic compilati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eac784808602d3554e4610e70a8d8a22ef2ca1594062599ec6acd43db68b98a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128783"
---
# <a name="debugging-compiled-visual-basic-components"></a>Debug di componenti Visual Basic compilati

Dato che in molti casi sarà possibile eseguire il debug solo di una parte delle funzionalità del componente all'interno dell'ambiente Microsoft Visual Basic, in alcune situazioni sarà necessario eseguire il debug dei componenti compilati con Visual Basic dopo che sono stati compilati. Poiché l'Visual Basic non abilita questa funzionalità, è necessario usare l'ambiente Microsoft Visual C++.

**Per eseguire il debug Visual Basic componente nell'ambiente Visual C++**

1.  In Visual Basic 6.0 aprire il Visual Basic di cui si vuole eseguire il debug.

2.  Nel menu **File** fare clic su **YourProject.dll**.

3.  Nella finestra **di dialogo Project** fare clic su **Opzioni**.

4.  Nella scheda **Compila Project** finestra di  dialogo Proprietà  progetto fare clic  su Compila in codice nativo e nessuna ottimizzazione e selezionare la casella di controllo Crea informazioni **di debug** simbolico .

5.  Fare **clic su OK** e quindi di nuovo su **OK** per compilare il progetto.

6.  Spostare la DLL compilata nel percorso in cui sono normalmente installate le applicazioni COM+.

    > [!Note]  
    > Se non si sposta la DLL, è possibile che venga visualizzato un messaggio di errore che informa che non è stato possibile trovare le informazioni di debug simboliche per la DLL. In caso di problemi con l'arresto del debugger in corrispondenza dei punti di interruzione del componente, verificare che la DLL si trova nella directory dei pacchetti standard, eliminare il componente dal relativo pacchetto e aggiungere nuovamente il componente.

     

7.  Avviare Visual C++.

8.  Scegliere Apri area di lavoro **dal** menu **File.**

9.  Nella finestra **di dialogo Apri** area di lavoro impostare File **di** tipo su Tutti i file ( **. \* \* )**, selezionare il componente compilato e fare clic su **Apri**.

10. Scegliere Apri (non  Apri area di **lavoro)** dal menu **File** e aprire il modulo Visual Basic (con estensione bas), il modulo (con estensione frm) o la classe (con estensione cls) di cui si vuole eseguire il debug.

11. Nel menu **Project** fare clic su **Impostazioni**.

12. Nella finestra **Project Impostazioni** finestra di dialogo, nella **scheda Debug** , selezionare **Generale** nella **casella** Categoria .

13. Nella casella **Eseguibile per la** sessione di debug immettere il percorso completo per Dllhost.exe, seguito da un argomento che specifica l'ID processo dell'applicazione COM+ contenente il componente. L'ID processo è visualizzato nella **scheda Generale** della finestra di dialogo Proprietà dell'applicazione COM+.  Di seguito è riportato un esempio: C: \\ Winnt \\ System32 \\Dllhost.exe /ProcessID:{ <processID> }.

14. Fare clic su **OK**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto del debug Visual Basic COM+ in contrasto con MTS](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[Debug nell'IDE Visual Basic](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 



