---
description: Gli oggetti flusso sono un'astrazione del flusso multimediale o dei flussi associati a una sessione di chiamata.
ms.assetid: 4bd7a305-69ff-4892-bf03-df9c6479adab
title: Oggetti Stream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeb89dbacf73baaffbca9aa3791aa73937a69e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314128"
---
# <a name="stream-objects"></a><span data-ttu-id="b56dd-103">Oggetti Stream</span><span class="sxs-lookup"><span data-stu-id="b56dd-103">Stream Objects</span></span>

<span data-ttu-id="b56dd-104">Gli oggetti flusso sono un'astrazione del flusso multimediale o dei flussi associati a una sessione di chiamata.</span><span class="sxs-lookup"><span data-stu-id="b56dd-104">Stream objects are an abstraction of the media stream or streams associated with a call session.</span></span> <span data-ttu-id="b56dd-105">Le interfacce e i metodi esposti negli oggetti flusso e sottoflusso consentono a un'applicazione di eseguire controlli molto dettagliati, ad esempio la sospensione di un flusso, l'aggiunta di nuovi tipi di supporti a una sessione di comunicazione o la modifica del volume audio di un particolare partecipante della conferenza.</span><span class="sxs-lookup"><span data-stu-id="b56dd-105">The interfaces and methods exposed on stream and substream objects allow an application to exercise very detailed controls such as pausing a stream, adding new media types to a communications session, or adjusting the audio volume of a particular conference participant.</span></span>

<span data-ttu-id="b56dd-106">I due tipi principali di flusso sono il flusso e il sottoflusso.</span><span class="sxs-lookup"><span data-stu-id="b56dd-106">The two main types of stream are the stream and the substream.</span></span> <span data-ttu-id="b56dd-107">Le interfacce e i metodi di un'implementazione standard sono simili per entrambi, ma il sottoflusso consente un livello di controllo più basso.</span><span class="sxs-lookup"><span data-stu-id="b56dd-107">The interfaces and methods of a standard implementation are similar for both, but substreaming allowing a lower level of control.</span></span> <span data-ttu-id="b56dd-108">Tutti i provider di servizi multimediali (MSPs) devono implementare le interfacce di controllo del flusso di base, ma il supporto per i flussi sottoflussi è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b56dd-108">All media service providers (MSPs) must implement the basic stream control interfaces, but support for substreams is optional.</span></span>

<span data-ttu-id="b56dd-109">Alcuni provider di servizi implementano inoltre [interfacce specifiche del provider](provider-specific-interfaces.md) per i flussi.</span><span class="sxs-lookup"><span data-stu-id="b56dd-109">In addition, some service providers implement [provider-specific interfaces](provider-specific-interfaces.md) for streams.</span></span> <span data-ttu-id="b56dd-110">Ad esempio, l'MSP IPConf fornisce controlli a livello di partecipante.</span><span class="sxs-lookup"><span data-stu-id="b56dd-110">For example, the IPConf MSP provides participant level controls.</span></span> <span data-ttu-id="b56dd-111">Per un riepilogo, vedere [IPConf msp Interfaces](ipconf-msp-interfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="b56dd-111">See [IPConf MSP Interfaces](ipconf-msp-interfaces.md) for a summary.</span></span> <span data-ttu-id="b56dd-112">Per altre interfacce che potrebbero essere implementate, vedere la documentazione del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="b56dd-112">For other interfaces that might be implemented, see the service provider's documentation.</span></span>

<span data-ttu-id="b56dd-113">MSP e TAPI creano oggetti flusso per una chiamata durante la configurazione iniziale di una sessione in uscita o in ingresso.</span><span class="sxs-lookup"><span data-stu-id="b56dd-113">The MSP and TAPI create stream objects for a call during initial setup of an outgoing or incoming session.</span></span> <span data-ttu-id="b56dd-114">L'applicazione è responsabile dell'identificazione dei terminali appropriati per questi flussi e della selezione dei terminali sui flussi.</span><span class="sxs-lookup"><span data-stu-id="b56dd-114">The application is responsible for identifying appropriate terminals for these streams, and selecting the terminals onto the streams.</span></span>

<span data-ttu-id="b56dd-115">Si noti che in alcuni casi un MSP potrebbe richiedere che l'applicazione arresti o sospenda i flussi prima di determinate operazioni della sessione di chiamata.</span><span class="sxs-lookup"><span data-stu-id="b56dd-115">Note that in some cases an MSP may require that the application stop or pause streams prior to certain call session operations.</span></span>

<span data-ttu-id="b56dd-116">Le interfacce di flusso sono documentate nel [riferimento MSPI (Media Service Provider Interface)](media-service-provider-interface-mspi-reference.md).</span><span class="sxs-lookup"><span data-stu-id="b56dd-116">The stream interfaces are documented in the [Media Service Provider Interface (MSPI) Reference](media-service-provider-interface-mspi-reference.md).</span></span>

<span data-ttu-id="b56dd-117">L'esempio [Select a Terminal](select-a-terminal.md) Code Mostra un esempio di enumerazione dei flussi e selezione di terminali su di essi.</span><span class="sxs-lookup"><span data-stu-id="b56dd-117">The [Select a Terminal](select-a-terminal.md) code example shows an example of enumerating streams and selecting terminals onto them.</span></span>

 

 



