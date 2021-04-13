---
title: Esempio della finestra di dialogo Apri
description: L'esempio di forme utilizzato è stato piuttosto escogitato. Passiamo a un oggetto COM che è possibile usare in un programma Windows reale la finestra di dialogo Apri.
ms.assetid: f426cf83-ed24-4eeb-bc28-b5871b824525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d896c5928c5bcf5e7dae7835d011ddf0f1fbd6e6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398990"
---
# <a name="example-the-open-dialog-box"></a>Esempio: finestra di dialogo Apri

L' `Shapes` esempio che è stato usato è piuttosto escogitato. Passiamo a un oggetto COM che è possibile usare in un programma Windows reale: la finestra di dialogo **Apri** .

![screenshot che mostra la finestra di dialogo Apri](images/fileopen01.png)

Per visualizzare la finestra di dialogo **Apri** , un programma può utilizzare un oggetto com denominato oggetto finestra di dialogo elemento comune. La finestra di dialogo elemento comune implementa un'interfaccia denominata [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog), dichiarata nel file di intestazione ShObjIdl. h.

Ecco un programma che Visualizza l'utente nella finestra di dialogo **Apri** . Se l'utente seleziona un file, il programma visualizza una finestra di dialogo contenente il nome del file.


```C++
#include <windows.h>
#include <shobjidl.h> 

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
        COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        IFileOpenDialog *pFileOpen;

        // Create the FileOpenDialog object.
        hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL, 
                IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

        if (SUCCEEDED(hr))
        {
            // Show the Open dialog box.
            hr = pFileOpen->Show(NULL);

            // Get the file name from the dialog box.
            if (SUCCEEDED(hr))
            {
                IShellItem *pItem;
                hr = pFileOpen->GetResult(&pItem);
                if (SUCCEEDED(hr))
                {
                    PWSTR pszFilePath;
                    hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);

                    // Display the file name to the user.
                    if (SUCCEEDED(hr))
                    {
                        MessageBoxW(NULL, pszFilePath, L"File Path", MB_OK);
                        CoTaskMemFree(pszFilePath);
                    }
                    pItem->Release();
                }
            }
            pFileOpen->Release();
        }
        CoUninitialize();
    }
    return 0;
}
```



Questo codice usa alcuni concetti che verranno descritti più avanti nel modulo, quindi non è necessario preoccuparsi se non si conoscono tutti i concetti. Ecco una struttura di base del codice:

1.  Chiamare [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) per inizializzare la libreria com.
2.  Chiamare [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare l'oggetto finestra di dialogo elemento comune e ottenere un puntatore all'interfaccia [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) dell'oggetto.
3.  Chiamare il metodo **show** dell'oggetto, che mostra la finestra di dialogo all'utente. Questo metodo si blocca fino a quando l'utente non dimentica la finestra di dialogo.
4.  Chiamare il metodo [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) dell'oggetto. Questo metodo restituisce un puntatore a un secondo oggetto COM, denominato oggetto *elemento della shell* . L'elemento della shell, che implementa l'interfaccia [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) , rappresenta il file selezionato dall'utente.
5.  Chiamare il metodo [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) dell'elemento della shell. Questo metodo ottiene il percorso del file sotto forma di stringa.
6.  Visualizza una finestra di messaggio in cui viene visualizzato il percorso del file.
7.  Chiamare [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) per annullare l'inizializzazione della libreria com.

Passaggi 1, 2 e 7 funzioni di chiamata definite dalla libreria COM. Si tratta di funzioni COM generiche. I passaggi da 3 a 5 chiamano i metodi definiti dall'oggetto finestra di dialogo elemento comune.

In questo esempio vengono illustrate entrambe le varietà di creazione di oggetti: la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) generica e un metodo ([**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult)) specifico per l'oggetto finestra di dialogo elemento comune.

## <a name="next"></a>Prossima

[Gestione della durata di un oggetto](managing-the-lifetime-of-an-object.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Apri esempio di finestra di dialogo](open-dialog-box-sample.md)
</dt> </dl>

 

 