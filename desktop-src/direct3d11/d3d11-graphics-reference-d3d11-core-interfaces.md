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
# <a name="direct3d-11-core-interfaces"></a>Interfacce di base Direct3D 11

Questa sezione contiene informazioni sulle interfacce di base.

## <a name="in-this-section"></a>Contenuto della sezione



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a><br/></td>
<td>Questa interfaccia incapsula i metodi per recuperare i dati dalla GPU in modo asincrono.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate"><strong>ID3D11BlendState</strong></a><br/></td>
<td>L'interfaccia di stato di Blend include una descrizione per lo stato di fusione che è possibile associare alla <a href="d3d10-graphics-programming-guide-output-merger-stage.md">fase di Unione dell'output</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11blendstate1"><strong>ID3D11BlendState1</strong></a><br/></td>
<td>L'interfaccia di stato di Blend include una descrizione per lo stato di fusione che è possibile associare alla <a href="d3d10-graphics-programming-guide-output-merger-stage.md">fase di Unione dell'output</a>. Questa interfaccia di stato di Blend supporta le operazioni logiche e le operazioni di fusione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a><br/></td>
<td>L'interfaccia <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a> incapsula un elenco di comandi grafici per la riproduzione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11counter"><strong>ID3D11Counter</strong></a><br/></td>
<td>Questa interfaccia incapsula i metodi per misurare le prestazioni della GPU.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate"><strong>ID3D11DepthStencilState</strong></a><br/></td>
<td>L'interfaccia di depth-stencil-state include una descrizione dello stato dello stencil depth che è possibile associare alla <a href="d3d10-graphics-programming-guide-output-merger-stage.md">fase di Unione dell'output</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a><br/></td>
<td>L'interfaccia del dispositivo rappresenta una scheda virtuale; viene usato per creare risorse.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a><br/></td>
<td>L'interfaccia del dispositivo rappresenta una scheda virtuale; viene usato per creare risorse. <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a> aggiunge nuovi metodi a quelli in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a><br/></td>
<td>L'interfaccia del dispositivo rappresenta una scheda virtuale; viene usato per creare risorse. <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a> aggiunge nuovi metodi a quelli in <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a><br/></td>
<td>L'interfaccia del dispositivo rappresenta una scheda virtuale; viene usato per creare risorse. <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a> aggiunge nuovi metodi a quelli in <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a><br/></td>
<td>L'interfaccia del dispositivo rappresenta una scheda virtuale; viene usato per creare risorse. <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a> aggiunge nuovi metodi a quelli in <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a>, ad esempio <strong>RegisterDeviceRemovedEvent</strong> e <strong>UnregisterDeviceRemoved</strong>. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a><br/></td>
<td>L'interfaccia del dispositivo rappresenta una scheda virtuale; viene usato per creare risorse. <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a> aggiunge nuovi metodi a quelli in <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a><br/></td>
<td>Un'interfaccia di dispositivo-figlio accede ai dati usati da un dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a><br/></td>
<td>L'interfaccia <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>sul ID3D11DeviceContext</strong></a> rappresenta un contesto di dispositivo che genera comandi di rendering.<br/>
<blockquote>
[!Note]<br />
La versione più recente di questa interfaccia è <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> introdotta in Windows 10 Creators Update. Le applicazioni destinazione Windows 10 Creators Update devono usare l'interfaccia <strong>ID3D11DeviceContext4</strong> anziché <strong>ID3D11Device</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a><br/></td>
<td>L'interfaccia del contesto del dispositivo rappresenta un contesto di dispositivo; viene usato per eseguire il rendering di comandi. <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a> aggiunge nuovi metodi a quelli in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>sul ID3D11DeviceContext</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a><br/></td>
<td>L'interfaccia del contesto del dispositivo rappresenta un contesto di dispositivo; viene usato per eseguire il rendering di comandi. <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a> aggiunge nuovi metodi a quelli in <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a><br/></td>
<td>L'interfaccia del contesto del dispositivo rappresenta un contesto di dispositivo; viene usato per eseguire il rendering di comandi. <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a> aggiunge nuovi metodi a quelli in <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a>. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a><br/></td>
<td>L'interfaccia del contesto del dispositivo rappresenta un contesto di dispositivo; viene usato per eseguire il rendering di comandi. <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> aggiunge nuovi metodi a quelli in <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a><br/></td>
<td>L'interfaccia <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a> rappresenta un oggetto stato del contesto, che include informazioni sullo stato e sul comportamento di un dispositivo Microsoft Direct3D.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence"><strong>ID3D11Fence</strong></a><br/></td>
<td>Rappresenta una recinzione, un oggetto usato per la sincronizzazione della CPU e una o più GPU.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11inputlayout"><strong>ID3D11InputLayout</strong></a><br/></td>
<td>Un'interfaccia di input-layout include una definizione del modo in cui inserire i dati dei vertici disposti in memoria nella <a href="d3d10-graphics-programming-guide-input-assembler-stage.md">fase input-assembler</a> della <a href="overviews-direct3d-11-graphics-pipeline.md">pipeline grafica</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread"><strong>ID3D11Multithread</strong></a><br/></td>
<td>Fornisce la protezione del threading per le sezioni critiche di un'applicazione multithread.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate"><strong>ID3D11Predicate</strong></a><br/></td>
<td>Un'interfaccia di predicato determina se la geometria deve essere elaborata in base ai risultati di una chiamata di progetto precedente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a><br/></td>
<td>Un'interfaccia di query esegue query sulle informazioni dalla GPU.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11query1"><strong>ID3D11Query1</strong></a><br/></td>
<td>Rappresenta un oggetto query per l'esecuzione di query sulle informazioni dell'unità di elaborazione grafica (GPU).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate"><strong>ID3D11RasterizerState</strong></a><br/></td>
<td>L'interfaccia di stato del rasterizzatore include una descrizione per lo stato di rasterizzazione che è possibile associare alla <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">fase di rasterizzazione</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11rasterizerstate1"><strong>ID3D11RasterizerState1</strong></a><br/></td>
<td>L'interfaccia di stato del rasterizzatore include una descrizione per lo stato di rasterizzazione che è possibile associare alla <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">fase di rasterizzazione</a>. Questa interfaccia di stato del rasterizzatore supporta il numero di campioni forzato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rasterizerstate2"><strong>ID3D11RasterizerState2</strong></a><br/></td>
<td>L'interfaccia di stato del rasterizzatore include una descrizione per lo stato di rasterizzazione che è possibile associare alla <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">fase di rasterizzazione</a>. Questa interfaccia di stato del rasterizzatore supporta il numero di campioni forzato e la modalità di rasterizzazione conservativa.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate"><strong>ID3D11SamplerState</strong></a><br/></td>
<td>L'interfaccia di stato del campionatore include una descrizione per lo stato del campionatore che è possibile associare a qualsiasi fase dello shader della <a href="overviews-direct3d-11-graphics-pipeline.md">pipeline</a> per riferimento da operazioni di esempio di trama.<br/></td>
</tr>
</tbody>
</table>



 

Direct3D 11 implementa le interfacce per:

-   [Risorse](d3d11-graphics-reference-resource-interfaces.md)
-   [Shader](d3d11-graphics-reference-d3d11-shader-interfaces.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento principale](d3d11-graphics-reference-d3d11-core.md)
</dt> </dl>

