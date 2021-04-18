---
description: Di seguito viene illustrato come organizzare l'applicazione in componenti Windows Installer.
ms.assetid: 981a3def-1e59-4703-ad97-c8cd5431375d
title: Definizione dei componenti del programma di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ade4476fa1bf54a0ab4f64d0d43d72265ac1eb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314292"
---
# <a name="defining-installer-components"></a>Definizione dei componenti del programma di installazione

Di seguito viene illustrato come organizzare l'applicazione in componenti Windows Installer.

**Per organizzare un'applicazione in componenti**

1.  Per iniziare, ottenere una directory e un albero di file per tutti i file e altre risorse usate nell'applicazione.
2.  Identificare i file, le chiavi del registro di sistema, i collegamenti o altre risorse condivise tra le applicazioni e che possono essere forniti dai componenti esistenti disponibili come [moduli unione](merge-modules.md). Non è necessario includere alcuna di queste risorse nei componenti creati. Ottenere invece questi componenti unendo i moduli unione nel pacchetto di installazione. Nei passaggi seguenti viene descritto come organizzare le risorse rimanenti dell'applicazione in componenti.
3.  Definire un nuovo componente per ogni file. exe,. dll e. ocx. Designare questi file come file del percorso della chiave dei relativi componenti. Assegnare a ogni componente un GUID del codice componente.
4.  Definire un nuovo componente per ogni file della guida con estensione hlp o CHM. Designare questi file come file del percorso della chiave dei relativi componenti. Aggiungere i file. cnt o. chi ai componenti che contenevano i file con estensione hlp e chm associati. Assegnare a ogni componente un GUID del codice componente.
5.  Definire un nuovo componente per ogni file che funge da destinazione di un collegamento. Designare questi file come file del percorso della chiave dei relativi componenti. Assegnare a ogni componente un GUID del codice componente.
6.  Raggruppare tutte le risorse rimanenti in cartelle. Tutte le risorse in ogni cartella devono essere fornite insieme. Se esiste la possibilità che una coppia di risorse possa essere distribuita separatamente in futuro, inserirle in cartelle separate. Definire un nuovo componente per ogni cartella. Provare a ridurre il numero totale di componenti per migliorare le prestazioni. Dividere l'applicazione in molti componenti quando è necessario che il programma di installazione verifichi accuratamente la validità dell'installazione. Designare qualsiasi file nel componente come file del percorso della chiave. Assegnare a ogni componente un GUID del codice componente.
7.  Aggiungere le chiavi del registro di sistema ai componenti. Qualsiasi chiave del registro di sistema che punta a un file deve essere inclusa nel componente di tale file. Le altre chiavi del registro di sistema devono essere raggruppate logicamente con i file che li richiedono.

 

 



