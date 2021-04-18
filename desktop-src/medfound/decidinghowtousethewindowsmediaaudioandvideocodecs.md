---
description: Uso degli oggetti codec e DSP
ms.assetid: ec571d31-6542-421a-8027-d4c61ce00035
title: Uso degli oggetti codec e DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a88670298bfc16ca1dc5053cabeb4f4e631c5c47
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320648"
---
# <a name="using-the-codec-and-dsp-objects"></a><span data-ttu-id="0491d-103">Uso degli oggetti codec e DSP</span><span class="sxs-lookup"><span data-stu-id="0491d-103">Using the Codec and DSP Objects</span></span>

<span data-ttu-id="0491d-104">Esistono diversi modi per usare i codec Windows Media Audio e video e DSP per codificare, decodificare o trasformare il contenuto multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="0491d-104">There are several ways to use the Windows Media Audio and Video codecs and DSPs to encode, decode, or transform your digital media content.</span></span> <span data-ttu-id="0491d-105">Il Windows Media Audio e il codec video e l'API DSP sono destinati agli utenti che devono configurare manualmente gli oggetti codec e DSP o usarli al di fuori del contesto uno degli SDK di Windows Media, ad esempio Windows Media Format SDK o Media Foundation SDK.</span><span class="sxs-lookup"><span data-stu-id="0491d-105">The Windows Media Audio and Video Codec and DSP API is intended for those users who need to configure codec and DSP objects manually or use them outside of the context one of the Windows Media SDKs, such as the Windows Media Format SDK or Media Foundation SDK.</span></span>

<span data-ttu-id="0491d-106">I creatori di contenuti e gli utenti finali possono usare un'ampia gamma di strumenti e applicazioni per codificare il contenuto in flussi Windows Media Audio o Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="0491d-106">Content creators and end users can use a variety of tools and applications to encode content in Windows Media Audio or Windows Media Video streams.</span></span> <span data-ttu-id="0491d-107">Windows Media Encoder, ad esempio, è progettato appositamente per semplificare il processo di codifica.</span><span class="sxs-lookup"><span data-stu-id="0491d-107">Windows Media Encoder, for example, is specifically designed to make the encoding process easy.</span></span> <span data-ttu-id="0491d-108">Analogamente, Windows Media Player è appositamente progettato per funzionare correttamente con i dati multimediali digitali codificati nei formati Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0491d-108">Likewise, Windows Media Player is specially designed to work well with digital media data that is encoded in Windows Media formats.</span></span> <span data-ttu-id="0491d-109">Per molte applicazioni, è sufficiente utilizzare Windows Media Encoder SDK o Windows Media Player SDK.</span><span class="sxs-lookup"><span data-stu-id="0491d-109">For many applications, using the Windows Media Encoder SDK or the Windows Media Player SDK is all that is needed.</span></span> <span data-ttu-id="0491d-110">In particolare, queste due tecnologie sono valide per gli scenari che assomigliano alla funzionalità degli strumenti che consentono di automatizzare.</span><span class="sxs-lookup"><span data-stu-id="0491d-110">In particular, these two technologies are good for scenarios that resemble the functionality of the tools they automate.</span></span>

<span data-ttu-id="0491d-111">Se è necessario un maggiore controllo sul processo di codifica o decodifica, ma si intende comunque utilizzare il formato ASF (Advanced Systems Format) come contenitore per i dati multimediali, Windows Media Format SDK può essere una scelta ottimale.</span><span class="sxs-lookup"><span data-stu-id="0491d-111">If you need greater control over the encoding or decoding process, but you still intend to use the Advanced Systems Format (ASF) as a container for your media data, the Windows Media Format SDK might be a good choice.</span></span> <span data-ttu-id="0491d-112">Gli oggetti di Windows Media Format SDK forniscono un framework flessibile per la creazione di file ASF e forniscono supporto incorporato per i codec Windows Media Audio e video.</span><span class="sxs-lookup"><span data-stu-id="0491d-112">The objects of the Windows Media Format SDK provide a flexible framework for creating ASF files, and provide built-in support for the Windows Media Audio and Video codecs.</span></span>

<span data-ttu-id="0491d-113">Il Media Foundation SDK, che è una novità di Windows Vista, semplifica notevolmente la codifica e la decodifica fornendo una pipeline multimediale personalizzabile.</span><span class="sxs-lookup"><span data-stu-id="0491d-113">The Media Foundation SDK, which is new for Windows Vista, greatly simplifies encoding and decoding by providing a customizable media pipeline.</span></span> <span data-ttu-id="0491d-114">È possibile impostare le proprietà dei supporti di input e di output e il caricatore della topologia di Media Foundation configurerà automaticamente i codec necessari e DSP.</span><span class="sxs-lookup"><span data-stu-id="0491d-114">You can set input and output media properties and the Media Foundation topology loader will configure the necessary codecs and DSPs for you.</span></span>

<span data-ttu-id="0491d-115">Il motivo principale per l'uso diretto degli oggetti codec è l'uso dei codec Windows Media Audio e video all'esterno del contenitore ASF.</span><span class="sxs-lookup"><span data-stu-id="0491d-115">The primary reason for using the codec objects directly is to use the Windows Media Audio and Video codecs outside of the ASF container.</span></span> <span data-ttu-id="0491d-116">L'uso degli oggetti codec e DSP fornisce anche un livello di controllo non disponibile con le tecnologie più astratte.</span><span class="sxs-lookup"><span data-stu-id="0491d-116">Using the codec and DSP objects also provides a level of control that is unavailable using any of the more abstracted technologies.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0491d-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0491d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0491d-118">Codec Windows Media</span><span class="sxs-lookup"><span data-stu-id="0491d-118">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 



