---
title: Riferimento al plug-in
description: Funzioni di adapter, funzioni wrapper e strutture per la creazione di adattatori plug-in personalizzati di tre tipi di motore, sensore e archiviazione.
ms.assetid: 1886c389-b914-4b2d-ab7e-3e163782673d
keywords:
- API Windows Biometric Framework API di Windows Biometric Framework, informazioni di riferimento sul plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc764be98f6417d211effe1c182279d54c95d234
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471702"
---
# <a name="plug-in-reference"></a><span data-ttu-id="cfd55-104">Riferimento al plug-in</span><span class="sxs-lookup"><span data-stu-id="cfd55-104">Plug-in Reference</span></span>

<span data-ttu-id="cfd55-105">I dispositivi biometrici sono prodotti in un'ampia gamma di tipi e configurazioni.</span><span class="sxs-lookup"><span data-stu-id="cfd55-105">Biometric devices are manufactured in a wide variety of types and configurations.</span></span> <span data-ttu-id="cfd55-106">Nel Windows Biometric Framework è incorporata un'architettura estendibile che consente di gestire questa varietà creando plug-in personalizzati. Al centro di questa architettura è presente un oggetto software denominato unità biometrica.</span><span class="sxs-lookup"><span data-stu-id="cfd55-106">The Windows Biometric Framework incorporates an extensible architecture that enables you to deal with this variety by creating custom plug-ins. At the center of this architecture is a software object called a biometric unit.</span></span> <span data-ttu-id="cfd55-107">È possibile considerare un'unità biometrica come un'astrazione che rappresenta un dispositivo biometrico per il Framework.</span><span class="sxs-lookup"><span data-stu-id="cfd55-107">You can think of a biometric unit as an abstraction that represents a biometric device to the Framework.</span></span> <span data-ttu-id="cfd55-108">I componenti del software plug-in denominati adapter consentono di connettere l'unità biometrica all'hardware associato.</span><span class="sxs-lookup"><span data-stu-id="cfd55-108">Plug-in software components called adapters connect the biometric unit to the associated hardware.</span></span> <span data-ttu-id="cfd55-109">Sono disponibili tre tipi di adapter che è possibile creare.</span><span class="sxs-lookup"><span data-stu-id="cfd55-109">There are three types of adapters that you can create.</span></span> <span data-ttu-id="cfd55-110">Un adattatore del motore genera modelli biometrici dagli esempi acquisiti, associa gli esempi ai modelli esistenti e indicizza i modelli.</span><span class="sxs-lookup"><span data-stu-id="cfd55-110">An engine adapter generates biometric templates from captured samples, matches samples to existing templates, and indexes templates.</span></span> <span data-ttu-id="cfd55-111">Un adattatore del sensore esegue il wrapping di un dispositivo biometrico e fornisce un'interfaccia standard per la configurazione del sensore, l'acquisizione di esempi e il controllo del flusso di dati biometrici nel motore di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="cfd55-111">A sensor adapter wraps a biometric device and provides a standard interface for configuring the sensor, capturing samples, and controlling the flow of biometric data to the processing engine.</span></span> <span data-ttu-id="cfd55-112">Un adattatore di archiviazione gestisce i database modello.</span><span class="sxs-lookup"><span data-stu-id="cfd55-112">A storage adapter manages template databases.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cfd55-113">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="cfd55-113">In this section</span></span>



| <span data-ttu-id="cfd55-114">Argomento</span><span class="sxs-lookup"><span data-stu-id="cfd55-114">Topic</span></span>                                                                 | <span data-ttu-id="cfd55-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cfd55-115">Description</span></span>                                                                                                                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cfd55-116">Funzioni plug-in</span><span class="sxs-lookup"><span data-stu-id="cfd55-116">Plug-in Functions</span></span>](plug-in-functions.md)<br/>                 | <span data-ttu-id="cfd55-117">Funzioni che è possibile utilizzare per creare i plug-in di adapter che costituiscono un'unità biometrica.</span><span class="sxs-lookup"><span data-stu-id="cfd55-117">Functions you can use to create the adapter plug-ins that make up a biometric unit.</span></span><br/>                                                                     |
| [<span data-ttu-id="cfd55-118">Strutture di plug-in</span><span class="sxs-lookup"><span data-stu-id="cfd55-118">Plug-in Structures</span></span>](plug-in-structures.md)<br/>               | <span data-ttu-id="cfd55-119">Strutture per lo sviluppo di applicazioni client da parte dell'API Windows Biometric Framework.</span><span class="sxs-lookup"><span data-stu-id="cfd55-119">Structures for client application development by the Windows Biometric Framework API.</span></span><br/>                                                                   |
| [<span data-ttu-id="cfd55-120">Funzioni wrapper plug-in</span><span class="sxs-lookup"><span data-stu-id="cfd55-120">Plug-in Wrapper Functions</span></span>](plug-in-wrapper-functions.md)<br/> | <span data-ttu-id="cfd55-121">Funzioni wrapper che consentono di chiamare una funzione pubblica su qualsiasi Adapter collegato alla pipeline senza acquisire manualmente un puntatore all'adapter.</span><span class="sxs-lookup"><span data-stu-id="cfd55-121">Wrapper functions that allow you to call a public function on any adapter attached to the pipeline without manually acquiring a pointer to the adapter.</span></span><br/> |



 

 

 





