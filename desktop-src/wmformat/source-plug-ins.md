---
title: Plug-in di origine
description: Plug-in di origine
ms.assetid: 9adc2d42-6273-4af0-b57f-2dde5738ed94
keywords:
- Windows Media Format SDK, plug-in di origine
- ASF (Advanced Systems Format), plug-in di origine
- ASF (Advanced Systems Format), plug-in di origine
- plug-in di origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4822b9110def4e1b758be40310f503fd56a251fd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299435"
---
# <a name="source-plug-ins"></a><span data-ttu-id="97585-107">Plug-in di origine</span><span class="sxs-lookup"><span data-stu-id="97585-107">Source Plug-ins</span></span>

<span data-ttu-id="97585-108">Un plug-in di origine è un'opzione disponibile per gli sviluppatori che desiderano implementare il proprio sistema di archiviazione per i file di Windows Media®.</span><span class="sxs-lookup"><span data-stu-id="97585-108">A source plug-in is an option available to developers who wish to implement their own storage system for Windows Media® files.</span></span> <span data-ttu-id="97585-109">Un plug-in di origine consente di eseguire questa operazione tramite l'implementazione di un'interfaccia COM denominata **IStream**, un'interfaccia standard per la fornitura di dati.</span><span class="sxs-lookup"><span data-stu-id="97585-109">A source plug-in enables this through the implementation of a COM interface called **IStream**, which is a standard interface for providing data.</span></span>

<span data-ttu-id="97585-110">Il plug-in di origine deve essere scritto come dll e la sua presenza viene resa nota all'SDK tramite una voce del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="97585-110">The source plug-in should be written as a dll, and its presence is made known to the SDK through a registry entry.</span></span> <span data-ttu-id="97585-111">In questo modo è possibile implementare un numero qualsiasi di plug-in di origine.</span><span class="sxs-lookup"><span data-stu-id="97585-111">There can be any number of source plug-ins implemented this way.</span></span> <span data-ttu-id="97585-112">Il plug-in di origine deve esportare la funzione [**WMCreateStreamForURL**](wmcreatestreamforurl.md) .</span><span class="sxs-lookup"><span data-stu-id="97585-112">The source plug-in must export the [**WMCreateStreamForURL**](wmcreatestreamforurl.md) function.</span></span>

<span data-ttu-id="97585-113">Per registrare un plug-in di origine, è necessario aggiungere la seguente voce del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="97585-113">To register a source plug-in, the following registry entry should be added:</span></span>

<span data-ttu-id="97585-114">HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows Media \\ WMSDK \\ Sources</span><span class="sxs-lookup"><span data-stu-id="97585-114">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Media\\WMSDK\\sources</span></span>

<span data-ttu-id="97585-115">Nome = "qualsiasi nome univoco"</span><span class="sxs-lookup"><span data-stu-id="97585-115">Name = "any unique name"</span></span>

<span data-ttu-id="97585-116">Valore = nome percorso della dll del plug-in di origine</span><span class="sxs-lookup"><span data-stu-id="97585-116">Value = pathname of the source plug-in dll</span></span>

<span data-ttu-id="97585-117">Una volta registrata la dll, l'applicazione può usare il metodo **IWMReader:: Open** (con l'URL appropriato come parametro) per accedere ai dati del flusso, che possono essere archiviati in file o contenitori di dati definiti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="97585-117">Once the dll has been registered, the application can use the **IWMReader::Open** method (with the appropriate URL as a parameter) to access stream data, which can be stored in files or user-defined data containers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97585-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="97585-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97585-119">**IWMReader:: Open**</span><span class="sxs-lookup"><span data-stu-id="97585-119">**IWMReader::Open**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)
</dt> <dt>

[<span data-ttu-id="97585-120">**Guida di riferimento alla programmazione**</span><span class="sxs-lookup"><span data-stu-id="97585-120">**Programming Reference**</span></span>](programming-reference.md)
</dt> <dt>

[<span data-ttu-id="97585-121">**WMCreateStreamForURL**</span><span class="sxs-lookup"><span data-stu-id="97585-121">**WMCreateStreamForURL**</span></span>](wmcreatestreamforurl.md)
</dt> </dl>

 

 




