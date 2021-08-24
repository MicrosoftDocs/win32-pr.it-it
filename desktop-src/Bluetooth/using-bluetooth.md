---
title: Uso di Bluetooth
description: In questa sezione vengono descritte le attività correlate alla scrittura Windows applicazioni basate su Bluetooth.
ms.assetid: a5eddf48-b548-44a8-ac09-ce16f8aa3943
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a80d57d12b2594ab5bbaeb5ad5d026552ab180ae409ba81446288ac396c746a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701831"
---
# <a name="using-bluetooth"></a>Uso di Bluetooth

In questa sezione vengono descritte le attività correlate alla scrittura Windows applicazioni basate su Bluetooth.

Bluetooth le definizioni di programmazione nei file Ws2bth.h e BluetoothAPIs.h. Il file Bthsdpdef.h deve essere incluso prima di BluetoothAPIs.h. Il file Ws2bth.h deve essere incluso dopo Winsock2.h per usare Bluetooth socket. Eseguire il collegamento solo a Bthprops.lib ed evitare il collegamento a Irprops.lib. Irprops.lib viene fornito solo per la compatibilità con le versioni precedenti. Bthprops.lib è disponibile nell'SDK Windows Vista. È possibile usare l'SDK Windows Vista per sviluppare applicazioni per Windows XP con Service Pack 2 (SP2). L Windows SDK di Vista è disponibile [nell'Area download](https://download.microsoft.com/download/a/7/7/a7767f09-0136-4a96-a1f8-276bf0ee31fa/Setup.exe).

Tutti i meccanismi sincroni e sovrapposti standard per leggere e scrivere dati attualmente supportati con altre famiglie di indirizzi funzionano correttamente anche con la famiglia di indirizzi AF \_ BTH.

Nell'SDK è incluso un codice di esempio che illustra una semplice Bluetooth applicazione con Winsock 2.2 e il protocollo RFCOMM. Il codice sorgente per l'esempio è disponibile nel percorso di installazione dell'SDK in C: Programmi \\ Microsoft SDK Windows Samples \\ \\ \\ <version number> \\ \\ NetDs \\ winsock \\ Bluetooth.

In questa sezione vengono descritti gli argomenti seguenti.



| Sezione                                                                                      | Content                                                                          |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Bluetooth Programmazione con Windows socket](bluetooth-programming-with-windows-sockets.md) | Viene illustrato come usare Windows Sockets per implementare una Bluetooth rete. |



 

 

 




