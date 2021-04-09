---
description: Il codice del pacchetto è un GUID che identifica un particolare pacchetto di Windows Installer.
ms.assetid: dcb6a0d4-e28d-453d-9bda-bfe74f74579b
title: Codici del pacchetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14aa77dbc6c11a1b420572293669a4177f7845ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131471"
---
# <a name="package-codes"></a>Codici del pacchetto

Il codice del pacchetto è un GUID che identifica un particolare [*pacchetto*](p-gly.md)di Windows Installer. Il codice del pacchetto associa un file con estensione msi a un'applicazione o a un prodotto e può essere usato anche per la verifica delle origini. I codici prodotto e pacchetto non sono intercambiabili. Per informazioni dettagliate, vedere [codici prodotto](product-codes.md).

I file con estensione msi non identici non devono avere lo stesso codice del pacchetto. È importante modificare il codice del pacchetto perché è l'identificatore primario usato dal programma di installazione per cercare e convalidare il pacchetto corretto per una determinata installazione. Se un pacchetto viene modificato senza modificare il codice del pacchetto, è possibile che il programma di installazione non usi il pacchetto più recente se entrambi sono ancora accessibili al programma di installazione.

Il codice del pacchetto viene archiviato nella proprietà [**Riepilogo numero revisione**](revision-number-summary.md) del [flusso di informazioni di riepilogo](summary-information-stream.md). Si noti che le lettere nel codice del prodotto e i GUID del codice del pacchetto devono essere in lettere maiuscole. Utilità come GUIDGEN generano GUID contenenti lettere minuscole. Le lettere minuscole in questi GUID devono essere modificate in lettere maiuscole per essere utilizzate come codice del prodotto o codice del pacchetto.

Sebbene sia comune spedire un'applicazione con lo stesso codice del pacchetto e il codice del prodotto, i due valori possono divergere durante l'aggiornamento dell'applicazione. Ad esempio, se si include un nuovo file con l'applicazione, è necessario aggiornare il database di installazione per installare il file. Se le modifiche sono minime, lo sviluppatore può scegliere di non modificare il codice del prodotto, tuttavia è necessario un file con estensione msi diverso per installare il nuovo file e quindi il codice del pacchetto deve essere incrementato. Viceversa, è possibile utilizzare un singolo pacchetto per installare più di un prodotto. Ad esempio, l'installazione di un pacchetto senza una trasformazione lingua potrebbe installare la versione in lingua inglese dell'applicazione e l'installazione dello stesso pacchetto con una trasformazione lingua potrebbe installare la versione francese. La trasformazione è diversa dal file con estensione msi che determina il codice del pacchetto. Le versioni in inglese e in francese potrebbero avere codici di prodotto diversi e lo stesso codice del pacchetto perché sono entrambi installati con lo stesso file con estensione msi.

 

 



