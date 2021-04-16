---
description: Caricamento di un file di progetto
ms.assetid: f8d142bd-e51d-4714-893b-8e3d02506891
title: Caricamento di un file di progetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9a710795a29481740bf85390cc7122cc801a22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225395"
---
# <a name="loading-a-project-file"></a>Caricamento di un file di progetto

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Per caricare un file di progetto, sono necessari due componenti: il parser XML e una sequenza temporale vuota. Il parser XML legge un file di progetto XML e crea ogni oggetto definito nel file. Inserisce quindi gli oggetti nella sequenza temporale e imposta gli attributi della sequenza temporale, ad esempio la frequenza dei fotogrammi predefinita. Nell'esempio di codice seguente viene caricato un file.


```C++
HRESULT         hr;
IAMTimeline     *pTL = NULL;
IXml2Dex        *pXML = NULL; 
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
            IID_IAMTimeline, (void**)&pTL);
hr = CoCreateInstance(CLSID_Xml2Dex, NULL, CLSCTX_INPROC_SERVER, 
            IID_IXml2Dex, (void**)&pXML);
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.xtl"), 15);
hr = pXML->ReadXMLFile(pTL, bstrFile); 
SysFreeString(bstrFile);
pXML->Release();
```



Il parser espone l'interfaccia [**IXml2Dex**](ixml2dex.md) , che contiene i metodi per il caricamento e il salvataggio dei file di progetto. La sequenza temporale espone l'interfaccia [**IAMTimeline**](iamtimeline.md) , che contiene i metodi per la modifica della sequenza temporale e la creazione di nuovi oggetti sequenza temporale. Chiamare la funzione **CoCreateInstance** per creare ogni componente, come illustrato. Si tenga presente che, creando una nuova istanza, si incrementa il conteggio dei riferimenti nell'interfaccia. Per evitare perdite di memoria, rilasciare sempre un'interfaccia quando viene utilizzata. In questo esempio, il puntatore a **IXml2Dex** non è necessario per altri scopi, quindi è possibile rilasciare l'interfaccia. Il puntatore a **IAMTimeline** è ancora necessario per la visualizzazione in anteprima della sequenza temporale.

Il metodo [**IXml2Dex:: ReadXMLFile**](ixml2dex-readxmlfile.md) legge il file specificato e popola la sequenza temporale con gli oggetti definiti nel file. Il nome file viene specificato usando un valore **BSTR** . Per abbreviare l'esempio, il nome del file nell'esempio viene specificato come stringa letterale. In genere, è possibile ottenerlo da una finestra di dialogo Apri file o qualcosa di simile.

Se il metodo **ReadXml** ha esito positivo, viene restituito un codice di esito positivo. In caso contrario, viene restituito un codice di errore come VFW \_ E \_ formato di file non valido \_ \_ . Controllare sempre il valore restituito per gestire correttamente le condizioni di errore. Per brevità, il codice di esempio non controlla la presenza di errori.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Caricamento e visualizzazione in anteprima di un progetto](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



