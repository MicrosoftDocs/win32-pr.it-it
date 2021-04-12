---
title: Stampa guidata online
description: La procedura guidata di stampa online di Windows Vista consente agli utenti di ordinare stampe di foto da rivenditori di stampa online.
ms.assetid: 1e73a5d0-2ca8-4eca-846a-bd69eee257cb
keywords:
- Stampa guidata online
- icone, stampa guidata online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8536eea7a51eddb2dbb46d10c9291a60edfdc74e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337422"
---
# <a name="online-printing-wizard"></a>Stampa guidata online

La procedura guidata di stampa online di Windows Vista consente agli utenti di ordinare stampe di foto da rivenditori di stampa online. Questa procedura guidata è progettata in modo da poter essere richiamata a livello di codice da qualsiasi applicazione che desideri offrire agli utenti la possibilità di ordinare stampe di foto. La stampa guidata foto è disponibile in Windows Vista. PIX per Windows

-   [Funzionalità fornite dalla procedura guidata di stampa online](#features-provided-by-the-online-print-wizard)
-   [Formati di file di foto supportati](#supported-photo-file-formats)
-   [Avvio a livello di codice della procedura guidata di stampa online](#programmatically-launching-the-online-print-wizard)
-   [Accesso all'icona della procedura guidata di stampa online](#accessing-the-online-print-wizard-icon)
-   [Proprietà MRU della procedura guidata di stampa online](#online-print-wizard-mru-properties)

## <a name="features-provided-by-the-online-print-wizard"></a>Funzionalità fornite dalla procedura guidata di stampa online

La procedura guidata di stampa online di Windows Vista consente agli utenti di ordinare le stampe da una selezione di rivenditori di stampa online. Quando viene richiamato, la procedura guidata:

1.  Accetta un file o un elenco di file per cui è necessario ordinare le stampe.
2.  Recupera automaticamente l'elenco corrente dei rivenditori di stampa online partecipanti e consente all'utente di selezionare il rivenditore da cui acquistare le stampe foto.
3.  Guida l'utente attraverso il processo o Ordina le stampe.

Qualsiasi applicazione può trarre vantaggio dalle funzionalità offerte dalla procedura guidata di stampa online di Windows Vista. Un'applicazione deve passare solo il file o i file per i quali verranno ordinate le stampe e la procedura guidata guiderà l'utente attraverso il processo di ordinamento.

Nella figura seguente viene illustrata la procedura guidata di stampa online di Windows Vista che visualizza un elenco di esempio dei rivenditori di stampa online partecipanti.

![procedura guidata di stampa online di Windows Vista](images/opw.png)

## <a name="supported-photo-file-formats"></a>Formati di file di foto supportati

La procedura guidata di stampa online di Windows Vista supporta qualsiasi formato di file di immagine per cui è installato un codec di Windows Imaging Component (WIC). WIC fornisce diversi codec standard, tra cui:

-   Bitmap (BMP)
-   Graphics Interchange Format (GIF)
-   Formato dell'icona (ICO)
-   Joint Photographic Experts Group (JPEG)
-   Portable Network Graphics (PNG)
-   Tagged Image File Format (TIFF)
-   Formato foto Windows Media

Per ulteriori informazioni sui codec WIC e WIC, vedere componente per la [creazione di immagini Windows](https://msdn.microsoft.com/library/ms737408(VS.85).aspx).

I formati di file supportati dai rivenditori di stampa online variano a seconda del rivenditore. è possibile che un rivenditore specifico non supporti tutti i formati di file supportati dalla procedura guidata di stampa online di Windows Vista. Se l'utente tenta di ordinare le stampe in un formato non supportato dal rivenditore selezionato, la procedura guidata di stampa online di Windows vista informa l'utente che il rivenditore selezionato non supporta il formato di file inviato.

## <a name="programmatically-launching-the-online-print-wizard"></a>Avvio a livello di codice della procedura guidata di stampa online

Per richiamare la procedura guidata di stampa online di Windows Vista, chiamare l'interfaccia [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) con l'identificatore di classe seguente (CLSID):


```
CLSID_PublishDropTarget
```



Questo CLSID è definito in ShObjIdl. h e ShObjIdl. idl. I file che devono essere elaborati dalla stampa guidata di Windows Vista sono specificati in un oggetto [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) .

Nell'esempio di codice riportato di seguito viene illustrato come richiamare la procedura guidata di stampa online di Windows Vista.


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



## <a name="accessing-the-online-print-wizard-icon"></a>Accesso all'icona della procedura guidata di stampa online

La procedura guidata stampa online di Windows Vista consente di esportare un'icona accessibile e visualizzata dalle applicazioni che lo chiamano. Nella figura seguente viene illustrata l'icona della procedura guidata di stampa online di Windows Vista.

![icona della procedura guidata di stampa online di Windows Vista](images/opw-icon.png)

Nell'esempio di codice seguente viene illustrato come recuperare l'indice per l'icona della procedura guidata di stampa online di Windows Vista leggendo la proprietà **OPWIcon** .


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



## <a name="online-print-wizard-mru-properties"></a>Proprietà MRU della procedura guidata di stampa online

La procedura guidata di stampa online di Windows Vista definisce tre proprietà correlate al rivenditore di stampa online usato più di recente (MRU).



| Nome della proprietà | Valore/funzione della proprietà                                                                                                                                                                                                                                                   |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MRUIcon**   | L'indice dell'icona per il rivenditore di stampa online usato più di recente può essere letto da questa proprietà.                                                                                                                                                                 |
| **MRUName**   | Il nome del rivenditore di stampa online usato più di recente può essere letto da questa proprietà.                                                                                                                                                                               |
| **UseMRU**    | Un valore di **variabile** **VT \_ bool** che indica se la procedura guidata deve ignorare la pagina di selezione del rivenditore di stampa online e usare invece il rivenditore di stampa online usato più di recente. Impostare questa proprietà su **Variant \_ true** per ignorare la pagina di selezione del rivenditore. |



 

Nell'esempio di codice seguente viene illustrato come impostare la proprietà UseMRU in modo che la procedura guidata di stampa online di Windows Vista ignori la pagina di selezione del rivenditore di stampa online e selezioni automaticamente il rivenditore usato più di recente.


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



Nell'esempio di codice riportato di seguito viene illustrato come leggere le proprietà MRUName e MRUIcon.


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



 

 