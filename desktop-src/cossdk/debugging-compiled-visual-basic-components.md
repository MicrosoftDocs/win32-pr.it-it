---
description: Poiché in molti casi sarà possibile eseguire il debug solo di una parte delle funzionalità dei componenti all'interno dell'ambiente Microsoft Visual Basic, sarà necessario eseguire il debug dei componenti compilati con Visual Basic dopo che sono stati compilati. Poiché l'Visual Basic non abilita questa funzionalità, è necessario usare l'ambiente Microsoft Visual C++ locale.
ms.assetid: a58c5884-3c2d-4699-8b19-277003912dfd
title: Debug di componenti Visual Basic compilati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2dec15f90d14d534221193020417415d11ddec
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882985"
---
# <a name="debugging-compiled-visual-basic-components"></a>Debug di componenti Visual Basic compilati

Poiché in molti casi sarà possibile eseguire il debug solo di una parte delle funzionalità del componente all'interno dell'ambiente Microsoft Visual Basic, sarà necessario eseguire il debug dei componenti compilati con Visual Basic dopo che sono stati compilati. Poiché l'Visual Basic non abilita questa funzionalità, è necessario usare l'ambiente Microsoft Visual C++ locale.

**Per eseguire il debug Visual Basic componente nell'Visual C++ locale**

1.  In Visual Basic 6.0 aprire il Visual Basic di cui si vuole eseguire il debug.

2.  Scegliere **Crea** YourProject.dlldal menu **File**.

3.  Nella finestra **di dialogo Project** fare clic su **Opzioni**.

4.  Nella scheda Compila **della** finestra di dialogo Project  proprietà fare clic  su Compila in codice nativo e nessuna ottimizzazione e selezionare la casella di controllo Crea informazioni **di debug** simbolico . 

5.  Fare **clic su OK** e quindi di nuovo su **OK** per compilare il progetto.

6.  Spostare la DLL compilata nel percorso in cui vengono normalmente installate le applicazioni COM+.

    > [!Note]  
    > Se non si sposta la DLL, è possibile che venga visualizzato un messaggio di errore che informa che non è stato possibile trovare informazioni di debug simboliche per la DLL. Se si verificano problemi durante l'arresto del debugger in corrispondenza dei punti di interruzione nel componente, verificare che la DLL si trova nella directory dei pacchetti standard, eliminare il componente dal relativo pacchetto e aggiungere di nuovo il componente.

     

7.  Avviare Visual C++.

8.  Scegliere **Apri** area di lavoro dal menu **File**.

9.  Nella finestra **di dialogo Apri** area di lavoro impostare File **di** tipo su Tutti i **file( \* . \* ),** selezionare il componente compilato e fare clic su **Apri**.

10. Scegliere **Apri** (non  Apri area di **lavoro)** dal menu File e aprire il modulo Visual Basic (bas), il modulo (con estensione frm) o la classe (con estensione cls) di cui si vuole eseguire il debug.

11. Nel menu **Project** fare clic su **Impostazioni**.

12. Nella scheda **Debug** della finestra  di dialogo Project Impostazioni selezionare **Generale** nella **casella** Categoria.

13. Nella casella **Eseguibile per la** sessione di debug immettere il percorso completo per Dllhost.exe, seguito da un argomento che specifica l'ID processo dell'applicazione COM+ contenente il componente. L'ID processo è visualizzato nella **scheda Generale** della finestra di dialogo Proprietà dell'applicazione COM+.  Di seguito è riportato un esempio: C: \\ Winnt \\ System32 \\Dllhost.exe /ProcessID:{ &lt; processID &gt; }.

14. Fare clic su **OK**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto del debug Visual Basic COM+ a differenza di MTS](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[Debug nell'IDE Visual Basic](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 



