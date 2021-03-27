---
title: Interfacce della versione comuni
description: Questa sezione contiene informazioni sulle interfacce della versione comuni di.
ms.assetid: d228c3c2-e2ff-4723-aec1-5c3ce82c321d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f535650fa24593cc4b663c1a2b01a1a2d53a9b3b
ms.sourcegitcommit: 8f833c83be1accc119cc57e67b608ffe1e0159b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/07/2020
ms.locfileid: "103734682"
---
# <a name="common-version-interfaces"></a><span data-ttu-id="7e79e-103">Interfacce della versione comuni</span><span class="sxs-lookup"><span data-stu-id="7e79e-103">Common version interfaces</span></span>

<span data-ttu-id="7e79e-104">Questa sezione contiene informazioni sulle interfacce della versione comuni di.</span><span class="sxs-lookup"><span data-stu-id="7e79e-104">This section contains information about the common version interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7e79e-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="7e79e-105">In this section</span></span>

| <span data-ttu-id="7e79e-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="7e79e-106">Topic</span></span> | <span data-ttu-id="7e79e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e79e-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="7e79e-108">**ID3D10Blob**</span><span class="sxs-lookup"><span data-stu-id="7e79e-108">**ID3D10Blob**</span></span>](/windows/win32/api/d3dcommon/nn-d3dcommon-id3d10blob) | <span data-ttu-id="7e79e-109">Questa interfaccia viene utilizzata per restituire dati di lunghezza arbitraria.</span><span class="sxs-lookup"><span data-stu-id="7e79e-109">This interface is used to return arbitrary-length data.</span></span> |
| <span data-ttu-id="7e79e-110">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e79e-110">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span></span> | <span data-ttu-id="7e79e-111">Questa interfaccia viene utilizzata per restituire dati di lunghezza arbitraria.</span><span class="sxs-lookup"><span data-stu-id="7e79e-111">This interface is used to return data of arbitrary length.</span></span> |
| [<span data-ttu-id="7e79e-112">**ID3DDestructionNotifier**</span><span class="sxs-lookup"><span data-stu-id="7e79e-112">**ID3DDestructionNotifier**</span></span>](/windows/win32/api/d3dcommon/nn-d3dcommon-id3ddestructionotifier) | <span data-ttu-id="7e79e-113">Usato per la registrazione per i callback quando un oggetto Nano-COM 3D diretto viene eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="7e79e-113">Used to register for callbacks when a Direct 3D nano-COM object is destroyed.</span></span> |
| [<span data-ttu-id="7e79e-114">**ID3DInclude**</span><span class="sxs-lookup"><span data-stu-id="7e79e-114">**ID3DInclude**</span></span>](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) | <span data-ttu-id="7e79e-115">[**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) è un'interfaccia di inclusione implementata dall'utente per consentire a un'applicazione di chiamare metodi sottoponibili a override dell'utente per l'apertura e la chiusura di \# file di inclusione dello shader.</span><span class="sxs-lookup"><span data-stu-id="7e79e-115">[**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) is an include interface that the user implements to allow an application to call user-overridable methods for opening and closing shader \#include files.</span></span> |
| [<span data-ttu-id="7e79e-116">**ID3DUserDefinedAnnotation**</span><span class="sxs-lookup"><span data-stu-id="7e79e-116">**ID3DUserDefinedAnnotation**</span></span>](/windows/desktop/api/D3D11_1/nn-d3d11_1-id3duserdefinedannotation) | <span data-ttu-id="7e79e-117">L'interfaccia [**ID3DUserDefinedAnnotation**](/windows/desktop/api/D3D11_1/nn-d3d11_1-id3duserdefinedannotation) consente a un'applicazione di descrivere le sezioni concettuali e i marcatori all'interno del flusso del codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7e79e-117">The [**ID3DUserDefinedAnnotation**](/windows/desktop/api/D3D11_1/nn-d3d11_1-id3duserdefinedannotation) interface enables an application to describe conceptual sections and markers within the application's code flow.</span></span> <span data-ttu-id="7e79e-118">Uno strumento abilitato in modo appropriato, ad esempio Microsoft Visual Studio Ultimate 2012, può visualizzare queste sezioni e marcatori visivamente lungo la linea temporale Microsoft Direct3D dello strumento, mentre lo strumento esegue il debug dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7e79e-118">An appropriately enabled tool, such as Microsoft Visual Studio Ultimate 2012, can display these sections and markers visually along the tool's Microsoft Direct3D time line, while the tool debugs the application.</span></span> <span data-ttu-id="7e79e-119">Queste note visive consentono agli utenti di tale strumento di passare alle parti della linea temporale di interesse o di comprendere il set di chiamate Direct3D prodotte da alcune sezioni del codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7e79e-119">These visual notes allow users of such a tool to navigate to parts of the time line that are of interest, or to understand what set of Direct3D calls are produced by certain sections of the application's code.</span></span> |

## <a name="related-topics"></a><span data-ttu-id="7e79e-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7e79e-120">Related topics</span></span>

[<span data-ttu-id="7e79e-121">Riferimento alla versione comune</span><span class="sxs-lookup"><span data-stu-id="7e79e-121">Common version reference</span></span>](d3d11-graphics-reference-d3d11-common.md)
