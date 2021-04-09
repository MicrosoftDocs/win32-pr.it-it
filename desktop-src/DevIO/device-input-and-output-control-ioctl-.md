---
description: La funzione DeviceIoControl fornisce un'interfaccia IOCTL (device input and Output Control) attraverso la quale un'applicazione può comunicare direttamente con un driver di dispositivo.
ms.assetid: 2dffd86a-162c-4e09-bfa1-73b87522741a
title: Controllo di input e output del dispositivo (IOCTL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce2bb2ee26c63c2aad02d8e8d167ff12383fc6b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878130"
---
# <a name="device-input-and-output-control-ioctl"></a>Controllo di input e output del dispositivo (IOCTL)

La funzione [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) fornisce un'interfaccia IOCTL (device input and Output Control) attraverso la quale un'applicazione può comunicare direttamente con un driver di dispositivo. La funzione **DeviceIoControl** è un'interfaccia generica che può inviare codici di controllo a un'ampia gamma di dispositivi. Ogni codice di controllo rappresenta un'operazione che deve essere eseguita dal driver. Ad esempio, un codice di controllo può chiedere a un driver di dispositivo di restituire informazioni sul dispositivo corrispondente o indirizzare il driver per eseguire un'azione sul dispositivo, ad esempio la formattazione di un disco.

Nei file di intestazione dell'SDK sono definiti diversi codici di controllo standard. Inoltre, i driver di dispositivo possono definire i propri codici di controllo specifici del dispositivo. Per un elenco dei codici di controllo standard inclusi nella documentazione di SDK, vedere la sezione Osservazioni di [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol).

I tipi di codici di controllo che è possibile specificare dipendono dal dispositivo a cui si accede e dalla piattaforma in cui è in esecuzione l'applicazione. Le applicazioni possono utilizzare i codici di controllo standard o i codici di controllo specifici del dispositivo per eseguire operazioni di input e output dirette su un'unità disco floppy, un'unità disco rigido, un'unità nastro o un'unità CD-ROM.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Chiamata di DeviceIoControl](calling-deviceiocontrol.md)
</dt> </dl>

 

 
