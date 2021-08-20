---
title: Metodi di CGuiPaper
description: I metodi di CGuiPaper sono riepilogati nel modo seguente. Questi metodi sono tutti implementati in GUIPAPER. CPP.
ms.assetid: 965a60d4-2737-4a2d-8790-bee70bceaeeb
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78f6d6fa04bba96d8cfb9e7ac23708560221f23b98437fa33f21245d28daf60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117962478"
---
# <a name="cguipaper-methods"></a>Metodi di CGuiPaper

I metodi di CGuiPaper sono riepilogati nel modo seguente. Questi metodi sono tutti implementati in GUIPAPER. CPP.



| Metodo                                                         | Descrizione                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| BOOL Init(HINSTANCE hInst, HWND hWnd, TCHAR \* pszCmdLineFile); | Inizializza l'oggetto GuiPaper. Chiede al server di creare un oggetto COPaper.                                                     |
| DrawOn(void) HRESULT;                                          | Blocca la carta per disegnare esclusivamente da questo client.                                                                   |
| DrawOff(void) HRESULT;                                         | Sblocca la carta per consentire ad altri client di disegnare.                                                                         |
| HRESULT ClearWin(void);                                        | Cancella la finestra di visualizzazione, ma mantiene i dati dell'input penna.                                                                           |
| HRESULT PaintWin(void);                                        | Cancella la finestra e ridisegna con i dati correnti dell'input penna.                                                                     |
| HRESULT Erase(void);                                           | Cancella il contenuto corrente del disegno e cancella la finestra di visualizzazione.                                                             |
| Ridimensionamento HRESULT(WORD wWidth, WORD wHeight);                     | Ridimensiona la finestra di visualizzazione.                                                                                           |
| HRESULT InkWidth(SHORT nInkWidth);                             | Imposta la larghezza corrente dell'input penna per il disegno.                                                                                   |
| HRESULT InkColor(COLORREF crInkColor);                         | Imposta il colore corrente dell'input penna per il disegno.                                                                                   |
| InkSaving HRESULT(BOOL bInkSaving);                            | Attiva e disattiva il salvataggio dei dati dell'input penna in COPaper.                                                                          |
| HRESULT InkStart(SHORT nX, SHORT nY);                          | Avvia la sequenza di disegno a penna.                                                                                          |
| HRESULT InkDraw(SHORT nX, SHORT nY);                           | Disegna i dati della sequenza di input penna.                                                                                              |
| HRESULT InkStop(SHORT nX, SHORT nY);                           | Arresta la sequenza di disegno a penna.                                                                                           |
| HRESULT ConnectPaperSink(void);                                | Connette l'oggetto PaperSink client all'origine COPaper del server.                                                    |
| HRESULT DisconnectPaperSink(void);                             | Disconnettere l'oggetto PaperSink client dall'origine COPaper del server.                                                |
| HRESULT Load(void);                                            | Carica i dati dell'input penna dal file composto corrente.                                                                            |
| HRESULT Save(void);                                            | Salva i dati dell'input penna esistenti nel file composto corrente.                                                                     |
| HRESULT AskSave(void);                                         | Verifica se il disegno è stato modificato. In tal caso, viene visualizzata una finestra di dialogo che chiede all'utente se salvare le modifiche e risponde in modo appropriato. |
| HRESULT Open(void);                                            | Visualizza la finestra di dialogo comune Win32. Apre un file composto di dati cartacei esistente.                                               |
| HRESULT SaveAs(void);                                          | Visualizza la finestra di dialogo comune Win32. Salva i dati cartacei correnti nel file rinominato.                                              |
| COLORREF PickColor(void);                                      | Visualizza la finestra di dialogo ommon Win32. Chiede all'utente di scegliere il nuovo colore della penna.                                                      |



 

Il **metodo Init** crea l'oggetto COPaper basato su server e assegna il membro \_ m pIPaper di CGuiPaper.

I **metodi AskSave**, **Open**, **SaveAs** e **PickColor** forniscono un comportamento dell'interfaccia utente grafica familiare usando le finestre di dialogo comuni Win32. Ad esempio, il **metodo Open** usa la finestra di dialogo Win32 Open File Name per chiedere all'utente di specificare un nome file per l'apertura.

I **metodi Load** e **Save** verranno descritti in dettaglio più avanti in questa presentazione.

**InkSaving,** **InkStart,** **InkDraw** e **InkStop** sono i metodi centrali per la funzionalità di disegno dell'applicazione **StoClien.** **StoClien usa** questi metodi CGuiPaper per acquisire, visualizzare e archiviare i dati di disegno interattivi nel modo in cui si verificano sotto il controllo utente. Svolgono un doppio ruolo di disegno dell'immagine disegnata nella finestra client e passano i dati di disegno a COPaper nel server. COPaper converte i dati di disegno in pacchetti di dati di input penna per l'archiviazione.

 

 




