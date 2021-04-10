---
description: Negozi di persone nelle vicinanze
ms.assetid: 3f2aa9bd-49ca-4fa6-b718-7cbeeef857c7
title: Negozi di persone nelle vicinanze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d18bf60e43aba278862fbd19f3c8909e344bc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883338"
---
# <a name="people-near-me-stores"></a>Negozi di persone nelle vicinanze

Le applicazioni in grado di [persone nelle vicinanze](about-people-near-me.md) (persone nelle vicinanze) possono usare gli archivi dati seguenti:

### <a name="windows-address-book"></a>Rubrica di Windows

La Rubrica di Windows archivia le informazioni sui contatti e i relativi certificati digitali. Il contatto "**me**", che rappresenta l'utente attualmente connesso, viene archiviato anche nella Rubrica di Windows.

### <a name="certificate-store"></a>Archivio certificati

L'archivio certificati contiene il certificato autofirmato per il contatto "**me**".

### <a name="application-store"></a>Archivio applicazioni

Un programma di installazione dell'applicazione registra un'applicazione con persone nelle vicinanze durante il processo di installazione. Si tratta degli oggetti che possono essere cercati da altri utenti durante il tentativo di connessione a un utente con un'applicazione comune, ad esempio un gioco per computer. Per ogni applicazione, l'archivio applicazioni contiene il nome dell'applicazione, un identificatore univoco globale (GUID), un ambito dell'applicazione, una descrizione e un percorso del file eseguibile del programma. L'ambito di un'applicazione può essere impostato su None (non annunciato), persone nelle vicinanze (annunciate nella subnet locale), contatti (annunciati solo per contatti) o tutti (annunciati nella subnet locale e per i contatti). L'archivio applicazioni si trova nel registro di sistema di Windows Vista.

 

 



