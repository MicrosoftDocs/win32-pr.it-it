---
description: Resolver di origine
ms.assetid: 93eecf10-308b-4bb4-92f9-fd32d6ecdb04
title: Resolver di origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a844893b0348546d4fd174b0b24405812efcef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344381"
---
# <a name="source-resolver"></a><span data-ttu-id="4cca8-103">Resolver di origine</span><span class="sxs-lookup"><span data-stu-id="4cca8-103">Source Resolver</span></span>

<span data-ttu-id="4cca8-104">Il resolver dell'origine accetta un URL o un flusso di byte e crea l'origine multimediale appropriata per il contenuto.</span><span class="sxs-lookup"><span data-stu-id="4cca8-104">The source resolver takes a URL or byte stream and creates the appropriate media source for that content.</span></span> <span data-ttu-id="4cca8-105">Il resolver dell'origine rappresenta il modo standard per la creazione di origini multimediali da parte delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="4cca8-105">The source resolver is the standard way for the applications to create media sources.</span></span>

<span data-ttu-id="4cca8-106">Internamente, il resolver di origine utilizza gli oggetti *gestore* :</span><span class="sxs-lookup"><span data-stu-id="4cca8-106">Internally, the source resolver uses *handler* objects:</span></span>

-   <span data-ttu-id="4cca8-107">I *gestori dello schema* accettano un URL e creano un'origine multimediale o un flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="4cca8-107">*Scheme handlers* take a URL and create a media source or a byte stream.</span></span>
-   <span data-ttu-id="4cca8-108">I *gestori del flusso di byte* accettano un flusso di byte e creano un'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="4cca8-108">*Byte stream handlers* take a byte stream and create a media source.</span></span>

<span data-ttu-id="4cca8-109">È possibile implementare un gestore personalizzato e aggiungerlo al registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4cca8-109">You can implement a custom handler and add it to the registry.</span></span> <span data-ttu-id="4cca8-110">I gestori dello schema sono registrati dallo schema URL e i gestori del flusso di byte sono registrati dall'estensione del nome file o dal tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="4cca8-110">Scheme handlers are registered by URL scheme, and byte stream handlers are registered by file name extension or MIME type.</span></span>

<span data-ttu-id="4cca8-111">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="4cca8-111">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="4cca8-112">Uso del resolver di origine</span><span class="sxs-lookup"><span data-stu-id="4cca8-112">Using the Source Resolver</span></span>](using-the-source-resolver.md)
-   [<span data-ttu-id="4cca8-113">Configurazione di un'origine multimediale</span><span class="sxs-lookup"><span data-stu-id="4cca8-113">Configuring a Media Source</span></span>](configuring-a-media-source.md)
-   [<span data-ttu-id="4cca8-114">Gestori di schemi e gestori di Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="4cca8-114">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)

## <a name="related-topics"></a><span data-ttu-id="4cca8-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4cca8-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cca8-116">Origini supporti</span><span class="sxs-lookup"><span data-stu-id="4cca8-116">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 



