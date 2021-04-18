---
description: "Affinché un'applicazione Tablet PC funzioni con l'input penna in modo efficace, l'applicazione deve essere in grado di:"
ms.assetid: 64a7b773-35c9-42f7-aec4-7fed34fa84d9
title: Scenari di interoperabilità importanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6dca3bcbf52d673131122615fa5a08317dbf10c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306062"
---
# <a name="important-interoperability-scenarios"></a><span data-ttu-id="33eb7-103">Scenari di interoperabilità importanti</span><span class="sxs-lookup"><span data-stu-id="33eb7-103">Important Interoperability Scenarios</span></span>

<span data-ttu-id="33eb7-104">Affinché un'applicazione Tablet PC funzioni con l'input penna in modo efficace, l'applicazione deve essere in grado di:</span><span class="sxs-lookup"><span data-stu-id="33eb7-104">For a Tablet PC application to operate with ink effectively, that application should be able to:</span></span>

-   <span data-ttu-id="33eb7-105">Salvare un documento nel formato binario nativo dell'applicazione senza perdere l'input penna del documento.</span><span class="sxs-lookup"><span data-stu-id="33eb7-105">Save a document in the application's native binary format without losing the document's ink.</span></span>
-   <span data-ttu-id="33eb7-106">Salvare un documento in qualsiasi formato supportato normalmente dall'applicazione, ad esempio HTML o RTF (Rich Text Format) senza perdere l'input penna del documento.</span><span class="sxs-lookup"><span data-stu-id="33eb7-106">Save a document in any format the application normally supports (for example, HTML or Rich Text Format (RTF)) without losing the document's ink.</span></span>
-   <span data-ttu-id="33eb7-107">Copiare l'input penna da un'applicazione a un'altra usando gli Appunti.</span><span class="sxs-lookup"><span data-stu-id="33eb7-107">Copy ink from one application to another by using the Clipboard.</span></span> <span data-ttu-id="33eb7-108">Questa operazione funziona se l'altra applicazione riconosce solo un formato specifico, ad esempio HTML, RTF o bitmap (BMP).</span><span class="sxs-lookup"><span data-stu-id="33eb7-108">This works if the other application only recognizes a specific format, such as HTML, RTF, or bitmap (BMP).</span></span> <span data-ttu-id="33eb7-109">Funziona anche se l'applicazione di destinazione riconosce l'input penna.</span><span class="sxs-lookup"><span data-stu-id="33eb7-109">It also works whether the destination application recognizes ink.</span></span> <span data-ttu-id="33eb7-110">Se riconosce l'input penna, l'applicazione di destinazione è in grado di interpretare l'input penna copiato come input penna e non solo come immagine.</span><span class="sxs-lookup"><span data-stu-id="33eb7-110">If it does recognize ink, the destination application is able to interpret the ink that has been copied as ink and not just as an image.</span></span>
-   <span data-ttu-id="33eb7-111">Copiare l'input penna, insieme al testo, tra due applicazioni che riconoscono l'input penna, ognuna delle quali contiene più di un oggetto [**input penna**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="33eb7-111">Copy ink, along with text, between two applications that recognize ink, each of which has more than one [**Ink**](inkdisp-class.md) object.</span></span> <span data-ttu-id="33eb7-112">Questa operazione richiede un formato HTML, RTF o simile.</span><span class="sxs-lookup"><span data-stu-id="33eb7-112">This requires HTML, RTF, or a similar format.</span></span>
-   <span data-ttu-id="33eb7-113">Copiare l'input penna tra due applicazioni, ognuna con un oggetto [**input penna**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="33eb7-113">Copy ink between two applications, each of which has one [**Ink**](inkdisp-class.md) object.</span></span> <span data-ttu-id="33eb7-114">Il formato ISF (Ink Serialized Format) è sufficiente per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="33eb7-114">Ink Serialized Format (ISF) is sufficient for this.</span></span>
-   <span data-ttu-id="33eb7-115">Copiare l'input penna da un'applicazione che dispone di più di un oggetto [**input penna**](inkdisp-class.md) in un'applicazione che dispone di un solo oggetto **input penna** .</span><span class="sxs-lookup"><span data-stu-id="33eb7-115">Copy ink from an application that has more than one [**Ink**](inkdisp-class.md) object to an application that has only one **Ink** object.</span></span> <span data-ttu-id="33eb7-116">In questo caso, l'applicazione con più di un oggetto **input penna** deve essere in grado di produrre il formato ISF (Ink Serialized Format).</span><span class="sxs-lookup"><span data-stu-id="33eb7-116">In this case, the application that has more than one **Ink** object must be able to produce Ink Serialized Format (ISF).</span></span>
-   <span data-ttu-id="33eb7-117">Copiare l'input penna da un'applicazione che dispone di un oggetto [**input penna**](inkdisp-class.md) in un'applicazione con più di un oggetto **input penna** .</span><span class="sxs-lookup"><span data-stu-id="33eb7-117">Copy ink from an application that has one [**Ink**](inkdisp-class.md) object to an application that has more than one **Ink** object.</span></span> <span data-ttu-id="33eb7-118">In questo caso, l'applicazione che dispone di più di un oggetto **Ink** deve essere in grado di riconoscere ISF.</span><span class="sxs-lookup"><span data-stu-id="33eb7-118">In this case, the application that has more than one **Ink** object must be able to recognize ISF.</span></span>

 

 



