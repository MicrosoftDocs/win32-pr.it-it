---
title: Funzioni di sicurezza
description: Le funzioni di sicurezza di gestione della rete ottengono e impostano i descrittori di sicurezza per le radici autonome e basate su dominio DFS.
ms.assetid: 90860842-0f4d-49ad-b835-50305328a050
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f717ff3f5701e507087fcdac164d9357f2505a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483845"
---
# <a name="security-functions"></a><span data-ttu-id="18df7-103">Funzioni di sicurezza</span><span class="sxs-lookup"><span data-stu-id="18df7-103">Security Functions</span></span>

<span data-ttu-id="18df7-104">Le funzioni di sicurezza di gestione della rete ottengono e impostano i descrittori di sicurezza per le radici autonome e basate su dominio DFS.</span><span class="sxs-lookup"><span data-stu-id="18df7-104">The network management security functions get and set security descriptors for DFS domain-based and stand-alone roots.</span></span>

<span data-ttu-id="18df7-105">Le funzioni di sicurezza DFS sono elencate di seguito.</span><span class="sxs-lookup"><span data-stu-id="18df7-105">The DFS security functions are listed following.</span></span>

| <span data-ttu-id="18df7-106">Funzione</span><span class="sxs-lookup"><span data-stu-id="18df7-106">Function</span></span>                                                               | <span data-ttu-id="18df7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18df7-107">Description</span></span>                                                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="18df7-108">**NetDfsGetSecurity**</span><span class="sxs-lookup"><span data-stu-id="18df7-108">**NetDfsGetSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)                         | <span data-ttu-id="18df7-109">Ottiene il descrittore di sicurezza per l'oggetto radice della radice DFS specificata.</span><span class="sxs-lookup"><span data-stu-id="18df7-109">Obtains the security descriptor for the root object of the specified DFS root.</span></span>                                       |
| [<span data-ttu-id="18df7-110">**NetDfsSetSecurity**</span><span class="sxs-lookup"><span data-stu-id="18df7-110">**NetDfsSetSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)                         | <span data-ttu-id="18df7-111">Individua l'oggetto radice per la radice DFS specificata e imposta il descrittore di sicurezza fornito.</span><span class="sxs-lookup"><span data-stu-id="18df7-111">Locates the root object for the specified DFS root and sets the supplied security descriptor on it.</span></span>                  |
| [<span data-ttu-id="18df7-112">**NetDfsGetStdContainerSecurity**</span><span class="sxs-lookup"><span data-stu-id="18df7-112">**NetDfsGetStdContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity) | <span data-ttu-id="18df7-113">Ottiene il descrittore di sicurezza per l'oggetto contenitore della radice autonoma DFS specificata.</span><span class="sxs-lookup"><span data-stu-id="18df7-113">Obtains the security descriptor for the container object of the specified DFS stand-alone root.</span></span>                      |
| [<span data-ttu-id="18df7-114">**NetDfsSetStdContainerSecurity**</span><span class="sxs-lookup"><span data-stu-id="18df7-114">**NetDfsSetStdContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity) | <span data-ttu-id="18df7-115">Individua l'oggetto contenitore per la radice autonoma DFS specificata e imposta il descrittore di sicurezza fornito.</span><span class="sxs-lookup"><span data-stu-id="18df7-115">Locates the container object for the specified DFS stand-alone root and sets the supplied security descriptor on it.</span></span> |
| [<span data-ttu-id="18df7-116">**NetDfsGetFtContainerSecurity**</span><span class="sxs-lookup"><span data-stu-id="18df7-116">**NetDfsGetFtContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)   | <span data-ttu-id="18df7-117">Ottiene il descrittore di sicurezza per l'oggetto contenitore della radice del dominio DFS specificata.</span><span class="sxs-lookup"><span data-stu-id="18df7-117">Obtains the security descriptor for the container object of the specified DFS domain root.</span></span>                           |
| [<span data-ttu-id="18df7-118">**NetDfsSetFtContainerSecurity**</span><span class="sxs-lookup"><span data-stu-id="18df7-118">**NetDfsSetFtContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)   | <span data-ttu-id="18df7-119">Individua l'oggetto contenitore per la radice del dominio DFS specificata e imposta il descrittore di sicurezza fornito.</span><span class="sxs-lookup"><span data-stu-id="18df7-119">Locates the container object for the specified DFS domain root and sets the supplied security descriptor on it.</span></span>      |
