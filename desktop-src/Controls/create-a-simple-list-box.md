---
title: Come creare una semplice casella di riepilogo
description: In questo argomento viene illustrato come inizializzare e recuperare elementi da una semplice casella di riepilogo.
ms.assetid: 4A717010-A1D3-4FFB-8E4E-D5C4F9D8D952
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca2230b265d61e9a59a8892e14127d25bf2cfd2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104047605"
---
# <a name="how-to-create-a-simple-list-box"></a><span data-ttu-id="7e094-103">Come creare una semplice casella di riepilogo</span><span class="sxs-lookup"><span data-stu-id="7e094-103">How to Create a Simple List Box</span></span>

<span data-ttu-id="7e094-104">In questo argomento viene illustrato come inizializzare e recuperare elementi da una semplice casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="7e094-104">This topic demonstrates how to initialize and retrieve items from a simple list box.</span></span>

<span data-ttu-id="7e094-105">L'esempio di codice C++ in questo argomento include una procedura della finestra di dialogo che compila una casella di riepilogo con informazioni sui giocatori di un team sportivo.</span><span class="sxs-lookup"><span data-stu-id="7e094-105">The C++ code example in this topic includes a dialog box procedure that fills a list box with information about players on a sports team.</span></span> <span data-ttu-id="7e094-106">Quando l'utente seleziona il nome di un lettore dall'elenco, le informazioni relative al lettore vengono visualizzate nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="7e094-106">When the user selects the name of a player from the list, information about the player is displayed in the dialog box.</span></span> <span data-ttu-id="7e094-107">Lo stile della finestra per la casella di riepilogo include l' [**\_ ordinamento di lbs**](list-box-styles.md), che consente di ottenere un elenco ordinato di elementi.</span><span class="sxs-lookup"><span data-stu-id="7e094-107">The window style for the list box includes [**LBS\_SORT**](list-box-styles.md), which results in a sorted list of items.</span></span> <span data-ttu-id="7e094-108">La schermata seguente mostra la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="7e094-108">The following screen shot shows the dialog box.</span></span>

