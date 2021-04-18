---
description: L'API Direct3D 9 funziona in Windows XP Display Driver Model (XPDM) o in Windows Vista Display Driver Model (WDDM), a seconda del sistema operativo installato.
ms.assetid: b552c822-aa01-4f1d-a0a6-1411ab006e7b
title: Confronto tra XPDM e WDDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccdf4bba28b53959d8e86d8928c786db3b1d0c7f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303792"
---
# <a name="xpdm-vs-wddm"></a>Confronto tra XPDM e WDDM

L'API Direct3D 9 funziona in Windows XP Display Driver Model (XPDM) o in Windows Vista Display Driver Model (WDDM), a seconda del sistema operativo installato. Esistono alcune differenze nel modo in cui l'API Direct3D si comporta sui due modelli di driver.

-   [Desktop protetto](#secure-desktop)
-   [Desktop remoto](#remote-desktop)
-   [Servizio Windows](#windows-service)
-   [Argomenti correlati](#related-topics)

## <a name="secure-desktop"></a>Desktop protetto

Il desktop protetto è attivo ogni volta che si verifica una delle condizioni seguenti: l'utente blocca il desktop (Windows + L), il screen saver viene attivato (quando nessun utente è connesso) o per impostazione predefinita quando il controllo dell'account utente visualizza un messaggio di richiesta. Quando il desktop protetto è attivo, il dispositivo HAL non è accessibile.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra XPDM e WDDM:<br/> Il tentativo di creare un dispositivo HAL Direct3D9 avrà esito negativo (con **D3DERR \_ non \_ disponibile**) e qualsiasi dispositivo Direct3D 9 esistente indicherà che è presente un codice di ritorno del dispositivo perso.<br/> Le API Direct3D9Ex e Direct3D 10 possono creare correttamente un dispositivo mentre il desktop protetto è attivo e tutte le chiamate a presenti ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) o DXGI) restituiranno un codice di stato che indica che il desktop non è al momento disponibile.<br/> |



 

## <a name="remote-desktop"></a>Desktop remoto

Quando un desktop remoto è attivo, la visualizzazione viene gestita dal computer di visualizzazione con il computer di hosting che invia le informazioni tramite la rete.



|                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra XPDM e WDDM:<br/> In XPDM tutti i tentativi di creare un dispositivo Direct3D 9 in un desktop remoto avranno esito negativo.<br/> In WDDM, desktop remoto supporta la creazione di un dispositivo HAL su una sessione Desktop remoto.<br/> |



 

## <a name="windows-service"></a>Servizio Windows

Un servizio Windows è un processo eseguito in background, controllato da Gestione controllo servizi (SCM). Un servizio viene eseguito indipendentemente dal desktop attivo e pertanto ha una capacità limitata di interagire con gli utenti.



|                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra XPDM e WDDM:<br/> In WDDM l'isolamento della sessione 0 garantisce che un servizio non disponga dell'accesso a un desktop utente come misura di sicurezza, pertanto un dispositivo Direct3D 9 HAL non sarà mai disponibile da un servizio Windows.<br/> |



 

> [!Note]  
> Non è possibile usare Direct3D 9 in un servizio Windows. Per ulteriori informazioni, vedere l' [articolo 978635 del supporto tecnico Microsoft](https://support.microsoft.com/kb/978635).

 


Nella tabella seguente sono riepilogate le differenze elencate di seguito.



|                 | XPDM | WDDM (Direct3D9) | WDDM (Direct3D9Ex/Direct3D10) |
|-----------------|------|------------------|------------------------------|
| Desktop protetto  |      |                  |                              |
| NULLREF         | Sì  | Sì              | Sì                          |
| HAL             | No   | No               | Sì                          |
| REF             | Sì  | Sì              | Sì                          |
| Desktop remoto  |      |                  |                              |
| NULLREF         | No   | Sì              | Sì                          |
| HAL             | No   | Sì              | Sì                          |
| REF             | Sì  | Sì              | Sì                          |
| Servizio Windows |      |                  |                              |
| NULLREF         | No   | No               | No                           |
| HAL             | No   | No               | No                           |
| REF             | No   | No               | No                           |
| WARP10          | N/D  | N/D              | Sì                          |



 

Per altre informazioni su XPDM, WDDM, Direct3D9Ex e Direct3D 10, vedere [API grafiche in Windows](../direct3darticles/graphics-apis-in-windows-vista.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
