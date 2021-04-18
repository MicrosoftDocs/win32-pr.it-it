---
description: Questa sezione illustra in dettaglio la versione binaria del formato di file DirectX (. x), come introdotto con la versione di DirectX 3,0.
ms.assetid: d1b6698f-72bd-40a4-a501-c2093cd940f6
title: Codifica binaria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56937b54be82e36d6ff18aab2a2349be6d59cc12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304550"
---
# <a name="binary-encoding"></a><span data-ttu-id="5ba35-103">Codifica binaria</span><span class="sxs-lookup"><span data-stu-id="5ba35-103">Binary Encoding</span></span>

<span data-ttu-id="5ba35-104">Questa sezione illustra in dettaglio la versione binaria del formato di file DirectX (. x), come introdotto con la versione di DirectX 3,0.</span><span class="sxs-lookup"><span data-stu-id="5ba35-104">This section details the binary version of the DirectX (.x) file format as introduced with the release of DirectX 3.0.</span></span>

<span data-ttu-id="5ba35-105">Il formato binario è una rappresentazione in formato token del formato di testo.</span><span class="sxs-lookup"><span data-stu-id="5ba35-105">The binary format is a tokenized representation of the text format.</span></span> <span data-ttu-id="5ba35-106">I token possono essere autonomi o accompagnati da record di dati primitivi.</span><span class="sxs-lookup"><span data-stu-id="5ba35-106">Tokens can be stand-alone or accompanied by primitive data records.</span></span> <span data-ttu-id="5ba35-107">I token autonomi offrono la struttura grammaticale e i token che portano a record forniscono i dati necessari.</span><span class="sxs-lookup"><span data-stu-id="5ba35-107">Stand-alone tokens give grammatical structure, and record-bearing tokens supply the necessary data.</span></span>

<span data-ttu-id="5ba35-108">Si noti che tutti i dati vengono archiviati in formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="5ba35-108">Note that all data is stored in little-endian format.</span></span> <span data-ttu-id="5ba35-109">Un flusso di dati binari validi è costituito da un'intestazione seguita da modelli e/o oggetti dati.</span><span class="sxs-lookup"><span data-stu-id="5ba35-109">A valid binary data stream consists of a header followed by templates and/or data objects.</span></span>

<span data-ttu-id="5ba35-110">In questa sezione vengono illustrati i componenti seguenti del formato di file binario e vengono forniti un modello di esempio e un oggetto dati binario.</span><span class="sxs-lookup"><span data-stu-id="5ba35-110">This section discusses the following components of the binary file format and provides an example template and binary data object.</span></span>

-   [<span data-ttu-id="5ba35-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5ba35-111">Header</span></span>](header.md)
-   [<span data-ttu-id="5ba35-112">Tokens</span><span class="sxs-lookup"><span data-stu-id="5ba35-112">Tokens</span></span>](tokens.md)
-   [<span data-ttu-id="5ba35-113">Record di token</span><span class="sxs-lookup"><span data-stu-id="5ba35-113">Token Records</span></span>](token-records.md)
-   [<span data-ttu-id="5ba35-114">Modelli</span><span class="sxs-lookup"><span data-stu-id="5ba35-114">Templates</span></span>](dx9-graphics-reference-x-file-binaryencoding-templates.md)
-   [<span data-ttu-id="5ba35-115">Dati</span><span class="sxs-lookup"><span data-stu-id="5ba35-115">Data</span></span>](dx9-graphics-reference-x-file-binaryencoding-data.md)
-   [<span data-ttu-id="5ba35-116">esempi</span><span class="sxs-lookup"><span data-stu-id="5ba35-116">Examples</span></span>](examples.md)

## <a name="related-topics"></a><span data-ttu-id="5ba35-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5ba35-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ba35-118">Riferimento al formato di file X</span><span class="sxs-lookup"><span data-stu-id="5ba35-118">X File Format Reference</span></span>](dx9-graphics-reference-x-file-format.md)
</dt> </dl>

 

 



