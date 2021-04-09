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
# <a name="how-to-create-a-simple-list-box"></a>Come creare una semplice casella di riepilogo

In questo argomento viene illustrato come inizializzare e recuperare elementi da una semplice casella di riepilogo.

L'esempio di codice C++ in questo argomento include una procedura della finestra di dialogo che compila una casella di riepilogo con informazioni sui giocatori di un team sportivo. Quando l'utente seleziona il nome di un lettore dall'elenco, le informazioni relative al lettore vengono visualizzate nella finestra di dialogo. Lo stile della finestra per la casella di riepilogo include l' [**\_ ordinamento di lbs**](list-box-styles.md), che consente di ottenere un elenco ordinato di elementi. La schermata seguente mostra la finestra di dialogo.

![Screenshot di una finestra di dialogo contenente una casella di riepilogo con etichetta, un testo sull'elemento casella di riepilogo selezionato e un pulsante OK](images/lb-roster.png)

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni


L'applicazione deve eseguire le seguenti attività correlate alla casella di riepilogo:

-   Inizializzare la casella di riepilogo
-   Recupera la selezione dell'utente dalla casella di riepilogo

Nell'esempio di codice C++ riportato di seguito, le informazioni sui giocatori sono archiviate in una matrice di strutture. Durante l'inizializzazione, la routine della finestra di dialogo usa il messaggio [**lb \_ ADDSTRING**](lb-addstring.md) per aggiungere i nomi dei membri del team alla casella di riepilogo (**\_ \_ esempio di ListBox di IDC**) uno alla volta. USA anche il messaggio [**lb \_ SETITEMDATA**](lb-setitemdata.md) per aggiungere l'indice della matrice del lettore alla casella di riepilogo come dati dell'elemento. In seguito, quando l'utente seleziona un lettore dalla casella di riepilogo, la routine della finestra di dialogo usa il messaggio [**lb \_ GETITEMDATA**](lb-getitemdata.md) per recuperare l'indice della matrice corrispondente. USA quindi l'indice della matrice per recuperare le informazioni sui giocatori dalla matrice.



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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al controllo casella di riepilogo](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[Informazioni sulle caselle di riepilogo](about-list-boxes.md)
</dt> <dt>

[Uso di caselle di riepilogo](using-list-boxes.md)
</dt> </dl>

 

 




