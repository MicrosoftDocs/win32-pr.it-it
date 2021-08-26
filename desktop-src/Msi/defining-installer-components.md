---
description: Di seguito viene descritto come organizzare l'applicazione in componenti Windows Installer.
ms.assetid: 981a3def-1e59-4703-ad97-c8cd5431375d
title: Definizione dei componenti del programma di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ae83d5fa02182c40fa209453484db23706db2f261f41324cd4d86894d9e78dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979561"
---
# <a name="defining-installer-components"></a>Definizione dei componenti del programma di installazione

Di seguito viene descritto come organizzare l'applicazione in componenti Windows Installer.

**Per organizzare un'applicazione in componenti**

1.  Per iniziare, ottenere una directory e un albero di file per tutti i file e altre risorse usate nell'applicazione.
2.  Identificare i file, le chiavi del Registro di sistema, i collegamenti o altre risorse condivisi tra le applicazioni e che possono essere forniti dai componenti esistenti disponibili come [moduli unione.](merge-modules.md) Non è necessario includere nessuna di queste risorse nei componenti creati. È invece possibile ottenere questi componenti unendo i moduli unione nel pacchetto di installazione. I passaggi seguenti descrivono come organizzare le risorse rimanenti dell'applicazione in componenti.
3.  Definire un nuovo componente per ogni .exe, .dll file con estensione ocx. Designare questi file come file di percorso della chiave dei relativi componenti. Assegnare a ogni componente un GUID del codice componente.
4.  Definire un nuovo componente per ogni file della Guida con estensione hlp o chm. Designare questi file come file di percorso della chiave dei relativi componenti. Aggiungere i file con estensione cnt o chi ai componenti che contiene i file con estensione hlp e chm associati. Assegnare a ogni componente un GUID del codice componente.
5.  Definire un nuovo componente per ogni file che funge da destinazione di un collegamento. Designare questi file come file di percorso della chiave dei relativi componenti. Assegnare a ogni componente un GUID del codice componente.
6.  Raggruppare tutte le risorse rimanenti in cartelle. Tutte le risorse in ogni cartella devono essere spediscono insieme. Se esiste la possibilità che una coppia di risorse possa essere spedita separatamente in futuro, inserire tali risorse in cartelle separate. Definire un nuovo componente per ogni cartella. Provare a mantenere basso il numero totale di componenti per migliorare le prestazioni. Dividere l'applicazione in molti componenti quando è necessario che il programma di installazione controlli accuratamente la validità dell'installazione. Designare qualsiasi file nel componente come file del percorso della chiave. Assegnare a ogni componente un GUID del codice componente.
7.  Aggiungere le chiavi del Registro di sistema ai componenti. Qualsiasi chiave del Registro di sistema che punta a un file deve essere inclusa nel componente del file. Le altre chiavi del Registro di sistema devono essere raggruppate logicamente con i file che le richiedono.

 

 



