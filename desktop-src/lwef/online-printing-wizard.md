---
title: Stampa guidata online
description: La Windows guidata stampa online di Vista consente agli utenti di ordinare stampe di foto dai rivenditori di stampa online partecipanti.
ms.assetid: 1e73a5d0-2ca8-4eca-846a-bd69eee257cb
keywords:
- Stampa guidata online
- icone, Stampa guidata online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc402f1fe5853c7a255ea45940d62efcd092c424be6905287315c5cfe5fc7504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975921"
---
# <a name="online-printing-wizard"></a>Stampa guidata online

La Windows guidata stampa online di Vista consente agli utenti di ordinare stampe di foto dai rivenditori di stampa online partecipanti. Questa procedura guidata è progettata in modo che possa essere richiamata a livello di codice da qualsiasi applicazione che voglia offrire agli utenti la possibilità di ordinare stampe di foto. La Stampa guidata foto è disponibile in Windows Vista. PIX per Windows

-   [Funzionalità fornite dalla Stampa guidata online](#features-provided-by-the-online-print-wizard)
-   [Formati di file foto supportati](#supported-photo-file-formats)
-   [Avvio della Stampa guidata online a livello di codice](#programmatically-launching-the-online-print-wizard)
-   [Accesso all'icona della Stampa guidata online](#accessing-the-online-print-wizard-icon)
-   [Proprietà MRU della Stampa guidata online](#online-print-wizard-mru-properties)

## <a name="features-provided-by-the-online-print-wizard"></a>Funzionalità fornite dalla Stampa guidata online

La Windows guidata stampa online di Vista consente agli utenti di ordinare stampe da una selezione di rivenditori di stampa online partecipanti. Quando viene richiamata, la procedura guidata:

1.  Accetta un file o un elenco di file per i quali devono essere ordinate le stampe.
2.  Recupera automaticamente l'elenco corrente dei rivenditori di stampa online partecipanti e consente all'utente di selezionare il rivenditore da cui acquistare le stampe foto.
3.  Guida l'utente nel processo o nell'ordinamento delle stampe.

Qualsiasi applicazione può trarre vantaggio dalle funzionalità offerte dalla Windows stampa online di Vista. Un'applicazione deve passare solo il file o i file per cui verranno ordinate le stampe e la procedura guidata guida l'utente nel processo di ordinamento.

Nella figura seguente viene illustrata la Windows guidata stampa online di Vista con un elenco di esempio dei rivenditori di stampa online partecipanti.

![Creazione guidata stampa online di Windows Vista](images/opw.png)

## <a name="supported-photo-file-formats"></a>Formati di file foto supportati

La Windows guidata stampa online di Vista supporta qualsiasi formato di file di immagine per il quale è installato un codec WIC (Windows Imaging Component). WIC offre diversi codec standard, tra cui:

-   Bitmap (BMP)
-   Graphics Interchange Format (GIF)
-   Formato icona (ICO)
-   Joint Photographic Experts Group (JPEG)
-   Portable Network Graphics (PNG)
-   Tagged Image File Format (TIFF)
-   Windows Formato foto multimediale

Per altre informazioni sui codec WIC e WIC, vedere Windows [Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx).

I formati di file supportati dai rivenditori di stampa online variano da rivenditore a rivenditore; è possibile che un rivenditore specifico non supporti tutti i formati di file supportati dalla Windows stampa online di Vista. Se l'utente tenta di ordinare le stampe in un formato non supportato dal rivenditore selezionato, la Stampa guidata in linea di Windows Vista notifica all'utente che il rivenditore selezionato non supporta il formato di file inviato.

## <a name="programmatically-launching-the-online-print-wizard"></a>Avvio della Stampa guidata online a livello di codice

Per richiamare la Windows guidata stampa online di Vista, chiamare [l'interfaccia IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) con l'identificatore di classe (CLSID) seguente:


```
CLSID_PublishDropTarget
```



Questo CLSID è definito in Shobjidl.h e Shobjidl.idl. I file che devono essere elaborati dalla Windows guidata stampa online di Vista vengono specificati in un [oggetto IDataObject.](/windows/win32/api/objidl/nn-objidl-idataobject)

Nell'esempio di codice seguente viene illustrato come richiamare la Windows guidata stampa online di Vista.


```
// A data object that contains the list of photos to print.
IDataObject* pDataObject;

// Create the Photo Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
hr = CoCreateInstance(CLSID_PublishDropTarget,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&spDropTarget));

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);}
```



## <a name="accessing-the-online-print-wizard-icon"></a>Accesso all'icona della Stampa guidata online

La Windows guidata stampa online di Vista esporta un'icona accessibile e visualizzata dalle applicazioni che la chiamano. Nella figura seguente viene illustrata l Windows di Stampa guidata vista online.

![Icona della stampa guidata online di Windows Vista](images/opw-icon.png)

Nell'esempio di codice seguente viene illustrato come recuperare l'indice per l'icona della Stampa guidata Windows Vista Online leggendo la **proprietà OPWIcon.**


```
// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Get the Online Printing Wizard properties.
CComPtr<IPropertyBag> spPropsBag;

spDropTarget->QueryInterface(IID_PPV_ARGS(&spPropsBag));

// Read the icon index from the properties set. 
CComVariant vtIcon;
int nIndex;
hr = spPropsBag->Read(L"OPWIcon", &vtIcon, NULL);

if SUCCEEDED(hr)
{
    nIndex = vtIcon.lVal;
}
```



## <a name="online-print-wizard-mru-properties"></a>Proprietà MRU della Stampa guidata online

La Windows guidata stampa online di Vista definisce tre proprietà correlate al rivenditore di stampa online usato più di recente.



| Nome della proprietà | Valore proprietà/Funzione                                                                                                                                                                                                                                                   |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MRUIcon**   | L'indice dell'icona per il rivenditore di stampa online usato più di recente può essere letto da questa proprietà.                                                                                                                                                                 |
| **MRUName**   | Il nome del rivenditore di stampa online usato più di recente può essere letto da questa proprietà.                                                                                                                                                                               |
| **UseMRU**    | Valore **VARIANT** **VT \_ BOOL** che indica se la procedura guidata deve ignorare la pagina di selezione del rivenditore di stampa online e usare il rivenditore di stampa online usato più di recente. Impostare questa proprietà su **VARIANT \_ TRUE per ignorare** la pagina di selezione del rivenditore. |



 

L'esempio di codice seguente illustra come impostare la proprietà UseMRU in modo che la Stampa guidata di Windows Vista esempli la pagina di selezione del rivenditore di stampa online e selezioni automaticamente il rivenditore usato più di recente.


```
// A data object that contains the list of photos to order prints for.
IDataObject* pDataObject;

// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Set the UserMRU property to true to skip retailer selection and use 
// the MRU retailer instead.    
CComQIPtr<IPropertyBag> spPropsBag(spDropTarget);
if(spPropsBag) 
{
    VARIANT varTrue = {0};
    varTrue.vt = VT_BOOL;
    varTrue.boolVal = VARIANT_TRUE;
    spPropsBag->Write(L"UseMRU", &varTrue);
}

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);
```



L'esempio di codice seguente illustra come leggere le proprietà MRUName e MRUIcon.


```
// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Get the Online Printing Wizard properties.
CComPtr<IPropertyBag> spPropsBag;
spDropTarget->QueryInterface(IID_PPV_ARGS(&spPropsBag));

CComVariant vtMRUName, vtMRUIconIndex;
CComBSTR bstrMRUName;
int nMRUIconIndex;

// Get the MRU name value.
hr = spPropsBag->Read(L"MRUName", &vtMRUName, NULL);
if SUCCEEDED(hr) 
{
    bstrMRUName = vtMRUName.bstrVal;
}

// Get the MRU icon index value.
hr = spPropsBag->Read(L"MRUIcon", &vtMRUIconIndex, NULL);
if SUCCEEDED(hr)
{
    nMRUIconIndex = vtMRUIconIndex.lVal;
}
```



 

 