---
description: Quando un thread comunica attivamente con un dispositivo wia (Windows Image Acquisition), ad esempio il trasferimento di dati o la scrittura di proprietà del dispositivo, WIA &\# 0034; blocca&\# 0034; il dispositivo.
ms.assetid: 59533937-284a-4732-a73b-d2e0b5a9a370
title: Comunicazione con un dispositivo WIA in più thread o applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f54cc8fe9a3b60d684ff9a62def2c0cf8862576034b16f58d3dd369d2b8be0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118209265"
---
# <a name="communicating-with-a-wia-device-in-multiple-threads-or-applications"></a>Comunicazione con un dispositivo WIA in più thread o applicazioni

Quando un thread comunica attivamente con un dispositivo WIA (Windows Image Acquisition), ad esempio il trasferimento di dati o la scrittura di proprietà del dispositivo, WIA "blocca" il dispositivo. Quando un dispositivo è bloccato, nessun altro thread o processo può comunicare attivamente con tale dispositivo.

WiA non impedisce a più thread o processi di mantenere le connessioni a un singolo dispositivo. In altre informazioni, un dispositivo viene bloccato solo durante la comunicazione effettiva e due o più applicazioni possono avere contemporaneamente selezionato un singolo dispositivo.

WIA crea un albero di elementi separato ogni volta che un thread o un'applicazione chiama [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) o [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md) per creare un'istanza di tale dispositivo. WIA gestisce informazioni sullo stato separate per ogni albero degli elementi. Ad esempio, se un thread crea due istanze di un determinato scanner, può impostare risoluzioni di analisi diverse per le due istanze. Quando [**IWiaDataTransfer::idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) viene chiamato in una determinata istanza, WIA carica le proprietà associate a tale istanza nel dispositivo prima che venga eseguita l'analisi effettiva. Ciò non influisce sullo stato dell'altra istanza del dispositivo.

Se un thread attualmente ha un dispositivo bloccato (comunica attivamente con tale dispositivo) e un altro thread tenta di chiamare un metodo che comunica attivamente con il dispositivo, il metodo restituisce un errore WIA \_ ERROR \_ BUSY.

In genere, la lettura e la scrittura delle proprietà del dispositivo richiedono così poco tempo che queste operazioni raramente causano un conflitto. Il trasferimento dei dati, tuttavia, richiede in genere più tempo e pertanto è più probabile che si creino conflitti di accesso ai dispositivi. È una programmazione valida per evitare lunghe operazioni sui dispositivi (trasferimenti di dati) contemporaneamente in thread separati all'interno di un'applicazione.

Un'applicazione non deve mai presupporre che sia l'unica applicazione che comunica con un dispositivo WIA all'avvio.

 

 



