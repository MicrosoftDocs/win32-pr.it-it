---
title: Per modificare i metadati con il writer
description: Per modificare i metadati con il writer
ms.assetid: 86badfe3-64bc-4285-a231-f6c0ebf4f262
keywords:
- Windows Media Format SDK, modifica dei metadati con il writer
- Windows Media Format SDK, modifica dei metadati
- Formato di sistemi avanzati (ASF), modifica dei metadati con il writer
- ASF (Advanced Systems Format), modifica dei metadati con il writer
- ASF (Advanced Systems Format), modifica dei metadati
- ASF (formato di sistemi avanzati), modifica dei metadati
- metadati, modifica con il writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2823b266b51da366683ac0b5cf65e10debf1ad
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104398766"
---
# <a name="to-edit-metadata-with-the-writer"></a><span data-ttu-id="14a57-110">Per modificare i metadati con il writer</span><span class="sxs-lookup"><span data-stu-id="14a57-110">To Edit Metadata with the Writer</span></span>

<span data-ttu-id="14a57-111">È possibile accedere direttamente dal writer, i metadati che entreranno nell'intestazione del file.</span><span class="sxs-lookup"><span data-stu-id="14a57-111">You can access, directly from the writer, the metadata that will go into the header of the file.</span></span> <span data-ttu-id="14a57-112">Chiamare il metodo **QueryInterface** di qualsiasi interfaccia nell'oggetto writer per ottenere un puntatore all'interfaccia [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) o [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) .</span><span class="sxs-lookup"><span data-stu-id="14a57-112">Call the **QueryInterface** method of any interface in the writer object to obtain a pointer to the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) or [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) interface.</span></span> <span data-ttu-id="14a57-113">Quando si dispone di un puntatore all'interfaccia appropriata, è possibile manipolare i metadati come se il file fosse stato caricato nell'oggetto editor dei metadati.</span><span class="sxs-lookup"><span data-stu-id="14a57-113">After you have a pointer to the appropriate interface, you can manipulate the metadata just as you would if you had loaded the file in the metadata editor object.</span></span> <span data-ttu-id="14a57-114">Per ulteriori informazioni sulla modifica dei metadati, vedere [utilizzo dei metadati](working-with-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="14a57-114">For more information about editing metadata, see [Working with Metadata](working-with-metadata.md).</span></span>

<span data-ttu-id="14a57-115">È necessario apportare tutte le modifiche ai metadati prima di chiamare [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span><span class="sxs-lookup"><span data-stu-id="14a57-115">You must make all changes to the metadata before calling [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

> [!Note]  
> <span data-ttu-id="14a57-116">Se si impostano i metadati per un file, si scrive il file e quindi si prepara la scrittura di un nuovo file senza rilasciare il writer, alcuni metadati impostati per il primo file rimarranno impostati e verranno inclusi nei file successivi.</span><span class="sxs-lookup"><span data-stu-id="14a57-116">If you set metadata for a file, write the file, and then prepare to write a new file without releasing the writer, some metadata that was set for the first file will remain set and will be included with subsequent files.</span></span> <span data-ttu-id="14a57-117">Quando si scrivono più file con la stessa istanza dell'oggetto writer, sono disponibili due opzioni: controllare tutti i metadati prima di scrivere ogni file oppure scrivere solo nei metadati del writer che si applicano a tutti i file che si stanno scrivendo.</span><span class="sxs-lookup"><span data-stu-id="14a57-117">When writing several files with the same instance of the writer object, you have two options: check all the metadata before writing each file, or only write in the writer metadata that applies to all of the files you are writing.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="14a57-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="14a57-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14a57-119">**Scrittura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="14a57-119">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




