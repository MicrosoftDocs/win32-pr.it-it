---
title: Dichiarazione di classe CGuiPaper
description: Dichiarazione di classe CGuiPaper
ms.assetid: b772d056-bf89-46a8-9462-21772cf96dfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d684618eea78247b94ed03223cfce45d2cc713f5507b1e290731d3451212b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663521"
---
# <a name="cguipaper-class-declaration"></a>Dichiarazione di classe CGuiPaper

Di seguito è riportata la dichiarazione della classe **CGuiPaper** da GUIPAPER.H.


```C++
class CGuiPaper
  {
    public:
      CGuiPaper(void);
      ~CGuiPaper(void);
      BOOL Init(HINSTANCE hInst, HWND hWnd, TCHAR* pszCmdLineFile);
      HRESULT DrawOn(void);
      HRESULT DrawOff(void);
      HRESULT ClearWin(void);
      HRESULT PaintWin(void);
      HRESULT Erase(void);
      HRESULT Resize(WORD wWidth, WORD wHeight);
      HRESULT InkWidth(SHORT nInkWidth);
      HRESULT InkColor(COLORREF crInkColor);
      HRESULT InkSaving(BOOL bInkSaving);
      HRESULT InkStart(SHORT nX, SHORT nY);
      HRESULT InkDraw(SHORT nX, SHORT nY);
      HRESULT InkStop(SHORT nX, SHORT nY);
      HRESULT ConnectPaperSink(void);
      HRESULT DisconnectPaperSink(void);
      HRESULT Load(void);
      HRESULT Save(void);
      int     AskSave(void);
      HRESULT Open(void);
      HRESULT SaveAs(void);
      COLORREF PickColor(void);

    private:
      HINSTANCE  m_hInst;
      HWND       m_hWnd;
      HDC        m_hDC;
      RECT       m_WinRect;
      IPaper*    m_pIPaper;
      SHORT      m_nLockKey;
      HPEN       m_hPen;
      SHORT      m_nInkWidth;
      COLORREF   m_crInkColor;
      BOOL       m_bInkSaving;
      BOOL       m_bInking;
      BOOL       m_bPainting;
      POINT      m_OldPos;
      IUnknown*  m_pCOPaperSink;
      DWORD      m_dwPaperSink;
      BOOL       m_bDirty;
      CPapFile*    m_pPapFile;
      OPENFILENAME m_ofnFile;
      TCHAR        m_szFileFilter[MAX_PATH];
      TCHAR        m_szFileName[MAX_PATH];
      TCHAR        m_szFileTitle[MAX_PATH];
      CHOOSECOLOR  m_ChooseColor;
      COLORREF     m_acrCustColors[16];

      IConnectionPoint* GetConnectionPoint(REFIID riid);
  };
```



**CGuiPaper** mantiene le proprietà gui correnti per la carta di disegno. I **membri m \_ crInkColor**, **m \_ crInkWidth** e **m \_ WinRect** contengono valori per il colore, la larghezza dell'input penna e il rettangolo di disegno correnti. Il **membro \_ m hWnd** archivia l'handle per la finestra in cui viene eseguito il disegno.

Il disegno effettivo delle immagini viene eseguito usando un handle per un contesto di dispositivo contenuto nel **membro m \_ hDC**. Un handle per la penna di disegno corrente viene mantenuto nel membro **m \_ hPen**. La penna viene distrutta e ricreata quando il colore o la larghezza viene modificata dall'utente.

I **membri m \_ pCOPaperSink** e **m \_ dwPaperSink** contengono i valori necessari per la connessione con COPaper per ricevere notifiche in ingresso tramite [**l'interfaccia IPaperSink.**](ipapersink-methods.md) Il **membro m \_ bDirty** contiene un flag che indica che l'utente ha modificato il disegno e che non riflette più i dati archiviati nel file.

Il **membro m \_ pIPaper** contiene il puntatore a interfaccia principale all'oggetto COPaper. Tutte le funzionalità COPaper sono accessibili tramite questo puntatore.

Il **membro m \_ nLockKey** viene usato per supportare uno schema di blocco client usato con più client per consentire a un client l'accesso esclusivo a un oggetto COPaper condiviso. COPaper assegna **m \_ nLockKey** durante una chiamata di blocco [**IPaper**](ipaper-methods.md)**::** e viene passato come parametro dal client nelle chiamate successive a COPaper. COPaper eseguirà il lavoro in queste chiamate solo se la chiave di blocco passata corrisponde all'ultima chiave consegnata a un client da COPaper.

Il **membro m \_ pPapFile** contiene un puntatore a un [**oggetto CPapFile.**](cpapfile-class-and-methods.md) Si tratta di un oggetto C++ che incapsula le operazioni di caricamento e salvataggio in un file composto di archiviazione strutturata. **CPapFile funziona** con l'oggetto COPaper basato su server sottostante per caricare e salvare i dati di disegno di COPaper.

 

 




