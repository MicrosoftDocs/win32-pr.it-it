---
description: "Windows Installer consente l'installazione di un'istanza di un codice prodotto per contesto e i due tipi di contesto possibili sono i seguenti: MachineUser se un codice prodotto rimane invariato, è possibile installare una sola istanza nel contesto del computer ed è possibile installare una sola istanza in ogni contesto utente. Affinché più istanze rimangano isolate, devono avere codici di prodotto diversi e non possono condividere dati di file o dati non di file. Il Windows Installer non può installare più istanze di prodotti usando installazioni simultanee. Tuttavia, è possibile installare più istanze di un prodotto se si dispone di un pacchetto di installazione separato per ogni istanza di un prodotto o di una patch. Ogni pacchetto può quindi contenere un proprio set di dati e avere un proprio codice prodotto univoco. A partire dal programma di installazione che esegue Windows Server 2003 e Windows XP con Service Pack 1 (SP1), è possibile installare più istanze di un prodotto utilizzando le trasformazioni del codice prodotto e un pacchetto con estensione msi o una patch. È inoltre possibile utilizzare le trasformazioni del codice prodotto per installare più istanze di un prodotto con Windows 2000 con Service Pack 4 (SP4) e Windows Installer&\\# 160; 3,0. L'unico modo per installare più istanze di un prodotto con versioni precedenti del programma di installazione è disporre di un pacchetto di installazione separato per ogni istanza. L'utilizzo delle trasformazioni dell'istanza riduce significativamente lo sforzo necessario per supportare più istanze di un prodotto. È possibile creare un pacchetto di base Windows Installer per un prodotto e quindi più trasformazioni di istanza che modificano il codice del prodotto e gestiscono i dati per ogni istanza. Per ulteriori informazioni, vedere la pagina relativa alla creazione di più istanze con trasformazioni di istanza e all'installazione di più istanze con trasformazioni dell'istanza."
ms.assetid: 5147ecbd-c395-4a8f-972d-f5c5b2173eff
title: Installazione di più istanze di prodotti e patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a3a1de5de7cc63d5eed2e191d77915630761561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233509"
---
# <a name="installing-multiple-instances-of-products-and-patches"></a>Installazione di più istanze di prodotti e patch

Windows Installer consente l'installazione di un'istanza di un codice prodotto per contesto e i due tipi di contesto possibili sono i seguenti:

-   Computer
-   Utente

Se il codice di un prodotto rimane invariato, è possibile installare una sola istanza nel contesto del computer ed è possibile installare una sola istanza in ogni contesto utente.

Affinché più istanze rimangano isolate, devono avere codici di prodotto diversi e non possono condividere dati di file o dati non di file. Il Windows Installer non può installare più istanze di prodotti usando [installazioni simultanee](concurrent-installations.md). Tuttavia, è possibile installare più istanze di un prodotto se si dispone di un pacchetto di installazione separato per ogni istanza di un prodotto o di una patch. Ogni pacchetto può quindi contenere un proprio set di dati e avere un proprio codice prodotto univoco.

A partire dal programma di installazione che esegue Windows Server 2003 e Windows XP con Service Pack 1 (SP1), è possibile installare più istanze di un prodotto utilizzando le trasformazioni del codice prodotto e un pacchetto con estensione msi o una patch. È inoltre possibile utilizzare le trasformazioni del codice prodotto per installare più istanze di un prodotto con Windows 2000 con Service Pack 4 (SP4) e Windows Installer 3,0. L'unico modo per installare più istanze di un prodotto con versioni precedenti del programma di installazione è disporre di un pacchetto di installazione separato per ogni istanza.

L'utilizzo delle trasformazioni dell'istanza riduce significativamente lo sforzo necessario per supportare più istanze di un prodotto. È possibile creare un pacchetto di base Windows Installer per un prodotto e quindi più trasformazioni di istanza che modificano il codice del prodotto e gestiscono i dati per ogni istanza.

Per ulteriori informazioni, vedere la pagina relativa alla [creazione di più istanze con trasformazioni di istanza](authoring-multiple-instances-with-instance-transforms.md) e [all'installazione di più istanze con trasformazioni dell'istanza](installing-multiple-instances-with-instance-transforms.md).

 

 



