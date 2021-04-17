---
title: Informazioni sul motore di sincronizzazione
description: Informazioni sul motore di sincronizzazione
ms.assetid: bb57ffb0-3833-463b-b66c-c23224fa2ba7
keywords:
- Windows Media Player, motore di sincronizzazione
- Modello a oggetti di Windows Media Player, motore di sincronizzazione
- modello a oggetti, motore di sincronizzazione
- Controllo ActiveX di Windows Media Player, motore di sincronizzazione
- Controllo ActiveX, motore di sincronizzazione
- Controllo ActiveX Windows Media Player Mobile, motore di sincronizzazione
- Windows Media Player Mobile, motore di sincronizzazione
- sincronizzazione di dispositivi, motore di sincronizzazione
- sincronizzazione dei dispositivi, motore di sincronizzazione
- motore di sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe0768c4805b074fdaf628a25daf47b9ced97ee
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398602"
---
# <a name="about-the-synchronization-engine"></a>Informazioni sul motore di sincronizzazione

Il motore di sincronizzazione è il componente di Windows Media Player che gestisce la copia del contenuto multimediale digitale nei dispositivi portatili. Windows Media Player supporta una singola istanza del motore di sincronizzazione per ogni dispositivo. Per eseguire attività di sincronizzazione a livello di programmazione, è necessario utilizzare un'istanza remota del controllo Media Player di Windows. In effetti, il programma condivide le istanze del motore di sincronizzazione con Windows Media Player e tutti gli altri programmi che usano le interfacce del lettore per la sincronizzazione dei dispositivi.

È possibile usare [IWMPSyncDevice:: Start](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start) e [IWMPSyncDevice:: Stop](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-stop) per controllare il momento in cui il motore di sincronizzazione esegue le operazioni. Nella maggior parte dei casi, non è consigliabile usare questi metodi. Al contrario, è necessario consentire al motore di sincronizzazione di pianificare automaticamente il lavoro. I metodi **Start** e **Stop** esistono per poterli utilizzare se il programma è stato progettato per sostituire l'interfaccia utente di Windows Media Player. In questo caso, è possibile fornire un pulsante di avvio/arresto simile a quello di Windows Media Player disponibile nella scheda **dispositivi** .

È possibile monitorare lo stato di avanzamento della sincronizzazione per un dispositivo eseguendo il polling di [IWMPSyncDevice:: Get \_ Progress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress). Questo metodo recupera un valore di avanzamento per l'intero processo di sincronizzazione con un dispositivo specifico. Il valore recuperato è un numero che rappresenta la percentuale di completamento della sincronizzazione. Sono disponibili due eventi che è possibile ricevere correlati alla sincronizzazione. L'evento **DeviceSyncError** informa l'utente quando si verifica un problema. L'evento **DeviceSyncStateChange** avvisa l'utente quando il motore di sincronizzazione ha modificato lo stato per il dispositivo corrente.

È possibile limitare la quantità di archiviazione del dispositivo utilizzata da Windows Media Player per la sincronizzazione chiamando [IWMPSyncDevice2:: setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo) con l'attributo **PercentSpaceReserved** . L'utilizzo di questa interfaccia richiede Windows Media Player 11.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sulla sincronizzazione dei dispositivi**](about-device-synchronization.md)
</dt> <dt>

[**Interfaccia IWMPEvents2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**Visualizzazione dello stato di avanzamento della sincronizzazione**](showing-synchronization-progress.md)
</dt> </dl>

 

 