![Screenshot di una finestra di dialogo contenente una casella di riepilogo con etichetta, un testo sull'elemento casella di riepilogo selezionato e un pulsante OK](images/lb-roster.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="7e094-110">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="7e094-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7e094-111">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="7e094-111">Technologies</span></span>

-   [<span data-ttu-id="7e094-112">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="7e094-112">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="7e094-113">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="7e094-113">Prerequisites</span></span>

-   <span data-ttu-id="7e094-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="7e094-114">C/C++</span></span>
-   <span data-ttu-id="7e094-115">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="7e094-115">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="7e094-116">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="7e094-116">Instructions</span></span>


<span data-ttu-id="7e094-117">L'applicazione deve eseguire le seguenti attività correlate alla casella di riepilogo:</span><span class="sxs-lookup"><span data-stu-id="7e094-117">The application must perform the following list box–related tasks:</span></span>

-   <span data-ttu-id="7e094-118">Inizializzare la casella di riepilogo</span><span class="sxs-lookup"><span data-stu-id="7e094-118">Initialize the list box</span></span>
-   <span data-ttu-id="7e094-119">Recupera la selezione dell'utente dalla casella di riepilogo</span><span class="sxs-lookup"><span data-stu-id="7e094-119">Retrieve the user's selection from the list box</span></span>

<span data-ttu-id="7e094-120">Nell'esempio di codice C++ riportato di seguito, le informazioni sui giocatori sono archiviate in una matrice di strutture.</span><span class="sxs-lookup"><span data-stu-id="7e094-120">In the following C++ code example, information about players is stored in an array of structures.</span></span> <span data-ttu-id="7e094-121">Durante l'inizializzazione, la routine della finestra di dialogo usa il messaggio [**lb \_ ADDSTRING**](lb-addstring.md) per aggiungere i nomi dei membri del team alla casella di riepilogo (**\_ \_ esempio di ListBox di IDC**) uno alla volta.</span><span class="sxs-lookup"><span data-stu-id="7e094-121">During initialization, the dialog box procedure uses the [**LB\_ADDSTRING**](lb-addstring.md) message to add the names of team members to the list box (**IDC\_LISTBOX\_EXAMPLE**) one at a time.</span></span> <span data-ttu-id="7e094-122">USA anche il messaggio [**lb \_ SETITEMDATA**](lb-setitemdata.md) per aggiungere l'indice della matrice del lettore alla casella di riepilogo come dati dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="7e094-122">It also uses the [**LB\_SETITEMDATA**](lb-setitemdata.md) message to add the array index of the player to the list box as item data.</span></span> <span data-ttu-id="7e094-123">In seguito, quando l'utente seleziona un lettore dalla casella di riepilogo, la routine della finestra di dialogo usa il messaggio [**lb \_ GETITEMDATA**](lb-getitemdata.md) per recuperare l'indice della matrice corrispondente.</span><span class="sxs-lookup"><span data-stu-id="7e094-123">Later, when the user selects a player from the list box, the dialog box procedure uses the [**LB\_GETITEMDATA**](lb-getitemdata.md) message to retrieve the corresponding array index.</span></span> <span data-ttu-id="7e094-124">USA quindi l'indice della matrice per recuperare le informazioni sui giocatori dalla matrice.</span><span class="sxs-lookup"><span data-stu-id="7e094-124">It then uses the array index to retrieve player information from the array.</span></span>



```C++
typedef struct 
{ 
    TCHAR achName[MAX_PATH]; 
    TCHAR achPosition[12]; 
    int nGamesPlayed; 
    int nGoalsScored; 
} Player; 

Player Roster[] = 
{ 
    {TEXT("Haas, Jonathan"), TEXT("Midfield"), 18, 4 }, 
    {TEXT("Pai, Jyothi"), TEXT("Forward"), 36, 12 }, 
    {TEXT("Hanif, Kerim"), TEXT("Back"), 26, 0 }, 
    {TEXT("Anderberg, Michael"), TEXT("Back"), 24, 2 }, 
    {TEXT("Jelitto, Jacek"), TEXT("Midfield"), 26, 3 }, 
    {TEXT("Raposo, Rui"), TEXT("Back"), 24, 3}, 
    {TEXT("Joseph, Brad"), TEXT("Forward"), 13, 3 }, 
    {TEXT("Bouchard, Thomas"), TEXT("Forward"), 28, 5 }, 
    {TEXT("Salmre, Ivo "), TEXT("Midfield"), 27, 7 }, 
    {TEXT("Camp, David"), TEXT("Midfield"), 22, 3 }, 
    {TEXT("Kohl, Franz"), TEXT("Goalkeeper"), 17, 0 }, 
}; 


INT_PTR CALLBACK ListBoxExampleProc(HWND hDlg, UINT message, 
        WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
    case WM_INITDIALOG:
        {
            // Add items to list. 
            HWND hwndList = GetDlgItem(hDlg, IDC_LISTBOX_EXAMPLE);  
            for (int i = 0; i < ARRAYSIZE(Roster); i++) 
            { 
                int pos = (int)SendMessage(hwndList, LB_ADDSTRING, 0, 
                    (LPARAM) Roster[i].achName); 
                // Set the array index of the player as item data.
                // This enables us to retrieve the item from the array
                // even after the items are sorted by the list box.
                SendMessage(hwndList, LB_SETITEMDATA, pos, (LPARAM) i); 
            } 
            // Set input focus to the list box.
            SetFocus(hwndList); 
            return TRUE;               
        } 

    case WM_COMMAND:
        switch (LOWORD(wParam))
        {
        case IDOK:
        case IDCANCEL:
            EndDialog(hDlg, LOWORD(wParam));
            return TRUE;

        case IDC_LISTBOX_EXAMPLE:
            {
                switch (HIWORD(wParam)) 
                { 
                case LBN_SELCHANGE:
                    {
                        HWND hwndList = GetDlgItem(hDlg, IDC_LISTBOX_EXAMPLE); 

                        // Get selected index.
                        int lbItem = (int)SendMessage(hwndList, LB_GETCURSEL, 0, 0); 

                        // Get item data.
                        int i = (int)SendMessage(hwndList, LB_GETITEMDATA, lbItem, 0);

                        // Do something with the data from Roster[i]
                        TCHAR buff[MAX_PATH];
                        StringCbPrintf (buff, ARRAYSIZE(buff),  
                            TEXT("Position: %s\nGames played: %d\nGoals: %d"), 
                            Roster[i].achPosition, Roster[i].nGamesPlayed, 
                            Roster[i].nGoalsScored);

                        SetDlgItemText(hDlg, IDC_STATISTICS, buff); 
                        return TRUE; 
                    } 
                }
            }
            return TRUE;
        }
    }
    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="7e094-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7e094-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e094-126">Riferimento al controllo casella di riepilogo</span><span class="sxs-lookup"><span data-stu-id="7e094-126">List Box Control Reference</span></span>](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[<span data-ttu-id="7e094-127">Informazioni sulle caselle di riepilogo</span><span class="sxs-lookup"><span data-stu-id="7e094-127">About List Boxes</span></span>](about-list-boxes.md)
</dt> <dt>

[<span data-ttu-id="7e094-128">Uso di caselle di riepilogo</span><span class="sxs-lookup"><span data-stu-id="7e094-128">Using List Boxes</span></span>](using-list-boxes.md)
</dt> </dl>

 

 




