---
title: Interfacce del livello di debug
description: Le interfacce seguenti sono dichiarate in d3d12sdklayers.h.
ms.assetid: 9BD5910A-8FF2-4540-BB8E-8EA5C10528CE
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d7e16d6c593f2dcfcc46266102ac15a61386ef
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812873"
---
# <a name="debug-layer-interfaces"></a>Interfacce del livello di debug

Le interfacce seguenti sono definite in `d3d12sdklayers.h` .

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**ID3D12Debug**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug) | Un'interfaccia di debug controlla le impostazioni di debug e convalida lo stato della pipeline. Può essere usato solo se il livello di debug è attivato. |
| [**ID3D12Debug1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1) | Aggiunge la convalida basata su GPU e la sincronizzazione della coda dei comandi dipendenti al livello di debug. |
| [**ID3D12Debug2**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2) | Aggiunge livelli configurabili di GPU-Based convalida. |
| [**ID3D12Debug3**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug3) | Aggiunge al livello di debug la convalida basata su GPU, la sincronizzazione della coda dei comandi dipendenti e i livelli configurabili di convalida basata su GPU. |
| [**ID3D12Debug4**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug4) | Aggiunge la possibilità di disabilitare il livello di debug. |
| [**ID3D12Debug5**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug5) | Aggiunge al livello di debug la possibilità di configurare la denominazione automatica degli oggetti. |
| [**ID3D12DebugCommandList**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist) | Fornisce metodi per monitorare ed eseguire il debug di un elenco di comandi. |
| [**ID3D12DebugCommandList1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1) | Questa interfaccia consente di modificare le impostazioni aggiuntive del livello di debug dell'elenco di comandi. |
| [**ID3D12DebugCommandQueue**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandqueue) | Fornisce metodi per monitorare ed eseguire il debug di una coda di comandi. |
| [**ID3D12DebugDevice**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice) | Questa interfaccia rappresenta un dispositivo grafico per il debug. |
| [**ID3D12DebugDevice1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1) | Specifica le impostazioni del livello di debug a livello di dispositivo. |
| [**ID3D12InfoQueue**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue) | Un'interfaccia information-queue archivia, recupera e filtra i messaggi di debug. La coda è costituita da una coda di messaggi, uno stack di filtri di archiviazione facoltativo e uno stack di filtri di recupero facoltativo. |
| [**ID3D12SharingContract**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12sharingcontract) | Parte di un contratto tra i livelli di diagnostica D3D11On12 e gli strumenti di diagnostica della grafica. |

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Installazione dell'ambiente di programmazione Direct3D 12](directx-12-programming-environment-set-up.md)
</dt> <dt>

[Informazioni di riferimento sul livello di debug](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[Informazioni di riferimento su Direct3D 12](direct3d-12-reference.md)
</dt> </dl>