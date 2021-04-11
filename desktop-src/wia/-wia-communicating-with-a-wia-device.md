---
description: Quando un thread comunica attivamente con un dispositivo Windows Image Acquisition (WIA) (ad esempio, il trasferimento di dati o la scrittura di proprietà del dispositivo) WIA &\# 0034; locks&\# 0034; il dispositivo.
ms.assetid: 59533937-284a-4732-a73b-d2e0b5a9a370
title: Comunicazione con un dispositivo WIA in più thread o applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7a4b518093c3a0fc09534d67e22e5349d44d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231559"
---
# <a name="communicating-with-a-wia-device-in-multiple-threads-or-applications"></a>Comunicazione con un dispositivo WIA in più thread o applicazioni

Quando un thread comunica attivamente con un dispositivo Windows Image Acquisition (WIA) (ad esempio, il trasferimento di dati o la scrittura di proprietà del dispositivo) WIA "blocca" il dispositivo. Quando un dispositivo è bloccato, nessun altro thread o processo può comunicare attivamente con tale dispositivo.

WIA non impedisce a più thread o processi di mantenere le connessioni a un singolo dispositivo. Ovvero, un dispositivo viene bloccato solo durante la comunicazione effettiva e due o più applicazioni possono avere contemporaneamente un singolo dispositivo selezionato.

WIA crea un albero degli elementi separato ogni volta che un thread o un'applicazione chiama [**IWiaDevMgr:: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) o [**IWiaDevMgr2:: CreateDevice**](-wia-iwiadevmgr2-createdevice.md) per creare un'istanza del dispositivo. WIA mantiene le informazioni di stato separate per ogni albero degli elementi. Se, ad esempio, un thread crea due istanze di un particolare scanner, può impostare risoluzioni di analisi diverse per le due istanze. Quando [**IWiaDataTransfer:: idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) viene chiamato su una particolare istanza, WIA carica le proprietà associate a tale istanza nel dispositivo prima che venga eseguita l'analisi effettiva. Questo non influisce sullo stato dell'altra istanza del dispositivo.

Se un thread dispone attualmente di un dispositivo bloccato (sta comunicando attivamente con tale dispositivo) e un altro thread tenta di chiamare un metodo che comunica attivamente con il dispositivo, il metodo restituisce \_ un \_ errore WIA occupato.

In genere, la lettura e la scrittura delle proprietà del dispositivo richiedono poco tempo che queste operazioni causino raramente un conflitto. Il trasferimento dei dati, tuttavia, richiede in genere più tempo ed è quindi più probabile che si creino conflitti di accesso ai dispositivi. Si tratta di una programmazione audio che consente di evitare lunghe operazioni del dispositivo (trasferimenti di dati) contemporaneamente in thread distinti all'interno di un'applicazione.

Un'applicazione non deve mai presupporre che sia l'unica applicazione che comunica con un dispositivo WIA all'avvio.

 

 



