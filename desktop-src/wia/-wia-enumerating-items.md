---
description: Quando viene creato un dispositivo, Windows Image Acquisition (WIA) crea un albero gerarchico di elementi WIA che rappresentano il dispositivo e le cartelle e le immagini associate a tale dispositivo.
ms.assetid: ab7246e8-47bb-4b94-8d91-1c22010ebd9f
title: Enumerazione di elementi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5438e5cb65b701fcbc24d61aa888ac6c88347cacdaca8fa0a861f8c452a1ebc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772881"
---
# <a name="enumerating-items"></a>Enumerazione di elementi

Quando viene creato un dispositivo, Windows Image Acquisition (WIA) crea un albero gerarchico di elementi WIA che rappresentano il dispositivo e le cartelle e le immagini associate a tale dispositivo. Usare il metodo dell'elemento radice (l'elemento alla radice dell'albero che rappresenta il dispositivo) [**IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (o [**IWiaItem2::EnumChildItems)**](-wia-iwiaitem2-enumchilditems.md)per creare un oggetto enumeratore e ottenere un puntatore all'interfaccia [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) (o [**IEnumWiaItem2),**](-wia-ienumwiaitem2.md)che viene usata per esplorare l'albero degli elementi e ottenere l'accesso alle immagini o alle scansioni associate al dispositivo.

Nell'esempio seguente viene illustrata una funzione che enumera in modo ricorsivo tutti gli elementi di un albero, a partire da un elemento radice passato alla funzione .


```
    HRESULT EnumerateItems( IWiaItem *pWiaItem ) //XP or earlier
    HRESULT EnumerateItems( IWiaItem2 *pWiaItem ) //Vista or later
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaItem)
        {
            return E_INVALIDARG;
        }

        //
        // Get the item type for this item.
        //
        LONG lItemType = 0;
        HRESULT hr = pWiaItem->GetItemType( &lItemType );
        if (SUCCEEDED(hr))
        {
            //
            // If it is a folder, or it has attachments, enumerate its children.
            //
            if (lItemType & WiaItemTypeFolder || lItemType & WiaItemTypeHasAttachments)
            {
                //
                // Get the child item enumerator for this item.
                //
                IEnumWiaItem *pEnumWiaItem = NULL; //XP or earlier
                IEnumWiaItem2 *pEnumWiaItem = NULL; //Vista or later
                
                hr = pWiaItem->EnumChildItems( &pEnumWiaItem );
                if (SUCCEEDED(hr))
                {
                    //
                    // Loop until you get an error or pEnumWiaItem->Next returns
                    // S_FALSE to signal the end of the list.
                    //
                    while (S_OK == hr)
                    {
                        //
                        // Get the next child item.
                        //
                        IWiaItem *pChildWiaItem = NULL; //XP or earlier
                        IWiaItem2 *pChildWiaItem = NULL; //Vista or later
                        
                        hr = pEnumWiaItem->Next( 1, &pChildWiaItem, NULL );

                        //
                        // pEnumWiaItem->Next will return S_FALSE when the list is
                        // exhausted, so check for S_OK before using the returned
                        // value.
                        //
                        if (S_OK == hr)
                        {
                            //
                            // Recurse into this item.
                            //
                            hr = EnumerateItems( pChildWiaItem );

                            //
                            // Release this item.
                            //
                            pChildWiaItem->Release();
                            pChildWiaItem = NULL;
                        }
                    }

                    //
                    // If the result of the enumeration is S_FALSE (which
                    // is normal), change it to S_OK.
                    //
                    if (S_FALSE == hr)
                    {
                        hr = S_OK;
                    }

                    //
                    // Release the enumerator.
                    //
                    pEnumWiaItem->Release();
                    pEnumWiaItem = NULL;
                }
            }
        }
        return  hr;
    }
```



La funzione accetta il parametro **pWiaItem**, un puntatore all'interfaccia [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) (o [**IWiaItem2**](-wia-iwiaitem2.md)) dell'elemento radice dell'albero degli elementi da enumerare.

In primo luogo, la funzione verifica se l'elemento è una cartella o se dispone di allegati. In caso contrario, chiama il metodo [**IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (o [**IWiaItem2::EnumChildItems)**](-wia-iwiaitem2-enumchilditems.md)di **pWiaItem** per creare un oggetto enumeratore per l'albero degli elementi. Se questa chiamata ha esito positivo e l'enumeratore è valido, la funzione scorre gli elementi figlio e chiama in modo ricorsivo su ogni elemento, trattando ognuno di essi come un potenziale elemento radice per il livello successivo di elementi figlio.

In questo modo, la funzione enumera tutti i rami dell'albero degli elementi sotto l'elemento radice passato a **EnumerateItems.**

 

 



