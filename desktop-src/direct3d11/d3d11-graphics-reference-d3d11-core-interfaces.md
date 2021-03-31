---
title: Interfacce di base Direct3D 11
description: Questa sezione contiene informazioni sulle interfacce di base.
ms.assetid: e96804db-0987-49ca-b1b1-321f36c13024
keywords:
- interfacce, Direct3D 11 Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c578d84a7a9f223cb81285b69f5b5d1baed4e6
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104474526"
---
# <a name="direct3d-11-core-interfaces"></a><span data-ttu-id="e8df4-104">Interfacce di base Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="e8df4-104">Direct3D 11 core interfaces</span></span>

<span data-ttu-id="e8df4-105">Questa sezione contiene informazioni sulle interfacce di base.</span><span class="sxs-lookup"><span data-stu-id="e8df4-105">This section contains information about the core interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e8df4-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="e8df4-106">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8df4-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="e8df4-107">Topic</span></span></th>
<th><span data-ttu-id="e8df4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8df4-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e8df4-109"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-109"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-110">Questa interfaccia incapsula i metodi per recuperare i dati dalla GPU in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="e8df4-110">This interface encapsulates methods for retrieving data from the GPU asynchronously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8df4-111"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate"><strong>ID3D11BlendState</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-111"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate"><strong>ID3D11BlendState</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-112">L'interfaccia di stato di Blend include una descrizione per lo stato di fusione che è possibile associare alla <a href="d3d10-graphics-programming-guide-output-merger-stage.md">fase di Unione dell'output</a>.</span><span class="sxs-lookup"><span data-stu-id="e8df4-112">The blend-state interface holds a description for blending state that you can bind to the <a href="d3d10-graphics-programming-guide-output-merger-stage.md">output-merger stage</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8df4-113"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11blendstate1"><strong>ID3D11BlendState1</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-113"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11blendstate1"><strong>ID3D11BlendState1</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-114">L'interfaccia di stato di Blend include una descrizione per lo stato di fusione che è possibile associare alla <a href="d3d10-graphics-programming-guide-output-merger-stage.md">fase di Unione dell'output</a>.</span><span class="sxs-lookup"><span data-stu-id="e8df4-114">The blend-state interface holds a description for blending state that you can bind to the <a href="d3d10-graphics-programming-guide-output-merger-stage.md">output-merger stage</a>.</span></span> <span data-ttu-id="e8df4-115">Questa interfaccia di stato di Blend supporta le operazioni logiche e le operazioni di fusione.</span><span class="sxs-lookup"><span data-stu-id="e8df4-115">This blend-state interface supports logical operations as well as blending operations.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8df4-116"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-116"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-117">L'interfaccia <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a> incapsula un elenco di comandi grafici per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="e8df4-117">The <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a> interface encapsulates a list of graphics commands for play back.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8df4-118"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11counter"><strong>ID3D11Counter</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-118"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11counter"><strong>ID3D11Counter</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-119">Questa interfaccia incapsula i metodi per misurare le prestazioni della GPU.</span><span class="sxs-lookup"><span data-stu-id="e8df4-119">This interface encapsulates methods for measuring GPU performance.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8df4-120"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate"><strong>ID3D11DepthStencilState</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-120"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate"><strong>ID3D11DepthStencilState</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-121">L'interfaccia di depth-stencil-state include una descrizione dello stato dello stencil depth che è possibile associare alla <a href="d3d10-graphics-programming-guide-output-merger-stage.md">fase di Unione dell'output</a>.</span><span class="sxs-lookup"><span data-stu-id="e8df4-121">The depth-stencil-state interface holds a description for depth-stencil state that you can bind to the <a href="d3d10-graphics-programming-guide-output-merger-stage.md">output-merger stage</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8df4-122"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-122"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-123">L'interfaccia del dispositivo rappresenta una scheda virtuale; viene usato per creare risorse.</span><span class="sxs-lookup"><span data-stu-id="e8df4-123">The device interface represents a virtual adapter; it is used to create resources.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8df4-124"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-124"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-125">L'interfaccia del dispositivo rappresenta una scheda virtuale; viene usato per creare risorse.</span><span class="sxs-lookup"><span data-stu-id="e8df4-125">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="e8df4-126"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a> aggiunge nuovi metodi a quelli in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e8df4-126"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8df4-127"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-127"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-128">L'interfaccia del dispositivo rappresenta una scheda virtuale; viene usato per creare risorse.</span><span class="sxs-lookup"><span data-stu-id="e8df4-128">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="e8df4-129"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a> aggiunge nuovi metodi a quelli in <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e8df4-129"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8df4-130"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-130"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-131">L'interfaccia del dispositivo rappresenta una scheda virtuale; viene usato per creare risorse.</span><span class="sxs-lookup"><span data-stu-id="e8df4-131">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="e8df4-132"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a> aggiunge nuovi metodi a quelli in <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e8df4-132"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8df4-133"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-133"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-134">L'interfaccia del dispositivo rappresenta una scheda virtuale; viene usato per creare risorse.</span><span class="sxs-lookup"><span data-stu-id="e8df4-134">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="e8df4-135"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a> aggiunge nuovi metodi a quelli in <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a>, ad esempio <strong>RegisterDeviceRemovedEvent</strong> e <strong>UnregisterDeviceRemoved</strong>.</span><span class="sxs-lookup"><span data-stu-id="e8df4-135"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a>, such as <strong>RegisterDeviceRemovedEvent</strong> and <strong>UnregisterDeviceRemoved</strong>.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8df4-136"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-136"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-137">L'interfaccia del dispositivo rappresenta una scheda virtuale; viene usato per creare risorse.</span><span class="sxs-lookup"><span data-stu-id="e8df4-137">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="e8df4-138"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a> aggiunge nuovi metodi a quelli in <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e8df4-138"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a> adds new methods to those in <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8df4-139"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-139"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-140">Un'interfaccia di dispositivo-figlio accede ai dati usati da un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e8df4-140">A device-child interface accesses data used by a device.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8df4-141"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-141"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-142">L'interfaccia <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>sul ID3D11DeviceContext</strong></a> rappresenta un contesto di dispositivo che genera comandi di rendering.</span><span class="sxs-lookup"><span data-stu-id="e8df4-142">The <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> interface represents a device context which generates rendering commands.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e8df4-143">La versione più recente di questa interfaccia è <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> introdotta in Windows 10 Creators Update.</span><span class="sxs-lookup"><span data-stu-id="e8df4-143">The latest version of this interface is <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> introduced in the Windows 10 Creators Update.</span></span> <span data-ttu-id="e8df4-144">Le applicazioni destinazione Windows 10 Creators Update devono usare l'interfaccia <strong>ID3D11DeviceContext4</strong> anziché <strong>ID3D11Device</strong>.</span><span class="sxs-lookup"><span data-stu-id="e8df4-144">Applications targetting Windows 10 Creators Update should use the <strong>ID3D11DeviceContext4</strong> interface instead of <strong>ID3D11Device</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8df4-145"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-145"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-146">L'interfaccia del contesto del dispositivo rappresenta un contesto di dispositivo; viene usato per eseguire il rendering di comandi.</span><span class="sxs-lookup"><span data-stu-id="e8df4-146">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="e8df4-147"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a> aggiunge nuovi metodi a quelli in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>sul ID3D11DeviceContext</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e8df4-147"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8df4-148"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-148"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-149">L'interfaccia del contesto del dispositivo rappresenta un contesto di dispositivo; viene usato per eseguire il rendering di comandi.</span><span class="sxs-lookup"><span data-stu-id="e8df4-149">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="e8df4-150"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a> aggiunge nuovi metodi a quelli in <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e8df4-150"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8df4-151"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-151"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-152">L'interfaccia del contesto del dispositivo rappresenta un contesto di dispositivo; viene usato per eseguire il rendering di comandi.</span><span class="sxs-lookup"><span data-stu-id="e8df4-152">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="e8df4-153"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a> aggiunge nuovi metodi a quelli in <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e8df4-153"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a>.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8df4-154"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-154"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-155">L'interfaccia del contesto del dispositivo rappresenta un contesto di dispositivo; viene usato per eseguire il rendering di comandi.</span><span class="sxs-lookup"><span data-stu-id="e8df4-155">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="e8df4-156"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> aggiunge nuovi metodi a quelli in <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e8df4-156"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> adds new methods to those in <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8df4-157"><a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-157"><a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-158">L'interfaccia <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a> rappresenta un oggetto stato del contesto, che include informazioni sullo stato e sul comportamento di un dispositivo Microsoft Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e8df4-158">The <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a> interface represents a context state object, which holds state and behavior information about a Microsoft Direct3D device.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8df4-159"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence"><strong>ID3D11Fence</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-159"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence"><strong>ID3D11Fence</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-160">Rappresenta una recinzione, un oggetto usato per la sincronizzazione della CPU e una o più GPU.</span><span class="sxs-lookup"><span data-stu-id="e8df4-160">Represents a fence, an object used for synchronization of the CPU and one or more GPUs.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8df4-161"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11inputlayout"><strong>ID3D11InputLayout</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-161"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11inputlayout"><strong>ID3D11InputLayout</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-162">Un'interfaccia di input-layout include una definizione del modo in cui inserire i dati dei vertici disposti in memoria nella <a href="d3d10-graphics-programming-guide-input-assembler-stage.md">fase input-assembler</a> della <a href="overviews-direct3d-11-graphics-pipeline.md">pipeline grafica</a>.</span><span class="sxs-lookup"><span data-stu-id="e8df4-162">An input-layout interface holds a definition of how to feed vertex data that is laid out in memory into the <a href="d3d10-graphics-programming-guide-input-assembler-stage.md">input-assembler stage</a> of the <a href="overviews-direct3d-11-graphics-pipeline.md">graphics pipeline</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8df4-163"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread"><strong>ID3D11Multithread</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-163"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread"><strong>ID3D11Multithread</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-164">Fornisce la protezione del threading per le sezioni critiche di un'applicazione multithread.</span><span class="sxs-lookup"><span data-stu-id="e8df4-164">Provides threading protection for critical sections of a multi-threaded application.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8df4-165"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate"><strong>ID3D11Predicate</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-165"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate"><strong>ID3D11Predicate</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-166">Un'interfaccia di predicato determina se la geometria deve essere elaborata in base ai risultati di una chiamata di progetto precedente.</span><span class="sxs-lookup"><span data-stu-id="e8df4-166">A predicate interface determines whether geometry should be processed depending on the results of a previous draw call.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8df4-167"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-167"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-168">Un'interfaccia di query esegue query sulle informazioni dalla GPU.</span><span class="sxs-lookup"><span data-stu-id="e8df4-168">A query interface queries information from the GPU.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8df4-169"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11query1"><strong>ID3D11Query1</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-169"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11query1"><strong>ID3D11Query1</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-170">Rappresenta un oggetto query per l'esecuzione di query sulle informazioni dell'unità di elaborazione grafica (GPU).</span><span class="sxs-lookup"><span data-stu-id="e8df4-170">Represents a query object for querying information from the graphics processing unit (GPU).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8df4-171"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate"><strong>ID3D11RasterizerState</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-171"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate"><strong>ID3D11RasterizerState</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-172">L'interfaccia di stato del rasterizzatore include una descrizione per lo stato di rasterizzazione che è possibile associare alla <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">fase di rasterizzazione</a>.</span><span class="sxs-lookup"><span data-stu-id="e8df4-172">The rasterizer-state interface holds a description for rasterizer state that you can bind to the <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">rasterizer stage</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8df4-173"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11rasterizerstate1"><strong>ID3D11RasterizerState1</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-173"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11rasterizerstate1"><strong>ID3D11RasterizerState1</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-174">L'interfaccia di stato del rasterizzatore include una descrizione per lo stato di rasterizzazione che è possibile associare alla <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">fase di rasterizzazione</a>.</span><span class="sxs-lookup"><span data-stu-id="e8df4-174">The rasterizer-state interface holds a description for rasterizer state that you can bind to the <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">rasterizer stage</a>.</span></span> <span data-ttu-id="e8df4-175">Questa interfaccia di stato del rasterizzatore supporta il numero di campioni forzato.</span><span class="sxs-lookup"><span data-stu-id="e8df4-175">This rasterizer-state interface supports forced sample count.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8df4-176"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rasterizerstate2"><strong>ID3D11RasterizerState2</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-176"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rasterizerstate2"><strong>ID3D11RasterizerState2</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-177">L'interfaccia di stato del rasterizzatore include una descrizione per lo stato di rasterizzazione che è possibile associare alla <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">fase di rasterizzazione</a>.</span><span class="sxs-lookup"><span data-stu-id="e8df4-177">The rasterizer-state interface holds a description for rasterizer state that you can bind to the <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">rasterizer stage</a>.</span></span> <span data-ttu-id="e8df4-178">Questa interfaccia di stato del rasterizzatore supporta il numero di campioni forzato e la modalità di rasterizzazione conservativa.</span><span class="sxs-lookup"><span data-stu-id="e8df4-178">This rasterizer-state interface supports forced sample count and conservative rasterization mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8df4-179"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate"><strong>ID3D11SamplerState</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8df4-179"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate"><strong>ID3D11SamplerState</strong></a></span></span><br/></td>
<td><span data-ttu-id="e8df4-180">L'interfaccia di stato del campionatore include una descrizione per lo stato del campionatore che è possibile associare a qualsiasi fase dello shader della <a href="overviews-direct3d-11-graphics-pipeline.md">pipeline</a> per riferimento da operazioni di esempio di trama.</span><span class="sxs-lookup"><span data-stu-id="e8df4-180">The sampler-state interface holds a description for sampler state that you can bind to any shader stage of the <a href="overviews-direct3d-11-graphics-pipeline.md">pipeline</a> for reference by texture sample operations.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e8df4-181">Direct3D 11 implementa le interfacce per:</span><span class="sxs-lookup"><span data-stu-id="e8df4-181">Direct3D 11 implements interfaces for:</span></span>

-   [<span data-ttu-id="e8df4-182">Risorse</span><span class="sxs-lookup"><span data-stu-id="e8df4-182">Resources</span></span>](d3d11-graphics-reference-resource-interfaces.md)
-   [<span data-ttu-id="e8df4-183">Shader</span><span class="sxs-lookup"><span data-stu-id="e8df4-183">Shaders</span></span>](d3d11-graphics-reference-d3d11-shader-interfaces.md)

## <a name="related-topics"></a><span data-ttu-id="e8df4-184">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e8df4-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8df4-185">Riferimento principale</span><span class="sxs-lookup"><span data-stu-id="e8df4-185">Core Reference</span></span>](d3d11-graphics-reference-d3d11-core.md)
</dt> </dl>

