---
description: Questa sezione descrive le funzioni IMM.
ms.assetid: 833c07eb-0ecf-41e2-9e01-8d83e51ffcef
title: Funzioni di Gestione metodi di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c0f03c2e6d29b262bd97729b92f9eea5fbf99d09f52ea3fe2b3579646a6fa8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948732"
---
# <a name="input-method-manager-functions"></a>Funzioni di Gestione metodi di input

Questa sezione descrive le funzioni IMM.



| Funzione                                                           | Descrizione                                                                                                                |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**CreateIFECommonInstance**](/windows/desktop/api/msime/nf-msime-createifecommoninstance)         | Restituisce un puntatore a [**un'interfaccia IFECommon.**](/windows/desktop/api/Msime/nn-msime-ifecommon)                                                          |
| [**CreateIFEDictionaryInstance**](/windows/desktop/api/msime/nf-msime-createifedictionaryinstance) | Restituisce un puntatore a [**un'interfaccia IFEDictionary.**](/windows/desktop/api/Msime/nn-msime-ifedictionary)                                                  |
| [**CreateIFELanguageInstance**](/windows/desktop/api/msime/nf-msime-createifelanguageinstance)     | Restituisce un puntatore a [**un'interfaccia IFELanguage.**](/windows/desktop/api/Msime/nn-msime-ifelanguage)                                                      |
| [**EnumInputContext**](/windows/desktop/api/Imm/nc-imm-imcenumproc)                       | Funzione di callback definita dall'applicazione che elabora i contesti di input forniti dalla **funzione ImmEnumInputContext.**   |
| [**EnumRegisterWordProc**](/windows/desktop/api/Imm/nc-imm-registerwordenumproca)               | Funzione di callback definita dall'applicazione usata con la **funzione ImmEnumRegisterWord.**                                   |
| [**ImmAssociateContext**](/windows/desktop/api/Imm/nf-imm-immassociatecontext)                 | Associa il contesto di input specificato alla finestra specificata.                                                          |
| [**ImmAssociateContextEx**](/windows/desktop/api/Imm/nf-imm-immassociatecontextex)             | Modifica l'associazione tra il contesto del metodo di input e la finestra specificata o i relativi elementi figlio.                         |
| [**ImmConfigureIME**](/windows/desktop/api/Imm/nf-imm-immconfigureimea)                         | Visualizza la finestra di dialogo di configurazione per l'IME dell'identificatore delle impostazioni locali di input specificato.                                |
| [**ImmCreateContext**](/windows/desktop/api/Imm/nf-imm-immcreatecontext)                       | Crea un nuovo contesto di input, allocando memoria per il contesto e inizializzando il contesto.                                        |
| [**ImmDestroyContext**](/windows/desktop/api/Imm/nf-imm-immdestroycontext)                     | Rilascia il contesto di input e libera la memoria associata.                                                                    |
| [**ImmDisableIME**](/windows/desktop/api/Imm/nf-imm-immdisableime)                             | Disabilita l'IME per un thread o per tutti i thread in un processo.                                                             |
| [**ImmDisableLegacyIME**](/windows/desktop/api/Imm/nf-imm-immdisablelegacyime)                 | Indica che questo thread è un thread dell'interfaccia Windows'interfaccia utente dell'app di Store.                                                               |
| [**ImmDisableTextFrameService**](/windows/desktop/api/Imm/nf-imm-immdisabletextframeservice)   | Deprecato. Disabilita il servizio di testo per il thread specificato.                                                            |
| [**ImmEnumInputContext**](/windows/desktop/api/Imm/nf-imm-immenuminputcontext)                 | Recupera il contesto di input per il thread specificato.                                                                      |
| [**ImmEnumRegisterWord**](/windows/desktop/api/Imm/nf-imm-immenumregisterworda)                 | Enumera le stringhe di registro con la stringa di lettura, lo stile e la stringa di registrazione specificati.                           |
| [**ImmEscape**](/windows/desktop/api/Imm/nf-imm-immescapea)                                     | Accede alle funzionalità di determinati IME non disponibili tramite altre funzioni API IME.                           |
| [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)                 | Recupera un elenco di candidati.                                                                                                |
| [**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta)       | Recupera le dimensioni degli elenchi candidati.                                                                                 |
| [**ImmGetCandidateWindow**](/windows/desktop/api/Imm/nf-imm-immgetcandidatewindow)             | Recupera informazioni sulla finestra dei candidati.                                                                         |
| [**ImmGetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta)             | Recupera informazioni sul tipo di carattere logico attualmente usato per visualizzare i caratteri nella finestra di composizione.               |
| [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa)         | Recupera informazioni sulla stringa di composizione.                                                                        |
| [**ImmGetCompositionWindow**](/windows/desktop/api/Imm/nf-imm-immgetcompositionwindow)         | Recupera informazioni sulla finestra di composizione.                                                                        |
| [**ImmGetContext**](/windows/desktop/api/Imm/nf-imm-immgetcontext)                             | Recupera il contesto di input associato alla finestra specificata.                                                          |
| [**ImmGetConversionList**](/windows/desktop/api/Imm/nf-imm-immgetconversionlista)               | Recupera l'elenco dei risultati della conversione di caratteri o parole senza generare messaggi correlati all'IME.                   |
| [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)           | Recupera lo stato di conversione corrente.                                                                                   |
| [**ImmGetDefaultIMEWnd**](/windows/desktop/api/Imm/nf-imm-immgetdefaultimewnd)                 | Recupera l'handle di finestra predefinito per la classe IME.                                                                      |
| [**ImmGetDescription**](/windows/desktop/api/Imm/nf-imm-immgetdescriptiona)                     | Copia la descrizione dell'IME nel buffer specificato.                                                                 |
| [**ImmGetGuideLine**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea)                         | Recupera informazioni sugli errori.                                                                                        |
| [**ImmGetIMEFileName**](/windows/desktop/api/Imm/nf-imm-immgetimefilenamea)                     | Recupera il nome file dell'IME associato alle impostazioni locali di input specificate.                                             |
| [**ImmGetImeMenuItems**](/windows/desktop/api/Imm/nf-imm-immgetimemenuitemsa)                   | Recupera le voci di menu registrate nel menu IME di un contesto di input specificato.                                 |
| [**ImmGetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus)                       | Determina se l'IME è aperto o chiuso.                                                                              |
| [**ImmGetProperty**](/windows/desktop/api/Imm/nf-imm-immgetproperty)                           | Recupera la proprietà e le funzionalità dell'IME associato alle impostazioni locali di input specificate.                             |
| [**ImmGetRegisterWordStyle**](/windows/desktop/api/Imm/nf-imm-immgetregisterwordstylea)         | Recupera un elenco degli stili supportati dall'IME associato alle impostazioni locali di input specificate.                            |
| [**ImmGetStatusWindowPos**](/windows/desktop/api/Imm/nf-imm-immgetstatuswindowpos)             | Recupera la posizione della finestra di stato.                                                                               |
| [**ImmGetVirtualKey**](/windows/desktop/api/Imm/nf-imm-immgetvirtualkey)                       | Recupera il valore della chiave virtuale originale associato a un messaggio di input della chiave già elaborato dall'IME.           |
| [**ImmInstallIME**](/windows/desktop/api/Imm/nf-imm-imminstallimea)                             | Installa un IME.                                                                                                           |
| [**ImmIsIME**](/windows/desktop/api/Imm/nf-imm-immisime)                                       | Determina se le impostazioni locali di input specificate hanno un IME.                                                                       |
| [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)                           | Verifica la presenza di messaggi destinati alla finestra IME e li invia alla finestra specificata.                          |
| [**ImmNotifyIME**](/windows/desktop/api/Imm/nf-imm-immnotifyime)                               | Notifica all'IME le modifiche apportate allo stato del contesto di input.                                                         |
| [**ImmRegisterWord**](/windows/desktop/api/Imm/nf-imm-immregisterworda)                         | Registra una stringa con il dizionario dell'IME associato alle impostazioni locali di input specificate.                              |
| [**ImmReleaseContext**](/windows/desktop/api/Imm/nf-imm-immreleasecontext)                     | Rilascia il contesto di input e sblocca la memoria associata al contesto di input.                                         |
| [**ImmRequestMessage**](/windows/desktop/api/Immdev/nf-immdev-immrequestmessagea)                     | Richiede un messaggio dall'applicazione.                                                                                   |
| [**ImmSetCandidateWindow**](/windows/desktop/api/Imm/nf-imm-immsetcandidatewindow)             | Imposta informazioni sulla finestra dei candidati.                                                                              |
| [**ImmSetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immsetcompositionfonta)             | Imposta il tipo di carattere logico da utilizzare per visualizzare i caratteri nella finestra di composizione.                                              |
| [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa)         | Imposta i caratteri, gli attributi e le clausole delle stringhe di composizione e di lettura.                                       |
| [**ImmSetCompositionWindow**](/windows/desktop/api/Imm/nf-imm-immsetcompositionwindow)         | Imposta la posizione della finestra di composizione.                                                                               |
| [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus)           | Imposta lo stato di conversione corrente.                                                                                        |
| [**ImmSetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immsetopenstatus)                       | Apre o chiude l'IME.                                                                                                   |
| [**ImmSetStatusWindowPos**](/windows/desktop/api/Imm/nf-imm-immsetstatuswindowpos)             | Imposta la posizione della finestra di stato.                                                                                    |
| [**ImmSimulateHotKey**](/windows/desktop/api/Imm/nf-imm-immsimulatehotkey)                     | Simula il tasto di scelta rapida IME specificato, causando la stessa risposta come se l'utente preme il tasto di scelta rapida nella finestra specificata. |
| [**ImmUnregisterWord**](/windows/desktop/api/Imm/nf-imm-immunregisterworda)                     | Rimuove una stringa di registro dal dizionario dell'IME associato alle impostazioni locali di input specificate.                       |



 

 

 



