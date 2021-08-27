---
title: Come usare i controlli List-View virtuali
description: Questo argomento illustra come usare i controlli di visualizzazione elenco virtuali.
ms.assetid: DA32D7B3-5FDB-4D73-9A72-0D4EEB2A0C4F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6ed847d7cb8a41e4cb1c255290ff660eb278bcd99126605a2874c52b279e694
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059701"
---
# <a name="how-to-use-virtual-list-view-controls"></a>Come usare i controlli List-View virtuali

Questo argomento illustra come usare i controlli di visualizzazione elenco virtuali. Gli esempi di codice C++ che seguono illustrano come elaborare i messaggi di notifica del controllo visualizzazione elenco virtuale, come ottimizzare la cache e come recuperare un elemento dalla cache.

-   [Informazioni importanti](#what-you-need-to-know)
-   [Elaborare codici di notifica di List-View virtuali](#process-virtual-list-view-control-notification-codes)
-   [Ottimizzare la cache](#optimize-the-cache)
-   [Recuperare un elemento dalla cache](#retrieve-an-item-from-the-cache)
-   [Argomenti correlati](#related-topics)

> [!Note]  
> Il codice di esempio in questa sezione presuppone che la cache sia una matrice allocata dinamicamente di strutture definite dall'applicazione. La struttura è definita nell'esempio di codice C++ seguente.

 


```C++
struct RndItem
{
    int   iIcon;                 // Bitmap assigned to this item.
    UINT  state;                 // Item state value.
    TCHAR Title[BUFFER_SIZE];    // BUFFER_SIZE is a user-defined macro value.
    TCHAR SubText1[BUFFER_SIZE]; // Text for the label of the first sub-item.
    TCHAR SubText2[BUFFER_SIZE]; // Text for the label of the second item.
};

```



## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="process-virtual-list-view-control-notification-codes"></a>Elaborare codici di notifica di List-View virtuali

Oltre ai codici di notifica inviati da altri controlli visualizzazione elenco, i controlli visualizzazione elenco virtuale possono anche inviare i codici di notifica [ \_ ODCACHEHINT](lvn-odcachehint.md) e [**LVN \_ ODFINDITEM.**](lvn-odfinditem.md)

Questa funzione definita dall'applicazione gestisce i messaggi di notifica comunemente inviati da un controllo visualizzazione elenco virtuale.


```C++
LRESULT OnNotify(HWND hwnd, NMHDR* pnmhdr)
{
    HRESULT hr;
    LRESULT lrt = FALSE;

    switch (pnmhdr->code)
    {
    case LVN_GETDISPINFO:
        {
            RndItem rndItem;
            NMLVDISPINFO* plvdi = (NMLVDISPINFO*) pnmhdr;

            if (-1 == plvdi->item.iItem)
            {
                OutputDebugString(TEXT("LVOWNER: Request for -1 item?\n"));
                DebugBreak();
            }

            // Retrieve information for item at index iItem.
            RetrieveItem( &rndItem, plvdi->item.iItem );

            if(plvdi->item.mask & LVIF_STATE)
            {
                // Fill in the state information.
                plvdi->item.state |= rndItem.state;
            }

            if(plvdi->item.mask & LVIF_IMAGE)
            {
                // Fill in the image information.
                plvdi->item.iImage = rndItem.iIcon;
            }

            if(plvdi->item.mask & LVIF_TEXT)
            {
                // Fill in the text information.
                switch (plvdi->item.iSubItem)
                {
                case 0:
                    // Copy the main item text.
                    hr = StringCchCopy(plvdi->item.pszText, MAX_COUNT, rndItem.Title);

                    if(FAILED(hr))
                    { 
                        // Insert error handling code here. MAX_COUNT
                        // is a user-defined value. You must not enter                                
                        // more characters than specified by MAX_COUNT or  
                        // the text will be truncated.
                    }
                    break;

                case 1:
                    // Copy SubItem1 text.
                    hr = StringCchCopy( plvdi->item.pszText, MAX_COUNT, rndItem.SubText1);

                    if(FAILED(hr))
                    {
                        // Insert error handling code here. MAX_COUNT
                        // is a user-defined value. You must not enter               
                        // more characters than specified by MAX_COUNT or   
                        // the text will be truncated..
                    }
                    break;

                case 2:
                    // Copy SubItem2 text.
                    hr = StringCchCopy(plvdi->item.pszText, MAX_COUNT, rndItem.SubText2);

                    if(FAILED(hr))
                    {
                        // Insert error handling code here. MAX_COUNT
                        // is a user-defined value. You must not enter                    
                        // more characters than specified by MAX_COUNT or  
                        // the text will be truncated..
                    }
                    break;

                default:
                    break;

                }

            }

            lrt = FALSE;
            break;
        }

    case LVN_ODCACHEHINT:
        {
            NMLVCACHEHINT* pcachehint = (NMLVCACHEHINT*) pnmhdr;

            // Load the cache with the recommended range.
            PrepCache( pcachehint->iFrom, pcachehint->iTo );
            break;
        }

    case LVN_ODFINDITEM:
        {
            LPNMLVFINDITEM pnmfi = NULL;
            
            pnmfi = (LPNMLVFINDITEM)pnmhdr;

            // Call a user-defined function that finds the index according to
            // LVFINDINFO (which is embedded in the LPNMLVFINDITEM structure).
            // If nothing is found, then set the return value to -1.

            break;
        }

    default:
        break;

    }       // End Switch block.

    return(lrt);
}
```



### <a name="optimize-the-cache"></a>Ottimizzare la cache

Un controllo visualizzazione elenco virtuale invia un messaggio di notifica [ \_ ODCACHEHINT LVN](lvn-odcachehint.md) quando il contenuto della relativa area di visualizzazione è stato modificato. Il messaggio contiene informazioni sull'intervallo di elementi da memorizzare nella cache. Quando si riceve il messaggio di notifica, l'applicazione deve essere pronta a caricare la cache con le informazioni sull'elemento per l'intervallo richiesto in modo che le informazioni siano immediatamente disponibili quando viene inviato un messaggio di notifica [ \_ LVN GETDISPINFO.](lvn-getdispinfo.md)

Nell'esempio di codice C++ seguente la funzione definita dall'applicazione accetta l'intervallo di elementi per la cache inviato da un controllo visualizzazione elenco virtuale. Esegue una verifica per determinare che l'intervallo di elementi richiesto non è già memorizzato nella cache e quindi alloca la memoria globale necessaria e riempie la cache, se necessario.


```C++
void PrepCache(int iFrom, int iTo)
{
    /*  Global Variables

     *  g_priCache[ ]: the main cache.
     *  g_iCache:      the index of the first item in the main cache.
     *  g_cCache:      the count of items in the main cache.
     *
     *  g_priEndCache[ ]: the cache of items at the end of the list.
     *  g_iEndCache:      the index of the first item in the end cache.
     *  g_cEndCache:      the count of items in the end cache.
     */
     
    // Local Variables
    int i;
    BOOL fOLFrom = FALSE;
    BOOL   fOLTo = FALSE;

    // Check to see if this is the end cache.
    if ((iTo == g_cCache - 1) && ((iTo - iFrom) < 30))  // 30 entries wide.
    {
        // Check to see if this is a portion of the current end cache.
        if ((g_cCache) && (iFrom >= g_iEndCache) && (iFrom < g_iEndCache+g_cEndCache))
            return;
            // If it is a part of current end cache, no loading is necessary.

        // This is a new end cache. Free the old memory.
        if ( g_priEndCache )
            GlobalFree( g_priEndCache );
            
        // Set the index and count values for the new end cache,
        // and then retrieve the memory.
        g_iEndCache   = iFrom;
        g_cEndCache   = (iTo - iFrom + 1);
        g_priEndCache = (RndItem *)GlobalAlloc(GPTR, sizeof(RndItem) * g_cEndCache);

        if (! g_priEndCache)
        {
            // TODO: Out of memory. Perform error handling.
        }

        // Loop to fill the cache with the recommended items.
        for (i=0; i<g_cEndCache; i++)
        {
            // TODO: Call a function that accesses item information and
            // fills a cache element.
        }
    }

    else
    {   
        // It is not a member of the current end cache.
        // Try the primary cache instead.

        // Check to see if iFrom is within the primary cache.
        if ((g_cCache) && (iFrom >= g_iCache) && (iFrom < g_iCache+g_cCache))
            fOLFrom = TRUE;

        // Check to see if iTo is within the primary cache.
        if ((g_cCache) && (iTo >= g_iCache) && (iTo <= g_iCache+g_cCache))
            fOLTo = TRUE;

        // do nothing if both iFrom and iTo are within the current cache.

        if (fOLFrom && fOLTo)
            return;

        // Enlarge the cache size rather than make it specific to this hint.
        if (fOLFrom)
            iFrom = g_iCache;

        else if (fOLTo)
            iTo = g_iCache + g_cCache;

        // A new primary cache is needed. Free the old primary cache.
        if ( g_priCache )
            GlobalFree( g_priCache );

        // Set the index and count values for the new primary cache,
        // and then retrieve the memory.
        g_iCache   = iFrom;
        g_cCache   = (iTo - iFrom + 1);
        g_priCache = (RndItem *)GlobalAlloc( GPTR, sizeof( RndItem ) * g_cCache );

        if (!g_priCache)
        {
            // TODO: Out of memory. Do error handling.
        }

        // Loop to fill the cache with the recommended items.
        for (i=0; i<g_cCache; i++)
        {
            // TODO: Call a function that accesses item information
            // and fills a cache element.
        }
    }
}
```



### <a name="retrieve-an-item-from-the-cache"></a>Recuperare un elemento dalla cache

Questa funzione di esempio accetta due parametri, l'indirizzo della struttura definita dall'applicazione e un valore intero che rappresenta l'indice dell'elemento nell'elenco. Controlla il valore dell'indice per individuare se l'elemento desiderato viene memorizzato nella cache. In caso contrario, il puntatore passato alla funzione viene impostato su una posizione nella cache. Se l'elemento non si trova nella cache principale o finale, le informazioni sull'elemento devono essere posizionate manualmente.


```C++
void RetrieveItem( RndItem * prndItem, int index )
{
    // Global Variables

    // g_priCache[ ]: the main cache.
    // g_iCache:      the index of the first item in the main cache.
    // c_cCache:      the count of items in the main cache.
    //
    // g_priEndCache[ ]:  the cache of items at the end of the list.
    // g_iEndCache:       the index of the first item in the end cache.
    // g_cEndCache:       the count of items in the end cache.
    //

    // Check to see if the item is in the main cache.
    if ((index >= g_iCache) && (index < g_iCache + g_cCache))
        *prndItem = g_priCache[index-g_iCache];

    // If it is not in the main cache, then check to see if
    // the item is in the end area cache.
    else if ((index >= g_iEndCache) && (index < g_iEndCache + g_cEndCache))
        *prndItem = g_priEndCache[index-g_iEndCache];

    else
    {
        // The item is not in either cache.
        // Therefore, retrieve the item information manually.
    }
}
```



## <a name="remarks"></a>Commenti

Per un elenco dei messaggi della finestra elaborati da un controllo di visualizzazione elenco, vedere [Default List-View Message Processing](listview-message-processing.md).

## <a name="complete-example"></a>Esempio completo

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sul controllo List-View](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Informazioni List-View controllo](list-view-controls-overview.md)
</dt> <dt>

[Uso dei List-View personalizzati](using-list-view-controls.md)
</dt> </dl>

 

 




