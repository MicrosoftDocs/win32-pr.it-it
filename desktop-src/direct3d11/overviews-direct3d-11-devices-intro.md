---
title: Introduzione a un dispositivo in Direct3D 11
description: Il modello a oggetti Direct3D 11 separa la funzionalità di creazione e rendering delle risorse in un dispositivo e in uno o più contesti. questa separazione è progettata per facilitare il multithreading.
ms.assetid: b9b45d18-f7b7-40f9-ae4e-576ca7a6eba7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9459574ad7d8732714ac54519294ae232e4d8d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475707"
---
# <a name="introduction-to-a-device-in-direct3d-11"></a>Introduzione a un dispositivo in Direct3D 11

Il modello a oggetti Direct3D 11 separa la funzionalità di creazione e rendering delle risorse in un dispositivo e in uno o più contesti. questa separazione è progettata per facilitare il multithreading.

-   [Dispositivo](#introduction-to-a-device-in-direct3d-11)
-   [Contesto di dispositivo](#device-context)
    -   [Contesto immediato](#immediate-context)
    -   [Contesto posticipato](#deferred-context)
-   [Considerazioni sul threading](#threading-considerations)
-   [Argomenti correlati](#related-topics)

## <a name="device"></a>Dispositivo

Un dispositivo viene usato per creare risorse ed enumerare le funzionalità di una scheda video. In Direct3D 11 un dispositivo è rappresentato con [**un'interfaccia ID3D11Device.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)

Ogni applicazione deve avere almeno un dispositivo, la maggior parte delle applicazioni crea un solo dispositivo. Creare un dispositivo per uno dei driver hardware installati nel computer chiamando [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) e specificare il tipo di driver con il flag [**D3D \_ DRIVER \_ TYPE.**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) Ogni dispositivo può usare uno o più contesti di dispositivo, a seconda della funzionalità desiderata.

## <a name="device-context"></a>Contesto di dispositivo

Un contesto di dispositivo contiene la circostanza o l'impostazione in cui viene usato un dispositivo. In particolare, viene usato un contesto di dispositivo per impostare lo stato della pipeline e generare comandi di rendering usando le risorse di proprietà di un dispositivo. Direct3D 11 implementa due tipi di contesti di dispositivo, uno per il rendering immediato e l'altro per il rendering posticipato. entrambi i contesti sono rappresentati con [**un'interfaccia ID3D11DeviceContext.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)

### <a name="immediate-context"></a>Contesto immediato

Il rendering di un contesto immediato viene eseguito direttamente nel driver. Ogni dispositivo ha un solo contesto immediato che può recuperare i dati dalla GPU. Un contesto immediato può essere usato per eseguire immediatamente il rendering (o riprodurre) un [elenco di comandi.](overviews-direct3d-11-render-multi-thread-command-list.md)

Esistono due modi per ottenere un contesto immediato:

-   Chiamando [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).
-   Chiamando [**ID3D11Device::GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).

### <a name="deferred-context"></a>Contesto posticipato

Un contesto posticipato registra i comandi GPU in un [elenco di comandi](overviews-direct3d-11-render-multi-thread-command-list.md). Un contesto posticipato viene usato principalmente per il multithreading e non è necessario per un'applicazione a thread singolo. Un contesto posticipato viene in genere usato da un thread di lavoro anziché dal thread di rendering principale. Quando si crea un contesto posticipato, non eredita alcuno stato dal contesto immediato.

Per ottenere un contesto posticipato, chiamare [**ID3D11Device::CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).

Qualsiasi contesto, immediato o posticipato, può essere usato in qualsiasi thread, purché il contesto sia usato solo in un thread alla volta.

## <a name="threading-considerations"></a>Considerazioni sul threading

Questa tabella evidenzia le differenze nel modello di threading in Direct3D 11 rispetto alle versioni precedenti di Direct3D.




| | | Differenze tra Direct3D 11 e le versioni precedenti di Direct3D:<br /> Tutti <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>i metodi dell'interfaccia ID3D11Device</strong></a> sono a thread libero, pertanto è sicuro che più thread chiamino le funzioni contemporaneamente.<br /><ul><li>Tutte le interfacce derivate da <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>(<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer"><strong>ID3D11Buffer,</strong></a> <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a>e così via) sono a thread libero.</li><li>Direct3D 11 suddivide la creazione e il rendering delle risorse in due interfacce. Map, Unmap, Begin, End e GetData vengono implementati in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> perché <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> definisce fortemente l'ordine delle operazioni. <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11resource"><strong>Le interfacce ID3D11Resource</strong></a> e <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a> implementano anche metodi per operazioni a thread libero.</li><li>I <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>metodi ID3D11DeviceContext</strong></a> (ad eccezione di quelli presenti in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild)</strong></a>non sono a thread libero, ovvero richiedono un threading singolo. Solo un thread può chiamare in modo sicuro uno dei relativi metodi (Disegno, Copia, Mappa e così via) alla volta.</li><li>In generale, il threading libero riduce al minimo il numero di primitive di sincronizzazione usate e la relativa durata. Tuttavia, un'applicazione che usa la sincronizzazione mantenuta per molto tempo può influire direttamente sulla concorrenza che un'applicazione può aspettarsi di ottenere.</li></ul>I metodi dell'interfaccia ID3D10Device non sono progettati per essere a thread libero. ID3D10Device implementa tutte le funzionalità di creazione e rendering (come ID3D9Device in Direct3D 9). Map e Unmap vengono implementati in interfacce derivate da ID3D10Resource, Begin, End e GetData implementate nelle interfacce derivate da ID3D10Asynchronous.<br /> | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





