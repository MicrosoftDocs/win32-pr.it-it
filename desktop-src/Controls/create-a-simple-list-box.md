---
title: Come creare una casella di riepilogo semplice
description: In questo argomento viene illustrato come inizializzare e recuperare elementi da una casella di riepilogo semplice.
ms.assetid: 4A717010-A1D3-4FFB-8E4E-D5C4F9D8D952
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a037bfbdb5232cd30d3e13fbc251c22c18c71a76398a351939602301a745d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063176"
---
# <a name="how-to-create-a-simple-list-box"></a>Come creare una casella di riepilogo semplice

In questo argomento viene illustrato come inizializzare e recuperare elementi da una casella di riepilogo semplice.

L'esempio di codice C++ in questo argomento include una procedura di finestra di dialogo che compila una casella di riepilogo con informazioni sui giocatori di una squadra di sport. Quando l'utente seleziona il nome di un giocatore dall'elenco, le informazioni sul giocatore vengono visualizzate nella finestra di dialogo. Lo stile della finestra per la casella di riepilogo include [**LBS \_ SORT,**](list-box-styles.md)che determina un elenco ordinato di elementi. Lo screenshot seguente mostra la finestra di dialogo.

![Screenshot di una finestra di dialogo contenente una casella di riepilogo con etichetta, il testo sull'elemento della casella di riepilogo selezionato e un pulsante OK](images/lb-roster.png)

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni


L'applicazione deve eseguire le attività correlate alla casella di riepilogo seguenti:

-   Inizializzare la casella di riepilogo
-   Recuperare la selezione dell'utente dalla casella di riepilogo

Nell'esempio di codice C++ seguente le informazioni sui lettori vengono archiviate in una matrice di strutture . Durante l'inizializzazione, la procedura della finestra di dialogo usa il messaggio [**\_ ADDSTRING LB**](lb-addstring.md) per aggiungere i nomi dei membri del team alla casella di riepilogo (**IDC \_ LISTBOX \_ EXAMPLE**) uno alla volta. Usa anche il messaggio [**\_ LB SETITEMDATA**](lb-setitemdata.md) per aggiungere l'indice della matrice del lettore alla casella di riepilogo come dati dell'elemento. Successivamente, quando l'utente seleziona un lettore dalla casella di riepilogo, la procedura della finestra di dialogo usa il messaggio [**\_ LB GETITEMDATA**](lb-getitemdata.md) per recuperare l'indice di matrice corrispondente. Usa quindi l'indice della matrice per recuperare le informazioni sul giocatore dalla matrice.



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

[Informazioni di riferimento sul controllo Casella di riepilogo](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[Informazioni sulle caselle di riepilogo](about-list-boxes.md)
</dt> <dt>

[Uso delle caselle di riepilogo](using-list-boxes.md)
</dt> </dl>

 

 




