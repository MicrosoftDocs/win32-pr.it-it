---
description: Configurazione della decodifica audio
ms.assetid: 362bd3bc-1474-4132-a8a8-e5dc0bba80e7
title: Configurazione della decodifica audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da4d6a9d41b5c504ff60f25db20265072218caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749330"
---
# <a name="configuring-audio-decoding-microsoft-media-foundation"></a><span data-ttu-id="e22ee-103">Configurazione della decodifica audio (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="e22ee-103">Configuring Audio Decoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="e22ee-104">La decodifica Windows Media Audio contenuto è molto più semplice rispetto alla codifica.</span><span class="sxs-lookup"><span data-stu-id="e22ee-104">Decoding Windows Media Audio content is much easier than encoding it.</span></span> <span data-ttu-id="e22ee-105">Dopo aver creato un oggetto Decoder audio, impostare il tipo di input usando il metodo **IMediaObject:: SetInputType** o **IMFTransform:: SetInputType** .</span><span class="sxs-lookup"><span data-stu-id="e22ee-105">After creating an audio decoder object, set the input type by using the **IMediaObject::SetInputType** or **IMFTransform::SetInputType** method.</span></span> <span data-ttu-id="e22ee-106">Il tipo di supporto utilizzato per l'input del decodificatore deve corrispondere al tipo di output utilizzato durante la codifica del contenuto.</span><span class="sxs-lookup"><span data-stu-id="e22ee-106">The media type that you use for the decoder input must match the output type that was used when the content was encoded.</span></span> <span data-ttu-id="e22ee-107">Sono inclusi i dati in formato esteso aggiunti alla struttura **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="e22ee-107">This includes the extended format data appended to the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="e22ee-108">È necessario assicurarsi che questi dati siano corretti, perché il decodificatore non è in grado di elaborare esempi senza di esso.</span><span class="sxs-lookup"><span data-stu-id="e22ee-108">You must ensure that this data is correct, because the decoder cannot process samples without it.</span></span>

<span data-ttu-id="e22ee-109">Dopo aver impostato il tipo di input, è possibile configurare tutte le funzionalità di decodificatore che si desidera utilizzare.</span><span class="sxs-lookup"><span data-stu-id="e22ee-109">After setting the input type, you can configure any decoder features you want to use.</span></span> <span data-ttu-id="e22ee-110">Le funzionalità di decodificatore, come quelle usate per la codifica, vengono impostate usando i metodi di **IPropertyBag** o **IPropertyStore**.</span><span class="sxs-lookup"><span data-stu-id="e22ee-110">Decoder features, like those used for encoding, are set using the methods of **IPropertyBag** or **IPropertyStore**.</span></span>

<span data-ttu-id="e22ee-111">Dopo aver impostato il tipo di input e aver configurato tutte le funzionalità del decodificatore, è possibile enumerare i tipi di output supportati dal decodificatore effettuando chiamate a **IMediaObject:: GetOutputType** o **IMFTransform:: GetOutputType**.</span><span class="sxs-lookup"><span data-stu-id="e22ee-111">After the input type is set and all decoder features are configured, you can enumerate the output types supported by the decoder by making calls to **IMediaObject::GetOutputType** or **IMFTransform::GetOutputType**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e22ee-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e22ee-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e22ee-113">Utilizzo di audio</span><span class="sxs-lookup"><span data-stu-id="e22ee-113">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



