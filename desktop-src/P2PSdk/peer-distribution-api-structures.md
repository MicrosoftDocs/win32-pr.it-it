---
description: Il servizio distribuzione peer Microsoft supporta le seguenti strutture.
ms.assetid: 26badfe6-3a5a-4c2e-9ef1-534c2e8573d0
title: Strutture dell'API di distribuzione peer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc9fbf86c242406aa86b7dd30497ba4c5085488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312250"
---
# <a name="peer-distribution-api-structures"></a><span data-ttu-id="250aa-103">Strutture dell'API di distribuzione peer</span><span class="sxs-lookup"><span data-stu-id="250aa-103">Peer Distribution API Structures</span></span>

<span data-ttu-id="250aa-104">Il servizio distribuzione peer Microsoft supporta le seguenti strutture.</span><span class="sxs-lookup"><span data-stu-id="250aa-104">The Microsoft Peer Distribution service supports the following structures.</span></span>



| <span data-ttu-id="250aa-105">Struttura</span><span class="sxs-lookup"><span data-stu-id="250aa-105">Structure</span></span>                                                              | <span data-ttu-id="250aa-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="250aa-106">Description</span></span>                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="250aa-107">**\_informazioni di \_ base sul client PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="250aa-107">**PEERDIST\_CLIENT\_BASIC\_INFO**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_client_basic_info)    | <span data-ttu-id="250aa-108">Indica se sono presenti numerosi client che scaricano simultaneamente lo stesso contenuto.</span><span class="sxs-lookup"><span data-stu-id="250aa-108">Indicates whether or not there are many clients simultaneously downloading the same content.</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="250aa-109">**\_tag di contenuto PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="250aa-109">**PEERDIST\_CONTENT\_TAG**</span></span>](/windows/win32/api/peerdist/ns-peerdist-peerdist_content_tag)                 | <span data-ttu-id="250aa-110">Contiene un tag fornito dal client che è un valore di input per [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent).</span><span class="sxs-lookup"><span data-stu-id="250aa-110">Contains a client supplied tag which is an input value for [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent).</span></span> <span data-ttu-id="250aa-111">Il tag è associato al segmento di contenuto e viene usato nelle API di gestione del contenuto, ad esempio [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent).</span><span class="sxs-lookup"><span data-stu-id="250aa-111">The tag is associated with the content segment and is used in content management APIs, like [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent).</span></span> |
| [<span data-ttu-id="250aa-112">**\_Opzioni di pubblicazione PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="250aa-112">**PEERDIST\_PUBLICATION\_OPTIONS**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_publication_options) | <span data-ttu-id="250aa-113">Contiene le opzioni di pubblicazione, incluse le informazioni sulla versione dell'API e i flag di opzione possibili.</span><span class="sxs-lookup"><span data-stu-id="250aa-113">Contains publication options, including the API version information and possible option flags.</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="250aa-114">**\_Opzioni di recupero \_ peer**</span><span class="sxs-lookup"><span data-stu-id="250aa-114">**PEER\_RETRIEVAL\_OPTIONS**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_retrieval_options)         | <span data-ttu-id="250aa-115">Contiene la versione delle informazioni sul contenuto da recuperare.</span><span class="sxs-lookup"><span data-stu-id="250aa-115">Contains version of the content information to retrieve.</span></span>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="250aa-116">**\_informazioni sullo stato di PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="250aa-116">**PEERDIST\_STATUS\_INFO**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_status_info)                 | <span data-ttu-id="250aa-117">Contiene informazioni sullo stato corrente e sulle funzionalità del servizio BranchCache nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="250aa-117">Contains information about the current status and capabilities of the BranchCache service on the local computer.</span></span>                                                                                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="250aa-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="250aa-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="250aa-119">Riferimento all'API di distribuzione peer</span><span class="sxs-lookup"><span data-stu-id="250aa-119">Peer Distribution API Reference</span></span>](peer-distribution-api-reference.md)
</dt> </dl>

 

 



