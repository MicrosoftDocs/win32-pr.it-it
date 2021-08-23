---
description: Conversione automatica da MTS
ms.assetid: 0848639a-26ce-47ad-8384-8969a7c3bcde
title: Conversione automatica da MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e02cc3889c479d829290b22b71edf13cc4ebc8f419c333d5e99390d47c01da65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549488"
---
# <a name="automatic-conversion-from-mts"></a>Conversione automatica da MTS

La conversione automatica avviene in due passaggi, come indicato di seguito:

1.  Durante Windows configurazione. La conversione viene gestita dal processo di Windows di installazione tramite l'utilità MTSTOCOM.
    > [!Note]  
    > Se il passaggio 1 non riesce, alcuni o tutti i pacchetti MTS potrebbero essere stati effettivamente convertiti, ma potrebbero mancare determinate proprietà. In questo caso, usare lo strumento amministrativo Servizi componenti per verificare tutti gli attributi. Gli attributi MTS saranno ancora presenti nel computer (nel Registro di sistema in HKEY LOCAL MACHINE Microsoft Transaction Server), ma saranno accessibili solo tramite \_ \_ \\ l'utilità \\ regedit.exe.

     

2.  Dopo l'ultimo riavvio prima Windows viene visualizzata la finestra di dialogo di accesso. Il passaggio 2 gestisce le azioni di conversione che richiedono l'accesso alla rete (principalmente la creazione di membri del ruolo).
    > [!Note]  
    > Se il passaggio 2 non riesce (a causa di errori temporanei della rete o del controller di dominio), è possibile eseguire di nuovo l'utilità di conversione MTSTOCOM per un numero qualsiasi di volte. A tale scopo, al prompt  dei comandi o dopo aver selezionato Esegui dal menu **Start** digitare quanto segue: **%windir% \\ system32 \\mtstocom.exe**.

     

## <a name="mtstocom-log-file"></a>MTSTOCOM Log File

L'utilità MTSTOCOM genera un file di log (Mtstocom.log) nella directory Windows. Questo file di log mantiene un record della conversione dai pacchetti MTS alle applicazioni COM+. Se si sono verificati errori durante il processo di conversione, è sempre buona idea controllare il file di log per altre informazioni. Il file di log rileva i problemi comuni, ad esempio utente o password non validi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risultati e problemi della conversione COM+](com--conversion-results-and-issues.md)
</dt> <dt>

[Conversione manuale da MTS](manual-conversion-from-mts.md)
</dt> <dt>

[Libreria di amministrazione MTS](mts-administration-library.md)
</dt> </dl>

 

 



