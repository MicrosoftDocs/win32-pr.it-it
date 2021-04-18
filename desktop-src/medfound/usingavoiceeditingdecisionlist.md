---
description: Uso di un elenco di decisioni di modifica per la codifica vocale
ms.assetid: a3d88483-acc9-47cf-8735-f17bd3b4ad57
title: Uso di un elenco di decisioni di modifica per la codifica vocale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970cc40bc5749b9edc1017546020fa3806a9730b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310168"
---
# <a name="using-an-editing-decision-list-for-encoding-voice"></a><span data-ttu-id="8524b-103">Uso di un elenco di decisioni di modifica per la codifica vocale</span><span class="sxs-lookup"><span data-stu-id="8524b-103">Using an Editing Decision List for Encoding Voice</span></span>

<span data-ttu-id="8524b-104">Un elenco di decisioni di modifica (EDL) indica i dati forniti a un codec che fornisce informazioni sul modo in cui devono essere codificate parti specifiche del contenuto.</span><span class="sxs-lookup"><span data-stu-id="8524b-104">An editing decision list (EDL), is data given to a codec that provides information about how specific portions of content should be encoded.</span></span> <span data-ttu-id="8524b-105">Il codec Windows Media Audio 9 Voice supporta un semplice EDL in cui è possibile specificare le parti di contenuto che contengono musica.</span><span class="sxs-lookup"><span data-stu-id="8524b-105">The Windows Media Audio 9 Voice codec supports a simple EDL in which you can specify the portions of content that contain music.</span></span> <span data-ttu-id="8524b-106">Per impostazione predefinita, il codec rileva i passaggi di musica stessa quando è configurato per codificare contenuto misto.</span><span class="sxs-lookup"><span data-stu-id="8524b-106">By default, the codec detects passages of music itself when configured to encode mixed content.</span></span> <span data-ttu-id="8524b-107">Usare EDL solo se il codec non rileva correttamente i tipi di contenuto.</span><span class="sxs-lookup"><span data-stu-id="8524b-107">You should use an EDL only if the codec is not detecting the content types correctly.</span></span>

<span data-ttu-id="8524b-108">Per usare un EDL, il codificatore vocale deve essere impostato in modo da codificare il contenuto misto.</span><span class="sxs-lookup"><span data-stu-id="8524b-108">To use an EDL, the voice encoder must be set to encode mixed content.</span></span> <span data-ttu-id="8524b-109">Configurare la modalità del codec vocale su "mixed" impostando la proprietà [MFPKEY \_ WMAVOICE \_ enc \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) su 2.</span><span class="sxs-lookup"><span data-stu-id="8524b-109">Configure the mode of the voice codec to "mixed" by setting the [MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) property to 2.</span></span> <span data-ttu-id="8524b-110">Impostare EDL usando la proprietà [MFPKEY \_ WMAVOICE \_ enc \_ EDL](mfpkey-wmavoice-enc-edlproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="8524b-110">Set the EDL using the [MFPKEY\_WMAVOICE\_ENC\_EDL](mfpkey-wmavoice-enc-edlproperty.md) property.</span></span> <span data-ttu-id="8524b-111">Il valore di questa proprietà è una stringa contenente un elenco delimitato da virgole degli intervalli di tempo nel contenuto che deve essere codificato come musica.</span><span class="sxs-lookup"><span data-stu-id="8524b-111">The value of this property is a string containing a comma-delimited list of the time ranges in the content that should be encoded as music.</span></span> <span data-ttu-id="8524b-112">Il primo elemento dell'elenco è la versione di EDL, che è sempre 1.</span><span class="sxs-lookup"><span data-stu-id="8524b-112">The first item in the list is the version of the EDL, which is always 1.</span></span> <span data-ttu-id="8524b-113">Il secondo elemento è il numero di sezioni di musica descritte nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="8524b-113">The second item is the number of music sections described in the list.</span></span> <span data-ttu-id="8524b-114">Il secondo elemento è un numero di coppie di valori uguale al secondo elemento; ogni coppia di valori descrive il punto iniziale e finale di un passaggio di musica nel contenuto, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="8524b-114">Following the second item are a number of pairs of values equal to the second item; each pair of values describes the starting and ending point of a music passage in the content, in milliseconds.</span></span>

<span data-ttu-id="8524b-115">Ad esempio, la stringa EDL "1, 4, 1000, 2000, 5000, 6000, 9000, 10000, 13000, 14000" specifica quattro passaggi musicali, ognuno dei quali è un secondo lungo.</span><span class="sxs-lookup"><span data-stu-id="8524b-115">For example, the EDL string "1, 4, 1000, 2000, 5000, 6000, 9000, 10000, 13000, 14000" specifies four musical passages, each of which is one second long.</span></span> <span data-ttu-id="8524b-116">Se le informazioni nella stringa EDL non sono valide, verranno ignorate.</span><span class="sxs-lookup"><span data-stu-id="8524b-116">If the information in the EDL string is invalid, it is ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8524b-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8524b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8524b-118">Uso del codec Windows Media Audio 9 Voice</span><span class="sxs-lookup"><span data-stu-id="8524b-118">Using the Windows Media Audio 9 Voice Codec</span></span>](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[<span data-ttu-id="8524b-119">Utilizzo di audio</span><span class="sxs-lookup"><span data-stu-id="8524b-119">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



