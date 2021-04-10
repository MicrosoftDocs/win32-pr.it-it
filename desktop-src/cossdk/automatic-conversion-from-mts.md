---
description: Conversione automatica da MTS
ms.assetid: 0848639a-26ce-47ad-8384-8969a7c3bcde
title: Conversione automatica da MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d424a443995c9fff9073878a43543d4c029a2445
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127166"
---
# <a name="automatic-conversion-from-mts"></a>Conversione automatica da MTS

La conversione automatica viene eseguita in due passaggi, come indicato di seguito:

1.  Durante l'installazione di Windows. La conversione viene gestita dal processo di installazione di Windows tramite l'utilità MTSTOCOM.
    > [!Note]  
    > Se il passaggio 1 ha esito negativo, è possibile che alcuni o tutti i pacchetti MTS siano stati effettivamente convertiti, ma che alcune proprietà siano mancanti. In questo caso, utilizzare lo strumento di amministrazione Servizi componenti per verificare tutti gli attributi. Gli attributi MTS saranno ancora presenti nel computer (nel registro di sistema nel computer locale HKEY \_ \_ \\ Microsoft \\ Transaction Server) ma saranno accessibili solo tramite l'utilità regedit.exe.

     

2.  Dopo l'ultimo riavvio prima della visualizzazione della finestra di dialogo di accesso di Windows. Il passaggio 2 gestisce le azioni di conversione che richiedono l'accesso alla rete (principalmente la creazione di membri del ruolo).
    > [!Note]  
    > Se il passaggio 2 ha esito negativo (a causa di errori di rete o del controller di dominio temporanei), è possibile eseguire di nuovo l'utilità di conversione MTSTOCOM per un numero qualsiasi di volte. A tale scopo, al prompt dei comandi o dopo aver selezionato **Esegui** dal menu **Start** , digitare quanto segue: **% windir% \\ system32 \\mtstocom.exe**.

     

## <a name="mtstocom-log-file"></a>File di log MTSTOCOM

L'utilità MTSTOCOM genera un file di log (Mtstocom. log) nella directory Windows. Questo file di log mantiene un record della conversione da pacchetti MTS a applicazioni COM+. Se si sono verificati errori durante il processo di conversione, è sempre consigliabile controllare il file di log per ulteriori informazioni. Il file di log rileva i problemi comuni, ad esempio l'utente o la password non valida.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risultati e problemi di conversione COM+](com--conversion-results-and-issues.md)
</dt> <dt>

[Conversione manuale da MTS](manual-conversion-from-mts.md)
</dt> <dt>

[Libreria di amministrazione MTS](mts-administration-library.md)
</dt> </dl>

 

 



