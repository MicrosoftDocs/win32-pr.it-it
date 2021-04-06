---
description: 'Altre informazioni su: implementazione di un decodificatore WIC-Enabled'
ms.assetid: a26a592d-42ef-4690-95b4-48a5324be75a
title: Implementazione di un decodificatore WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebd6d56258bf18e6cc914a40efa4cd3a57a92fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883406"
---
# <a name="implementing-a-wic-enabled-decoder"></a><span data-ttu-id="c0bd1-103">Implementazione di un decodificatore WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="c0bd1-103">Implementing a WIC-Enabled Decoder</span></span>


<span data-ttu-id="c0bd1-104">L'implementazione di un decodificatore Windows Imaging Component (WIC) richiede la scrittura di due classi.</span><span class="sxs-lookup"><span data-stu-id="c0bd1-104">Implementing a Windows Imaging Component (WIC) decoder requires writing two classes.</span></span> <span data-ttu-id="c0bd1-105">Le interfacce di queste classi corrispondono direttamente alle responsabilità decodificatore descritte nella sezione [decodifica](-wic-howwicworks.md) del funzionamento [del componente Imaging di Windows](-wic-howwicworks.md).</span><span class="sxs-lookup"><span data-stu-id="c0bd1-105">The interfaces on these classes correspond directly to the decoder responsibilities outlined in the [Decoding](-wic-howwicworks.md) section of [How The Windows Imaging Component Works](-wic-howwicworks.md).</span></span>

<span data-ttu-id="c0bd1-106">Una delle classi fornisce servizi a livello di contenitore e implementa l'interfaccia [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) .</span><span class="sxs-lookup"><span data-stu-id="c0bd1-106">One of the classes provides container-level services and implements the [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) interface.</span></span> <span data-ttu-id="c0bd1-107">Se il formato dell'immagine supporta i metadati a livello di contenitore, è necessario implementare anche l'interfaccia [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) in questa classe.</span><span class="sxs-lookup"><span data-stu-id="c0bd1-107">If your image format supports container-level metadata, you must also implement the [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) interface on this class.</span></span> <span data-ttu-id="c0bd1-108">È consigliabile supportare l'interfaccia [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) sul decodificatore e sul codificatore per supportare un'esperienza utente migliore.</span><span class="sxs-lookup"><span data-stu-id="c0bd1-108">It is recommended that you support the [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) interface on both the decoder and encoder to support a better user experience.</span></span>

<span data-ttu-id="c0bd1-109">L'altra classe che sarà implementata fornisce servizi a livello di frame ed esegue la decodifica effettiva dei bit dell'immagine per ogni frame nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="c0bd1-109">The other class you will implement provides frame-level services and does the actual decoding of the image bits for each frame in the container.</span></span> <span data-ttu-id="c0bd1-110">Questa classe implementa l'interfaccia [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md) e l'interfaccia [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) .</span><span class="sxs-lookup"><span data-stu-id="c0bd1-110">This class implements the [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md) interface and the [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) interface.</span></span> <span data-ttu-id="c0bd1-111">Se si scrive un decodificatore per un formato non elaborato, si implementa anche l'interfaccia [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md) in questa classe.</span><span class="sxs-lookup"><span data-stu-id="c0bd1-111">If you are writing a decoder for a raw format, you also implement the [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md) interface on this class.</span></span> <span data-ttu-id="c0bd1-112">Oltre alle interfacce necessarie, si consiglia di implementare l'interfaccia [IWICBitmapSourceTransform](-wic-imp-iwicmetadatablockreader.md) in questa classe per consentire le migliori prestazioni possibili per il formato di immagine.</span><span class="sxs-lookup"><span data-stu-id="c0bd1-112">In addition to the required interfaces, it is highly recommended that you implement the [IWICBitmapSourceTransform](-wic-imp-iwicmetadatablockreader.md) interface on this class to enable the best possible performance for your image format.</span></span>

<span data-ttu-id="c0bd1-113">Uno degli oggetti forniti da WIC è [**ImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span><span class="sxs-lookup"><span data-stu-id="c0bd1-113">One of the objects provided by WIC is the [**ImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span></span> <span data-ttu-id="c0bd1-114">Spesso si usa l'interfaccia [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) su questo oggetto per creare diversi componenti.</span><span class="sxs-lookup"><span data-stu-id="c0bd1-114">You frequently use the [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) interface on this object to create various components.</span></span> <span data-ttu-id="c0bd1-115">Poiché viene usata di frequente, è consigliabile conservarvi un riferimento come proprietà del membro sia per le classi del codificatore che del codificatore.</span><span class="sxs-lookup"><span data-stu-id="c0bd1-115">Because it is used frequently, you should keep a reference to it as a member property on both your decoder and encoder classes.</span></span>


```C++
IWICImagingFactory* m_pImagingFactory = NULL;
IWICComponentFactory* m_pComponentFactory = NULL;
HRESULT hr;
      
hr = CoCreateInstance(CLSID_WICImagingFactory, NULL,
  CLSCTX_INPROC_SERVER, IID_IWICImagingFactory,
  (LPVOID*) m_pImagingFactory);

hr = m_pImagingFactory->QueryInterface(
  IID_IWICComponentFactory, (void**)&m_pComponentFactory);
```



## <a name="related-topics"></a><span data-ttu-id="c0bd1-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c0bd1-116">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c0bd1-117">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="c0bd1-117">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c0bd1-118">Funzionamento del componente Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="c0bd1-118">How The Windows Imaging Component Works</span></span>](-wic-howwicworks.md)
</dt> <dt>

[<span data-ttu-id="c0bd1-119">Interfacce del decodificatore</span><span class="sxs-lookup"><span data-stu-id="c0bd1-119">Decoder Interfaces</span></span>](-wic-decoderinterfaces.md)
</dt> <dt>

[<span data-ttu-id="c0bd1-120">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="c0bd1-120">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="c0bd1-121">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="c0bd1-121">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="c0bd1-122">Cenni preliminari sui metadati WIC</span><span class="sxs-lookup"><span data-stu-id="c0bd1-122">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="c0bd1-123">Panoramica della codifica</span><span class="sxs-lookup"><span data-stu-id="c0bd1-123">Encoding Overview</span></span>](-wic-creating-encoder.md)
</dt> </dl>

 

 



