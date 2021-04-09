---
title: Dichiarazione della classe CGuiPaper
description: Dichiarazione della classe CGuiPaper
ms.assetid: b772d056-bf89-46a8-9462-21772cf96dfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 269694b83804f3e85cd8654cd2a1be843396a2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044245"
---
# <a name="cguipaper-class-declaration"></a><span data-ttu-id="ff12e-103">Dichiarazione della classe CGuiPaper</span><span class="sxs-lookup"><span data-stu-id="ff12e-103">CGuiPaper Class Declaration</span></span>

<span data-ttu-id="ff12e-104">Di seguito è riportata la dichiarazione della classe **CGuiPaper** da GUIPAPER. H.</span><span class="sxs-lookup"><span data-stu-id="ff12e-104">The following is the **CGuiPaper** class declaration from GUIPAPER.H.</span></span>


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



<span data-ttu-id="ff12e-105">**CGuiPaper** gestisce le proprietà dell'interfaccia utente grafica corrente per il disegno.</span><span class="sxs-lookup"><span data-stu-id="ff12e-105">**CGuiPaper** maintains the current GUI properties for the drawing paper.</span></span> <span data-ttu-id="ff12e-106">I membri **m \_ crInkColor**, **m \_ crInkWidth** e **m \_ WinRect** contengono valori per il colore, la larghezza e il rettangolo di disegno correnti.</span><span class="sxs-lookup"><span data-stu-id="ff12e-106">Members **m\_crInkColor**, **m\_crInkWidth**, and **m\_WinRect** contain values for the current ink color, ink width, and drawing rectangle.</span></span> <span data-ttu-id="ff12e-107">Il **membro \_ HWND m** archivia l'handle per la finestra in cui viene eseguito il disegno.</span><span class="sxs-lookup"><span data-stu-id="ff12e-107">The **m\_hWnd** member stores the handle to the window where painting is done.</span></span>

<span data-ttu-id="ff12e-108">Il disegno effettivo delle immagini viene eseguito usando un handle per un contesto di dispositivo contenuto nel membro **m \_ HDC**.</span><span class="sxs-lookup"><span data-stu-id="ff12e-108">The actual painting of images is done using a handle to a device context held in member **m\_hDC**.</span></span> <span data-ttu-id="ff12e-109">Un handle per la penna di disegno corrente viene mantenuto nel membro **m \_ hPen**.</span><span class="sxs-lookup"><span data-stu-id="ff12e-109">A handle to the current drawing pen is kept in member **m\_hPen**.</span></span> <span data-ttu-id="ff12e-110">La penna viene distrutta e ricreata quando il colore o la larghezza viene modificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="ff12e-110">The pen is destroyed and recreated when its color or width is changed by the user.</span></span>

<span data-ttu-id="ff12e-111">I membri **m \_ pCOPaperSink** e **m \_ dwPaperSink** contengono i valori necessari per la connessione a un documento per ricevere le notifiche in ingresso tramite l'interfaccia [**IPaperSink**](ipapersink-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="ff12e-111">Members **m\_pCOPaperSink** and **m\_dwPaperSink** hold values necessary for connecting with COPaper to receive incoming notifications through the [**IPaperSink**](ipapersink-methods.md) interface.</span></span> <span data-ttu-id="ff12e-112">Member **m \_ bDirty** contiene un flag che indica che l'utente ha modificato il disegno e che non riflette più i dati archiviati nel file.</span><span class="sxs-lookup"><span data-stu-id="ff12e-112">Member **m\_bDirty** holds a flag indicating that the user has changed the drawing and that it no longer reflects the data stored in its file.</span></span>

<span data-ttu-id="ff12e-113">Il membro **m \_ pIPaper** include il puntatore di interfaccia principale all'oggetto Copaper.</span><span class="sxs-lookup"><span data-stu-id="ff12e-113">Member **m\_pIPaper** holds the main interface pointer to the COPaper object.</span></span> <span data-ttu-id="ff12e-114">È possibile accedere a tutte le funzionalità della cocarta tramite questo puntatore.</span><span class="sxs-lookup"><span data-stu-id="ff12e-114">All of the COPaper functionality is accessed through this pointer.</span></span>

<span data-ttu-id="ff12e-115">Il **membro \_ nLockKey m** viene usato per supportare uno schema di blocco client usato con più client per consentire a un client di accedere in modo esclusivo a un oggetto Copaper condiviso.</span><span class="sxs-lookup"><span data-stu-id="ff12e-115">The **m\_nLockKey** member is used to support a client locking scheme that is used with multiple clients to allow a client exclusive access to a shared COPaper object.</span></span> <span data-ttu-id="ff12e-116">Il Copaper assegna **m \_ nLockKey** durante una chiamata [**iPaper**](ipaper-methods.md)::**Lock** e viene passato come parametro dal client nelle chiamate successive a Copaper.</span><span class="sxs-lookup"><span data-stu-id="ff12e-116">COPaper assigns **m\_nLockKey** during an [**IPaper**](ipaper-methods.md)::**Lock** call and is passed as a parameter by the client in subsequent calls to COPaper.</span></span> <span data-ttu-id="ff12e-117">Il Copaper eseguirà il lavoro in queste chiamate solo se la chiave di blocco che viene passata corrisponde alla chiave passata a un client da un documento.</span><span class="sxs-lookup"><span data-stu-id="ff12e-117">COPaper will perform the work in those calls only if the lock key that is passed matches the key last handed out to a client by COPaper.</span></span>

<span data-ttu-id="ff12e-118">Il membro **m \_ pPapFile** include un puntatore a un oggetto [**CPapFile**](cpapfile-class-and-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="ff12e-118">Member **m\_pPapFile** holds a pointer to a [**CPapFile**](cpapfile-class-and-methods.md) object.</span></span> <span data-ttu-id="ff12e-119">Si tratta di un oggetto C++ che incapsula le operazioni di caricamento e salvataggio in un file composto di archiviazione strutturata.</span><span class="sxs-lookup"><span data-stu-id="ff12e-119">It is a C++ object that encapsulates load and save operations on a structured storage compound file.</span></span> <span data-ttu-id="ff12e-120">**CPapFile** funziona con l'oggetto Copaper basato su server sottostante per caricare e salvare i dati di disegno del documento.</span><span class="sxs-lookup"><span data-stu-id="ff12e-120">**CPapFile** works with the underlying server-based COPaper object to load and save the COPaper drawing data.</span></span>

 

 




