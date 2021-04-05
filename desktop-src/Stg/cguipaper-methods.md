---
title: Metodi CGuiPaper
description: I metodi di CGuiPaper sono riepilogati come indicato di seguito. Questi metodi sono tutti implementati in GUIPAPER. CPP.
ms.assetid: 965a60d4-2737-4a2d-8790-bee70bceaeeb
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1303ca38ffe02da0dc747e1a8834d36419452209
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708206"
---
# <a name="cguipaper-methods"></a>Metodi CGuiPaper

I metodi di CGuiPaper sono riepilogati come indicato di seguito. Questi metodi sono tutti implementati in GUIPAPER. CPP.



| Metodo                                                         | Descrizione                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| BOOL init (HINSTANCE hInst, HWND hWnd, TCHAR \* pszCmdLineFile); | Inizializza GuiPaper. Chiede al server di creare un oggetto Copaper.                                                     |
| HRESULT DrawOn (void);                                          | Blocca la carta per il disegno esclusivo del client.                                                                   |
| HRESULT DrawOff (void);                                         | Sblocca la carta per consentire l'estrazione di altri client.                                                                         |
| HRESULT ClearWin (void);                                        | Cancella la finestra di visualizzazione, ma conserva i dati dell'input penna.                                                                           |
| HRESULT PaintWin (void);                                        | Cancella la finestra e i ridisegni con i dati di input penna correnti.                                                                     |
| HRESULT Erase (void);                                           | Cancella il contenuto del disegno corrente e cancella la finestra di visualizzazione.                                                             |
| HRESULT Resize (WORD wWidth, WORD peso);                     | Ridimensiona la finestra di visualizzazione.                                                                                           |
| HRESULT InkWidth (SHORT nInkWidth);                             | Imposta la larghezza dell'input penna corrente per il disegno.                                                                                   |
| HRESULT InkColor (COLORREF crInkColor);                         | Imposta il colore dell'input penna corrente per il disegno.                                                                                   |
| HRESULT InkSaving (BOOL bInkSaving);                            | Attiva e disattiva il salvataggio dei dati di input penna in un documento.                                                                          |
| HRESULT InkStart (SHORT nX, SHORT nY);                          | Avvia la sequenza di disegno dell'input penna.                                                                                          |
| HRESULT InkDraw (SHORT nX, SHORT nY);                           | Disegna i dati della sequenza di input penna.                                                                                              |
| HRESULT InkStop (SHORT nX, SHORT nY);                           | Arresta la sequenza di disegno dell'input penna.                                                                                           |
| HRESULT ConnectPaperSink (void);                                | Connette l'oggetto PaperSink del client all'origine del documento del server.                                                    |
| HRESULT DisconnectPaperSink (void);                             | Disconnettere l'oggetto PaperSink del client dall'origine del documento del server.                                                |
| Carico HRESULT (void);                                            | Carica i dati dell'input penna dal file composto corrente.                                                                            |
| HRESULT Save (void);                                            | Salva i dati Ink esistenti nel file composto corrente.                                                                     |
| HRESULT AskSave (void);                                         | Controlla se il disegno è stato modificato. In tal caso, viene visualizzata la finestra di dialogo in cui viene chiesto all'utente se salvare le modifiche e rispondere in modo appropriato. |
| HRESULT aperto (void);                                            | Mostra la finestra di dialogo comune Win32. Apre un file composto di dati cartacei esistente.                                               |
| SaveAs di HRESULT (void);                                          | Mostra la finestra di dialogo comune Win32. Salva i dati cartacei correnti in un file rinominato.                                              |
| COLORREF PickColor (void);                                      | Mostra la finestra di dialogo Pratolina Win32. Chiede all'utente di scegliere il nuovo colore della penna.                                                      |



 

Il metodo **init** crea l'oggetto Copaper basato su server e assegna il \_ membro pIPaper di CGuiPaper.

I metodi **AskSave**, **Open**, **SaveAs** e **PickColor** forniscono un comportamento familiare dell'interfaccia utente grafica usando le finestre di dialogo comuni di Win32. Ad esempio, il metodo **Open** usa la finestra di dialogo Apri nome file Win32 per chiedere all'utente di specificare un nome di file per l'apertura.

I metodi **Load** e **Save** verranno descritti in dettaglio più avanti in questa presentazione.

**InkSaving**, **InkStart**, **InkDraw** e **InkStop** sono i metodi centrali per la funzionalità di disegno dell'applicazione **StoClien** . **StoClien** utilizza questi metodi CGuiPaper per acquisire, visualizzare e archiviare i dati di disegno interattivo come avviene nel controllo utente. Eseguono un doppio ruolo di disegnare l'immagine disegnata nella finestra del client, nonché di passare i dati di disegno a un documento nel server. Il documento converte i dati di disegno in pacchetti di dati di input penna per l'archiviazione.

 

 




