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
# <a name="loading-a-project-file"></a><span data-ttu-id="4c658-103">Caricamento di un file di progetto</span><span class="sxs-lookup"><span data-stu-id="4c658-103">Loading a Project File</span></span>

<span data-ttu-id="4c658-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="4c658-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="4c658-105">Per caricare un file di progetto, sono necessari due componenti: il parser XML e una sequenza temporale vuota.</span><span class="sxs-lookup"><span data-stu-id="4c658-105">To load a project file, you need two components: the XML parser and an empty timeline.</span></span> <span data-ttu-id="4c658-106">Il parser XML legge un file di progetto XML e crea ogni oggetto definito nel file.</span><span class="sxs-lookup"><span data-stu-id="4c658-106">The XML parser reads an XML project file and creates each object defined in the file.</span></span> <span data-ttu-id="4c658-107">Inserisce quindi gli oggetti nella sequenza temporale e imposta gli attributi della sequenza temporale, ad esempio la frequenza dei fotogrammi predefinita.</span><span class="sxs-lookup"><span data-stu-id="4c658-107">Then it inserts the objects into the timeline and sets any timeline attributes, such as the default frame rate.</span></span> <span data-ttu-id="4c658-108">Nell'esempio di codice seguente viene caricato un file.</span><span class="sxs-lookup"><span data-stu-id="4c658-108">The following code example loads a file.</span></span>


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



<span data-ttu-id="4c658-109">Il parser espone l'interfaccia [**IXml2Dex**](ixml2dex.md) , che contiene i metodi per il caricamento e il salvataggio dei file di progetto.</span><span class="sxs-lookup"><span data-stu-id="4c658-109">The parser exposes the [**IXml2Dex**](ixml2dex.md) interface, which contains methods for loading and saving project files.</span></span> <span data-ttu-id="4c658-110">La sequenza temporale espone l'interfaccia [**IAMTimeline**](iamtimeline.md) , che contiene i metodi per la modifica della sequenza temporale e la creazione di nuovi oggetti sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="4c658-110">The timeline exposes the [**IAMTimeline**](iamtimeline.md) interface, which contains methods for manipulating the timeline and creating new timeline objects.</span></span> <span data-ttu-id="4c658-111">Chiamare la funzione **CoCreateInstance** per creare ogni componente, come illustrato.</span><span class="sxs-lookup"><span data-stu-id="4c658-111">Call the **CoCreateInstance** function to create each component, as shown.</span></span> <span data-ttu-id="4c658-112">Si tenga presente che, creando una nuova istanza, si incrementa il conteggio dei riferimenti nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="4c658-112">Remember that by creating a new instance, you are incrementing the reference count on the interface.</span></span> <span data-ttu-id="4c658-113">Per evitare perdite di memoria, rilasciare sempre un'interfaccia quando viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="4c658-113">To avoid memory leaks, always release an interface when you are through with it.</span></span> <span data-ttu-id="4c658-114">In questo esempio, il puntatore a **IXml2Dex** non è necessario per altri scopi, quindi è possibile rilasciare l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="4c658-114">In this example, the pointer to **IXml2Dex** is not needed for anything more, so you can release the interface.</span></span> <span data-ttu-id="4c658-115">Il puntatore a **IAMTimeline** è ancora necessario per la visualizzazione in anteprima della sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="4c658-115">The pointer to **IAMTimeline** is still needed for previewing the timeline.</span></span>

<span data-ttu-id="4c658-116">Il metodo [**IXml2Dex:: ReadXMLFile**](ixml2dex-readxmlfile.md) legge il file specificato e popola la sequenza temporale con gli oggetti definiti nel file.</span><span class="sxs-lookup"><span data-stu-id="4c658-116">The [**IXml2Dex::ReadXMLFile**](ixml2dex-readxmlfile.md) method reads the specified file and populates the timeline with the objects defined in the file.</span></span> <span data-ttu-id="4c658-117">Il nome file viene specificato usando un valore **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="4c658-117">The file name is specified using a **BSTR** value.</span></span> <span data-ttu-id="4c658-118">Per abbreviare l'esempio, il nome del file nell'esempio viene specificato come stringa letterale.</span><span class="sxs-lookup"><span data-stu-id="4c658-118">To shorten the example, the file name in the example is given as a literal string.</span></span> <span data-ttu-id="4c658-119">In genere, è possibile ottenerlo da una finestra di dialogo Apri file o qualcosa di simile.</span><span class="sxs-lookup"><span data-stu-id="4c658-119">Normally, you obtain it from an Open File dialog or something similar.</span></span>

<span data-ttu-id="4c658-120">Se il metodo **ReadXml** ha esito positivo, viene restituito un codice di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4c658-120">If the **ReadXML** method is successful, it returns a success code.</span></span> <span data-ttu-id="4c658-121">In caso contrario, viene restituito un codice di errore come VFW \_ E \_ formato di file non valido \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4c658-121">Otherwise, it returns an error code such as VFW\_E\_INVALID\_FILE\_FORMAT.</span></span> <span data-ttu-id="4c658-122">Controllare sempre il valore restituito per gestire correttamente le condizioni di errore.</span><span class="sxs-lookup"><span data-stu-id="4c658-122">Always check the return value, in order to handle error conditions gracefully.</span></span> <span data-ttu-id="4c658-123">Per brevità, il codice di esempio non controlla la presenza di errori.</span><span class="sxs-lookup"><span data-stu-id="4c658-123">Again for brevity, the example code does not check for errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c658-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4c658-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c658-125">Caricamento e visualizzazione in anteprima di un progetto</span><span class="sxs-lookup"><span data-stu-id="4c658-125">Loading and Previewing a Project</span></span>](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



