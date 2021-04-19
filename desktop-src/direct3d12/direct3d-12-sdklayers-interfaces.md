---
title: Interfacce del livello di debug
description: Le interfacce seguenti sono dichiarate in d3d12sdklayers. h.
ms.assetid: 9BD5910A-8FF2-4540-BB8E-8EA5C10528CE
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e37dbe2e3348a500a8898d1e1076d2fafde66768
ms.sourcegitcommit: 0aa1dd7577961438a1b3172f3a92fb11cbf359f1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2020
ms.locfileid: "106299483"
---
# <a name="debug-layer-interfaces"></a>Interfacce del livello di debug

Le interfacce seguenti sono definite in `d3d12sdklayers.h` .

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**ID3D12Debug**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug) | Un'interfaccia di debug controlla le impostazioni di debug e convalida lo stato della pipeline. Può essere utilizzato solo se il livello di debug è attivato. |
| [**ID3D12Debug1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1) | Aggiunge la convalida basata su GPU e la sincronizzazione della coda dei comandi dipendenti al livello di debug. |
| [**ID3D12Debug2**](/windows/desktop/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2) | Aggiunge livelli configurabili di convalida GPU-Based. |
| [**ID3D12Debug3**](/windows/desktop/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug3) | Aggiunge alla convalida basata su GPU del livello di debug, alla sincronizzazione della coda dei comandi dipendenti e ai livelli configurabili della convalida basata su GPU. |
| [**ID3D12DebugCommandList**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist) | Fornisce metodi per monitorare ed eseguire il debug di un elenco di comandi. |
| [**ID3D12DebugCommandList1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1) | Questa interfaccia consente di modificare le impostazioni aggiuntive del livello di debug dell'elenco dei comandi. |
| [**ID3D12DebugCommandQueue**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandqueue) | Fornisce metodi per monitorare ed eseguire il debug di una coda di comandi. |
| [**ID3D12DebugDevice**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice) | Questa interfaccia rappresenta un dispositivo grafico per il debug. |
| [**ID3D12DebugDevice1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1) | Specifica le impostazioni del livello di debug a livello di dispositivo. |
| [**ID3D12InfoQueue**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue) | Un'interfaccia della coda di informazioni archivia, recupera e filtra i messaggi di debug. La coda è costituita da una coda di messaggi, da uno stack di filtri di archiviazione facoltativo e da uno stack di filtri di recupero facoltativo. |
| [**ID3D12SharingContract**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12sharingcontract) | Parte di un contratto tra i livelli di diagnostica D3D11On12 e gli strumenti di diagnostica grafica. |

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione dell'ambiente di programmazione Direct3D 12](directx-12-programming-environment-set-up.md)
</dt> <dt>

[Riferimento al livello di debug](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[Guida di riferimento a Direct3D 12](direct3d-12-reference.md)
</dt> </dl>