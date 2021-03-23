---
title: Uso di Direct3D 11, Direct3D 10 e Direct2D
description: Questa sezione illustra le tecniche di interoperabilità con le versioni precedenti di Direct3D e Direct2D, l'API Direct3D 11on12 e le linee guida per il porting da Direct3D 11 a Direct3D 12.
ms.assetid: 1AB98335-30B1-4244-B244-F8573524B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b200da0708b9b990b102a77867669217318f1d67
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103725"
---
# <a name="working-with-direct3d-11-direct3d-10-and-direct2d"></a><span data-ttu-id="e748e-103">Uso di Direct3D 11, Direct3D 10 e Direct2D</span><span class="sxs-lookup"><span data-stu-id="e748e-103">Working with Direct3D 11, Direct3D 10 and Direct2D</span></span>

<span data-ttu-id="e748e-104">Questa sezione illustra le tecniche di interoperabilità con le versioni precedenti di Direct3D e Direct2D, l'API Direct3D 11on12 e le linee guida per il porting da Direct3D 11 a Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="e748e-104">This section covers interop techniques with earlier versions of Direct3D and Direct2D, the Direct3D 11on12 API, and porting guidelines from Direct3D 11 to Direct3D 12.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e748e-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="e748e-105">In this section</span></span>



| <span data-ttu-id="e748e-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="e748e-106">Topic</span></span>                                                                                             | <span data-ttu-id="e748e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e748e-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e748e-108">Interoperabilità di Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e748e-108">Direct3D 12 Interop</span></span>](direct3d-12-with-direct3d-11--direct-2d-and-gdi.md)<br/>             | <span data-ttu-id="e748e-109">D3D12 può essere usato per scrivere applicazioni con componenti.</span><span class="sxs-lookup"><span data-stu-id="e748e-109">D3D12 can be used to write componentized applications.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="e748e-110">D3D11On12</span><span class="sxs-lookup"><span data-stu-id="e748e-110">Direct3D 11 on 12</span></span>](direct3d-11-on-12.md)<br/>                                             | <span data-ttu-id="e748e-111">D3D11On12 è un meccanismo mediante il quale gli sviluppatori possono usare le interfacce e gli oggetti di D3D11 per guidare l'API D3D12.</span><span class="sxs-lookup"><span data-stu-id="e748e-111">D3D11On12 is a mechanism by which developers can use D3D11 interfaces and objects to drive the D3D12 API.</span></span> <span data-ttu-id="e748e-112">D3D11on12 consente ai componenti scritti con D3D11, ad esempio D2D testo e interfaccia utente, di interagire con i componenti scritti per l'API D3D12.</span><span class="sxs-lookup"><span data-stu-id="e748e-112">D3D11on12 enables components written using D3D11 (for example, D2D text and UI) to work together with components written targeting the D3D12 API.</span></span> <span data-ttu-id="e748e-113">D3D11on12 consente anche il porting incrementale di un'applicazione da D3D11 a D3D12, consentendo a parti dell'app di continuare a usare D3D11 per semplicità, mentre altre sono destinate a D3D12 per le prestazioni, pur avendo sempre il rendering completo e corretto.</span><span class="sxs-lookup"><span data-stu-id="e748e-113">D3D11on12 also enables incremental porting of an application from D3D11 to D3D12, by enabling portions of the app to continue targeting D3D11 for simplicity while others target D3D12 for performance, while always having complete and correct rendering.</span></span> <span data-ttu-id="e748e-114">D3D11On12 rende più semplice l'uso di tecniche di interoperabilità per condividere le risorse e sincronizzare il lavoro tra le due API.</span><span class="sxs-lookup"><span data-stu-id="e748e-114">D3D11On12 makes it simpler than using interop techniques to share resources and synchronize work between the two APIs.</span></span> <br/> |
| [<span data-ttu-id="e748e-115">Conversione da Direct3D 11 a Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e748e-115">Porting from Direct3D 11 to Direct3D 12</span></span>](porting-from-direct3d-11-to-direct3d-12.md)<br/> | <span data-ttu-id="e748e-116">In questa sezione vengono fornite alcune indicazioni sul porting da un motore di grafica Direct3D 11 personalizzato a Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="e748e-116">This section provides some guidance on porting from a custom Direct3D 11 graphics engine to Direct3D 12.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="e748e-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e748e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e748e-118">Guida per programmatori Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e748e-118">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> </dl>

 

 





