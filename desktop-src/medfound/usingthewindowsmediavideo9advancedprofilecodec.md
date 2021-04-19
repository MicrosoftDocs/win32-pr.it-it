---
description: Uso del profilo avanzato Windows Media Video 9
ms.assetid: 2abc0efc-dd11-4921-897c-209a26f8ba1d
title: Uso del profilo avanzato Windows Media Video 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692243117cde3b4b5f1179c5f7324d25842191b6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320518"
---
# <a name="using-the-windows-media-video-9-advanced-profile"></a><span data-ttu-id="79593-103">Uso del profilo avanzato Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="79593-103">Using the Windows Media Video 9 Advanced Profile</span></span>

<span data-ttu-id="79593-104">Le procedure video di base descritte nella sezione [utilizzo del video](workingwithvideo.md) si applicano anche direttamente al profilo avanzato Windows Media video 9.</span><span class="sxs-lookup"><span data-stu-id="79593-104">The basic video procedures described in the [Working with Video](workingwithvideo.md) section also apply directly to the Windows Media Video 9 Advanced Profile.</span></span> <span data-ttu-id="79593-105">Non sono necessarie procedure particolari.</span><span class="sxs-lookup"><span data-stu-id="79593-105">No special procedures are required.</span></span>

<span data-ttu-id="79593-106">Il profilo avanzato Windows Media Video 9 è associato agli identificatori di classe CLSID \_ CWMV9EncMediaObject e CLSID \_ CWMVDecMediaObject.</span><span class="sxs-lookup"><span data-stu-id="79593-106">The Windows Media Video 9 Advanced Profile is associated with the class identifiers CLSID\_CWMV9EncMediaObject and CLSID\_CWMVDecMediaObject.</span></span> <span data-ttu-id="79593-107">Il valore di FOURCC per i tipi di supporto che usano questo codec è "WVC1".</span><span class="sxs-lookup"><span data-stu-id="79593-107">The FOURCC value for media types using this codec is "WVC1".</span></span>

<span data-ttu-id="79593-108">Il profilo avanzato Windows Media Video 9 supporta tutte le modalità di codifica comuni, nonché la codifica interlacciata, la codifica mista interlacciata e progressiva, le risoluzioni diverse dalle funzionalità di visualizzazione e riduzione degli intervalli.</span><span class="sxs-lookup"><span data-stu-id="79593-108">The Windows Media Video 9 Advanced Profile supports all common encoding modes as well interlaced encoding, mixed interlaced and progressive encoding, resolutions that are different than the display, and range reduction features.</span></span> <span data-ttu-id="79593-109">Un'altra funzionalità è la possibilità di archiviare i metadati di sequenza e frame nel flusso di bit stesso; in precedenza era necessario usare l'API ASF e le estensioni di unità dati.</span><span class="sxs-lookup"><span data-stu-id="79593-109">Another feature is the ability to store sequence and frame metadata in the bit-stream itself; previously this had required use of the ASF and Data Unit Extensions API.</span></span>

<span data-ttu-id="79593-110">Le seguenti proprietà del profilo avanzato Windows Media Video 9, che può essere controllato usando le impostazioni del registro di sistema, non hanno stringhe **IPropertyBag** o **IPropertyStore** corrispondenti:</span><span class="sxs-lookup"><span data-stu-id="79593-110">The following properties of the Windows Media Video 9 Advanced Profile, which can be controlled using registry settings, do not have corresponding **IPropertyBag** or **IPropertyStore** strings:</span></span>

-   <span data-ttu-id="79593-111">Opzione DQuant.</span><span class="sxs-lookup"><span data-stu-id="79593-111">Dquant Option.</span></span>
-   <span data-ttu-id="79593-112">DQuant livello di attendibilità.</span><span class="sxs-lookup"><span data-stu-id="79593-112">Dquant Strength.</span></span>
-   <span data-ttu-id="79593-113">Forza sovrapposizione.</span><span class="sxs-lookup"><span data-stu-id="79593-113">Force Overlap.</span></span>
-   <span data-ttu-id="79593-114">Metodo di costo del vettore di movimento.</span><span class="sxs-lookup"><span data-stu-id="79593-114">Motion Vector Cost Method.</span></span>

## <a name="achieving-optimal-visual-quality"></a><span data-ttu-id="79593-115">Ottenere qualità visiva ottimale</span><span class="sxs-lookup"><span data-stu-id="79593-115">Achieving Optimal Visual Quality</span></span>

<span data-ttu-id="79593-116">Per la maggior parte dei dati video, per ottenere una qualità visiva ottimale usando il profilo avanzato Windows Media Video 9, è possibile impostare la proprietà [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) su 1.</span><span class="sxs-lookup"><span data-stu-id="79593-116">For most video data, to achieve optimal visual quality using the Windows Media Video 9 Advanced Profile, you can set the [MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) property to 1.</span></span>

## <a name="about-the-previous-windows-media-video-9-advanced-profile-codecs"></a><span data-ttu-id="79593-117">Informazioni sui codec precedenti del profilo avanzato Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="79593-117">About the Previous Windows Media Video 9 Advanced Profile Codecs</span></span>

<span data-ttu-id="79593-118">La versione corrente del codec del profilo avanzato Windows Media Video 9 è basata sulla società di Motion Picture and Television Engineers (SMPTE) standard per il profilo avanzato VC-1 (SMPTE 421M).</span><span class="sxs-lookup"><span data-stu-id="79593-118">The current version of the Windows Media Video 9 Advanced Profile codec is based on the Society of Motion Picture and Television Engineers (SMPTE) standard for VC-1 (SMPTE 421M) Advanced Profile.</span></span> <span data-ttu-id="79593-119">Questo codec sostituisce il codec precedente di Windows, detto anche Windows Media Video 9 Advanced Profile codec, identificato dal codice FOURCC "WMVA".</span><span class="sxs-lookup"><span data-stu-id="79593-119">This codec replaces the earlier codec from Windows also called the Windows Media Video 9 Advanced Profile codec which was identified by the FOURCC code "WMVA".</span></span> <span data-ttu-id="79593-120">La versione precedente del codec VC-1 è stata implementata prima che lo standard del profilo avanzato VC-1 venisse finalizzato e non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="79593-120">The previous version of the VC-1 codec was implemented before the VC-1 advanced profile standard was finalized, and is no longer supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79593-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="79593-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79593-122">Uso dei video</span><span class="sxs-lookup"><span data-stu-id="79593-122">Working with Video</span></span>](workingwithvideo.md)
</dt> 
<dt>

[<span data-ttu-id="79593-123">Uso delle impostazioni avanzate del codec del profilo avanzato Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="79593-123">Using the Advanced Settings of the Windows Media Video 9 Advanced Profile Codec</span></span>](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx)
</dt> </dl>

 

 



