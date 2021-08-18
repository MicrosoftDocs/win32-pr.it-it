---
description: "Windows Il programma di installazione consente l'installazione di un'istanza di un codice prodotto per contesto e i due possibili tipi di contesto sono i seguenti: MachineUser Se un codice prodotto rimane invariato, nel contesto del computer può essere installata una sola istanza e in ogni contesto utente può essere installata una sola istanza. Perché più istanze rimangano isolate, devono avere codici prodotto diversi e non possono condividere dati di file o dati non file. Il Windows non può installare più istanze di prodotti usando installazioni simultanee. Tuttavia, è possibile installare più istanze di un prodotto se si dispone di un pacchetto di installazione separato per ogni istanza di un prodotto o di una patch. Ogni pacchetto può quindi mantenere il proprio set di dati e avere un codice prodotto univoco. A partire dal programma di installazione che esegue Windows Server 2003 e Windows XP con Service Pack 1 (SP1), è possibile installare più istanze di un prodotto usando le trasformazioni del codice prodotto e un pacchetto .msi o una patch. È anche possibile usare le trasformazioni del codice prodotto per installare più istanze di un prodotto con Windows 2000 con Service Pack 4 (SP4) e Windows Installer&\\# 160; 3.0. L'unico modo per installare più istanze di un prodotto con versioni precedenti del programma di installazione è disporre di un pacchetto di installazione separato per ogni istanza. L'uso delle trasformazioni di istanza riduce significativamente il lavoro necessario per supportare più istanze di un prodotto. È possibile creare un pacchetto Windows installer di base per un prodotto e quindi più trasformazioni di istanza che modificano il codice del prodotto e gestiscono i dati per ogni istanza. Per altre informazioni, vedere Creazione di più istanze con trasformazioni di istanza e Installazione di più istanze con trasformazioni di istanza."
ms.assetid: 5147ecbd-c395-4a8f-972d-f5c5b2173eff
title: Installazione di più istanze di prodotti e patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6c9f061ef203effc4ec71c386f17a4c92bae957610fdc3a15b0c64a92e1e024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946149"
---
# <a name="installing-multiple-instances-of-products-and-patches"></a>Installazione di più istanze di prodotti e patch

Windows Il programma di installazione consente l'installazione di un'istanza di un codice prodotto per contesto e i due possibili tipi di contesto sono i seguenti:

-   Computer
-   Utente

Se un codice prodotto rimane invariato, è possibile installare una sola istanza nel contesto del computer e una sola istanza può essere installata in ogni contesto utente.

Perché più istanze rimangano isolate, devono avere codici prodotto diversi e non possono condividere dati di file o dati non file. Il Windows non può installare più istanze di prodotti usando [installazioni simultanee.](concurrent-installations.md) Tuttavia, è possibile installare più istanze di un prodotto se si dispone di un pacchetto di installazione separato per ogni istanza di un prodotto o di una patch. Ogni pacchetto può quindi mantenere il proprio set di dati e avere un codice prodotto univoco.

A partire dal programma di installazione che esegue Windows Server 2003 e Windows XP con Service Pack 1 (SP1), è possibile installare più istanze di un prodotto usando le trasformazioni del codice prodotto e un pacchetto .msi o una patch. È anche possibile usare le trasformazioni del codice prodotto per installare più istanze di un prodotto con Windows 2000 con Service Pack 4 (SP4) e Windows Installer 3.0. L'unico modo per installare più istanze di un prodotto con versioni precedenti del programma di installazione è disporre di un pacchetto di installazione separato per ogni istanza.

L'uso delle trasformazioni di istanza riduce significativamente il lavoro necessario per supportare più istanze di un prodotto. È possibile creare un pacchetto Windows installer di base per un prodotto e quindi più trasformazioni di istanza che modificano il codice del prodotto e gestiscono i dati per ogni istanza.

Per altre informazioni, vedere [Creazione di più istanze](authoring-multiple-instances-with-instance-transforms.md) con trasformazioni di istanza e Installazione di più istanze con trasformazioni di [istanza](installing-multiple-instances-with-instance-transforms.md).

 

 



