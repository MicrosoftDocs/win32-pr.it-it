---
title: Informazioni sul motore di sincronizzazione
description: Informazioni sul motore di sincronizzazione
ms.assetid: bb57ffb0-3833-463b-b66c-c23224fa2ba7
keywords:
- Windows Media Player, motore di sincronizzazione
- Windows Media Player a oggetti, motore di sincronizzazione
- modello a oggetti, motore di sincronizzazione
- Windows Media Player ActiveX, motore di sincronizzazione
- ActiveX, motore di sincronizzazione
- Windows Media Player Controllo del ActiveX mobile, motore di sincronizzazione
- Windows Media Player dispositivi mobili, motore di sincronizzazione
- sincronizzazione di dispositivi, motore di sincronizzazione
- sincronizzazione dei dispositivi, motore di sincronizzazione
- motore di sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ccac14f6416b080ae22407930d720df84bd5b4dc399892b9a2d8678d03eee6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903071"
---
# <a name="about-the-synchronization-engine"></a>Informazioni sul motore di sincronizzazione

Il motore di sincronizzazione è il componente Windows Media Player che gestisce la copia di contenuto multimediale digitale in dispositivi portatili. Windows Media Player supporta una singola istanza del motore di sincronizzazione per ogni dispositivo. È necessario utilizzare un'istanza remota del controllo Windows Media Player per eseguire attività di sincronizzazione a livello di codice. In effetti, il programma condivide le istanze del motore di sincronizzazione con Windows Media Player e tutti gli altri programmi che usano le interfacce del lettore per la sincronizzazione dei dispositivi.

È possibile usare [IWMPSyncDevice::start](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start) e [IWMPSyncDevice::stop](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-stop) per controllare quando il motore di sincronizzazione esegue il proprio lavoro. Nella maggior parte dei casi, non è consigliabile usare questi metodi. È invece consigliabile consentire al motore di sincronizzazione di pianificare automaticamente il proprio lavoro. I **metodi start** e **stop** sono disponibili in modo che sia possibile usarli se il programma è progettato per sostituire il Windows Media Player'interfaccia utente. In questo caso, è possibile specificare un pulsante di avvio/arresto simile a quello Windows Media Player nella **scheda** Dispositivi.

È possibile monitorare lo stato di avanzamento della sincronizzazione per un dispositivo effettuando il polling [di IWMPSyncDevice::get \_ progress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress). Questo metodo recupera un valore di stato per l'intero processo di sincronizzazione con un particolare dispositivo. Il valore recuperato è un numero che rappresenta la percentuale di completamento della sincronizzazione. È possibile ricevere due eventi correlati alla sincronizzazione. **L'evento DeviceSyncError** invia una notifica quando si verifica un problema. **L'evento DeviceSyncStateChange** avvisa l'utente quando lo stato del motore di sincronizzazione per il dispositivo corrente è cambiato.

È possibile limitare la quantità di spazio di archiviazione del dispositivo Windows Media Player per la sincronizzazione chiamando [IWMPSyncDevice2::setItemInfo con](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo) l'attributo **PercentSpaceReserved.** L'uso di questa interfaccia richiede Windows Media Player 11.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sulla sincronizzazione dei dispositivi**](about-device-synchronization.md)
</dt> <dt>

[**Interfaccia IWMPEvents2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**Visualizzazione dello stato di avanzamento della sincronizzazione**](showing-synchronization-progress.md)
</dt> </dl>

 

 




