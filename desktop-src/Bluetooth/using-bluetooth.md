---
title: Uso di Bluetooth
description: In questa sezione vengono descritte le attività correlate alla scrittura di applicazioni basate su Windows per Bluetooth.
ms.assetid: a5eddf48-b548-44a8-ac09-ce16f8aa3943
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b9b396de2635f9d1e76005c6638abb1d49c0ff
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734530"
---
# <a name="using-bluetooth"></a>Uso di Bluetooth

In questa sezione vengono descritte le attività correlate alla scrittura di applicazioni basate su Windows per Bluetooth.

Bluetooth fornisce le definizioni di programmazione nei file Ws2bth. h e BluetoothAPIs. h. Il file Bthsdpdef. h deve essere incluso prima di BluetoothAPIs. h. Per usare i Socket Bluetooth, è necessario includere il file Ws2bth. h dopo Winsock2. h. Collegare solo a bthprops. lib ed evitare il collegamento a irprops. lib. Irprops. lib è disponibile solo per compatibilità con le versioni precedenti. Bthprops. lib è disponibile in Windows Vista SDK. È possibile utilizzare Windows Vista SDK per sviluppare applicazioni per Windows XP con Service Pack 2 (SP2). Windows Vista SDK è disponibile nell' [area download](https://download.microsoft.com/download/a/7/7/a7767f09-0136-4a96-a1f8-276bf0ee31fa/Setup.exe).

Tutti i meccanismi sincroni e sovrapposti standard per la lettura e la scrittura di dati attualmente supportati con altre famiglie di indirizzi funzionano correttamente anche con la \_ famiglia di indirizzi AF BTH.

Con l'SDK è incluso un codice di esempio che illustra una semplice applicazione Bluetooth che usa il protocollo Winsock 2,2 e RFCOMM. Il codice sorgente per l'esempio si trova nel percorso di installazione di SDK in C: \\ programmi \\ Microsoft SDK \\ Windows \\ <version number> \\ Samples \\ NetDs \\ Winsock \\ Bluetooth.

In questa sezione vengono descritti gli argomenti seguenti.



| Sezione                                                                                      | Content                                                                          |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Programmazione Bluetooth con Windows Sockets](bluetooth-programming-with-windows-sockets.md) | Viene illustrato come utilizzare le interfacce Windows Sockets per implementare una rete Bluetooth. |



 

 

 




