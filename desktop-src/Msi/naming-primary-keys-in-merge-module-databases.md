---
description: I nomi delle chiavi primarie devono essere conformi a una convenzione di denominazione standard.
ms.assetid: 72822c25-cd21-454b-ab49-846474b55ef1
title: Denominazione di chiavi primarie nei database del modulo merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e5481e7fd29c4d3750e8fac01b6ca4bd6593af3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528177"
---
# <a name="naming-primary-keys-in-merge-module-databases"></a>Denominazione di chiavi primarie nei database del modulo merge

I nomi delle chiavi primarie devono essere conformi a una convenzione di denominazione standard. Lo scopo di questa convenzione di denominazione è ridurre la possibilità di creare un conflitto di nomi tra le colonne della tabella nel modulo merge e il pacchetto di installazione di destinazione. La convenzione di denominazione non può essere applicata alle tabelle in cui la chiave primaria è installabile. Non applicare la convenzione di denominazione alle tabelle seguenti:

-   [Tabella MIME](mime-table.md)
-   [Tabella di estensione](extension-table.md)
-   [Icona tabella](icon-table.md)
-   [Tabella Verb](verb-table.md)
-   [Tabella ProgId](progid-table.md)

Ad esempio, non utilizzare per la chiave primaria della tabella MIME perché si tratta del tipo MIME e l'applicazione della procedura di denominazione ne modifica il significato. In questi casi, i conflitti di nome dipendono dal significato dei dati univoci tra i moduli.

Il nome di una chiave primaria in un modulo merge deve essere costituito da un nome leggibile accodato con una stringa creata dal GUID del modulo merge. Ogni modulo merge deve avere un proprio [*GUID*](g-gly.md). Il GUID del modulo di merge deve essere creato anche nella proprietà di [**Riepilogo dei numeri di revisione**](revision-number-summary.md) del modulo merge. Gli sviluppatori possono creare GUID usando un'utilità, ad esempio GUIDGEN.

Nella procedura riportata di seguito viene descritto come generare una chiave del database primaria conforme alla convenzione di denominazione standard. Applicare la procedura seguente solo alle tabelle in cui la chiave primaria non è installata.

**Per assegnare un nome a una chiave primaria di un record di tabella in un modulo merge**

1.  Creazione della parte leggibile del nome per la chiave primaria. Selezionare un nome leggibile che identifichi questo record, ad esempio MyRowEntry.
2.  Generare o ottenere il GUID del modulo merge. Si noti che tutti i GUID devono essere creati in maiuscolo. Per ulteriori informazioni sui GUID, vedere [GUID](guid.md). Di seguito è riportato un esempio di GUID: {880DE2F0-CDD8-11D1-A849-006097ABDE17}. Nei passaggi seguenti si modifica questa operazione in una stringa di caratteri che deve essere aggiunta a ogni nome di chiave primaria nel modulo merge.
3.  Rimuovere le parentesi graffe dall'inizio e dalla fine del GUID.
4.  Modificare tutti i trattini in caratteri di sottolineatura.
5.  Aggiungere il risultato alla fine della parte leggibile del nome della chiave primaria. Separare il nome leggibile dal GUID modificato per un punto. Il nome della chiave primaria per il GUID di esempio specificato in precedenza diventa MyRowEntry. 880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.
6.  Ripetere l'operazione per assegnare un nome a tutte le chiavi primarie di tutte le tabelle del modulo merge.

 

 



