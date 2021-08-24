---
description: L'API Direct3D 9 opera sul modello di driver video Windows XP (XPDM) o sul modello di driver di visualizzazione di Windows Vista (WDDM), a seconda del sistema operativo installato.
ms.assetid: b552c822-aa01-4f1d-a0a6-1411ab006e7b
title: XPDM e WDDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0332198cd7c9425a3b5a107259dda1b1e974a04a2379244cdf939384260a89f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746051"
---
# <a name="xpdm-vs-wddm"></a>XPDM e WDDM

L'API Direct3D 9 opera sul modello di driver video Windows XP (XPDM) o sul modello di driver di visualizzazione di Windows Vista (WDDM), a seconda del sistema operativo installato. Esistono alcune differenze nel comportamento dell'API Direct3D nei due modelli di driver.

-   [Desktop sicuro](#secure-desktop)
-   [Desktop remoto](#remote-desktop)
-   [Servizio Windows](#windows-service)
-   [Argomenti correlati](#related-topics)

## <a name="secure-desktop"></a>Desktop sicuro

Il desktop protetto è attivo ogni volta che si verifica una delle operazioni seguenti: l'utente blocca il desktop (Windows+L), il screen saver viene attivato (quando nessun utente è connesso) o per impostazione predefinita quando controllo dell'account utente visualizza una richiesta. Quando il desktop sicuro è attivo, il dispositivo HAL non è accessibile.

Differenze tra XPDM e WDDM:

- Il tentativo di creare un dispositivo Direct3D9 HAL avrà esito negativo (con **D3DERR \_ NON \_ DISPONIBILE)** e qualsiasi dispositivo Direct3D 9 esistente indicherà un codice restituito del dispositivo perso in Present.

- Le API Direct3D9Ex e Direct3D 10 possono creare correttamente un dispositivo mentre il desktop protetto è attivo e qualsiasi chiamata a Present ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) o DXGI) restituirà un codice di stato che indica che il desktop non è attualmente disponibile.



 

## <a name="remote-desktop"></a>Desktop remoto

Quando un desktop remoto è attivo, lo schermo viene gestito dal computer di visualizzazione con il computer di hosting che invia informazioni tramite la rete.

Differenze tra XPDM e WDDM:

- In XPDM tutti i tentativi di creare un dispositivo Direct3D 9 in un desktop remoto avranno esito negativo.

- In WDDM Desktop remoto supporta la creazione di un dispositivo HAL in una sessione desktop remoto.



 

## <a name="windows-service"></a>Servizio Windows

Un Windows è un processo che viene eseguito in background, controllato da Gestione controllo servizi. Un servizio viene eseguito indipendentemente dal desktop attivo e pertanto ha una capacità limitata di interagire con gli utenti.

Differenze tra XPDM e WDDM:

- In WDDM, sessione 0 Isolation garantisce che un servizio non abbia accesso ad alcun desktop utente come misura di sicurezza, pertanto un dispositivo Direct3D 9 HAL non è mai disponibile da un servizio Windows.



 

> [!Note]  
> Non è possibile usare Direct3D 9 in un Windows servizio. Per altre informazioni, vedere l'articolo del supporto [tecnico Microsoft 978635](https://support.microsoft.com/kb/978635).

 


La tabella seguente riepiloga le differenze elencate di seguito.



| Desktop sicuro | XPDM | WDDM (Direct3D9) | WDDM(Direct3D9Ex/Direct3D10) |
|-----------------|------|------------------|------------------------------|
| NULLREF         | Sì  | Sì              | Sì                          |
| Hal             | No   | No               | Sì                          |
| REF             | Sì  | Sì              | Sì                          |
| Desktop remoto  |      |                  |                              |
| NULLREF         | No   | Sì              | Sì                          |
| Hal             | No   | Sì              | Sì                          |
| REF             | Sì  | Sì              | Sì                          |
| Servizio Windows |      |                  |                              |
| NULLREF         | No   | No               | No                           |
| Hal             | No   | No               | No                           |
| REF             | No   | No               | No                           |
| WARP10          | N/D  | N/D              | Sì                          |



 

Per altre informazioni su XPDM, WDDM, Direct3D9Ex e Direct3D 10, vedere API grafiche [in Windows](../direct3darticles/graphics-apis-in-windows-vista.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
