---
description: Persone nelle vicinanze Store
ms.assetid: 3f2aa9bd-49ca-4fa6-b718-7cbeeef857c7
title: Persone nelle vicinanze Store
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 945a49d174f53037427aaa2f45dc0f567dc0acdba57e4a0b0231954e7e66fe90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061379"
---
# <a name="people-near-me-stores"></a>Persone nelle vicinanze Store

Le applicazioni in [grado di Persone nelle vicinanze](about-people-near-me.md) (PNM) possono usare gli archivi dati seguenti:

### <a name="windows-address-book"></a>Windows Rubrica

Il Windows Rubrica archivia le informazioni sui contatti e i relativi certificati digitali. Anche il **contatto 'Me',** che rappresenta l'utente attualmente connesso, viene archiviato nel Windows Rubrica.

### <a name="certificate-store"></a>Archivio certificati

L'archivio certificati contiene il certificato autofirmato per il **contatto 'Me'.**

### <a name="application-store"></a>Archivio applicazioni

Un programma di installazione dell'applicazione registra un'applicazione con PNM durante il processo di installazione. Si tratta degli oggetti che possono essere cercati da altri utenti quando tentano di connettersi a un utente con un'applicazione comune, ad esempio un gioco di computer. Per ogni applicazione, l'archivio applicazioni contiene il nome dell'applicazione, un identificatore univoco globale (GUID), un ambito dell'applicazione, una descrizione e un percorso al file eseguibile del programma. L'ambito di un'applicazione può essere impostato su Nessuno (non annunciato), Persone nelle vicinanze (annunciato nella subnet locale), Contatti (annunciati solo per i contatti) o Tutti (annunciati nella subnet locale e per i contatti). L'archivio applicazioni si trova nel registro Windows Vista.

 

 



