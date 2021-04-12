---
title: Articoli sulla grafica DirectX
description: .
ms.assetid: 22178507-9a3b-49b1-a3db-851001a32e8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16ac2a3a6b9beff7dfc8bfe4f6c0de92885f39ca
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338654"
---
# <a name="directx-graphics-articles"></a>Articoli sulla grafica DirectX

## <a name="purpose"></a>Scopo

Questa sezione contiene articoli tecnici che descrivono il supporto di WARP e Windows 7 appena aggiunto per la modalità Flip presente e le statistiche presenti associate in Direct3D 9Ex e Gestione finestre desktop. Questa sezione contiene inoltre articoli tecnici sulle API di grafica Windows, il porting delle API Direct3D 9 alle API Microsoft DirectX Graphics Infrastructure (DXGI) e come distribuire Direct3D 11.

Per ulteriori informazioni su Direct3D, vedere [Direct3D](/windows/desktop/direct3d).

## <a name="developer-audience"></a>Sviluppatori

Questi articoli tecnici sono destinati agli sviluppatori di applicazioni grafiche DirectX.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [Aggiornamento della piattaforma per Windows 7](platform-update-for-windows-7.md) | Vengono descritti i componenti dello stack di grafica Windows 8 che diventano disponibili e in quale misura, tramite l' [aggiornamento della piattaforma per Windows 7](https://support.microsoft.com/kb/2670838). |
| [Miglioramenti di Direct3D 9Ex](direct3d-9ex-improvements.md) | Viene descritto il supporto appena aggiunto di Windows 7 per la modalità Flip presente e le statistiche presenti associate in Direct3D 9Ex e Gestione finestre desktop. Le applicazioni di destinazione includono video o applicazioni di presentazione basate su framerate. Le applicazioni che usano la modalità Flip 9Ex Direct3D presentano una riduzione del carico delle risorse di sistema quando DWM è abilitato. I miglioramenti attuali delle statistiche associati alla modalità Flip consentono alle applicazioni Direct3D 9Ex di controllare meglio la frequenza di presentazione fornendo i meccanismi di correzione e feedback in tempo reale. Sono incluse spiegazioni dettagliate e puntatori alle risorse di esempio. |
| [Condivisione della superficie tra le API di grafica Windows](surface-sharing-between-windows-graphics-apis.md) | Fornisce una panoramica tecnica sull'interoperabilità con la condivisione della superficie tra le API di grafica Windows, tra cui Direct3D 11, Direct2D, Direct3D 10 e Direct3D 9Ex. Se si ha già una conoscenza approfondita di queste API, questo documento consente di usare più API per eseguire il rendering nella stessa area in un'applicazione progettata per i sistemi operativi Windows 7 o Windows Vista. Questo argomento fornisce anche le linee guida per le procedure consigliate e i puntatori a risorse aggiuntive. |
| [Guida a WARP](directx-warp.md) | Fornisce una guida di Windows Advanced Rasterizzation Platform (WARP), un rasterizzatore software ad alta velocità. |
| [API grafiche in Windows](graphics-apis-in-windows-vista.md) | Vengono illustrate le funzionalità e le API di Windows graphics. |
| [Distribuzione di Direct3D 11 per sviluppatori di giochi](direct3d11-deployment.md) | Viene descritto come distribuire i componenti di Direct3D 11 in un sistema. |
| [Infrastruttura grafica DirectX (DXGI): procedure consigliate](dxgi-best-practices.md) | Vengono illustrati i problemi relativi al porting delle API Direct3D 9 alle API e alle funzionalità di DXGI di diverse versioni di DXGI. |
| [Uso di DirectX con schermi HDR e colori avanzati](high-dynamic-range.md) | In questo argomento viene fornita una panoramica tecnica sul rendering di contenuti High Dynamic Range Direct3D 11 e Direct3D 12 in una visualizzazione HDR10 con il supporto dei colori avanzati di Windows 10. |