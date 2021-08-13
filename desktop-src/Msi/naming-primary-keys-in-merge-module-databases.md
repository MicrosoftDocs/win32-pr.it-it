---
description: I nomi delle chiavi primarie di un database del modulo unione devono essere conformi a una convenzione di denominazione standard.
ms.assetid: 72822c25-cd21-454b-ab49-846474b55ef1
title: Denominazione delle chiavi primarie nei database del modulo di unione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b5ab2f7dbb5a41f5999271e5c679b67c6ee37d9b79302509ef61e9dbca97894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627809"
---
# <a name="naming-primary-keys-in-merge-module-databases"></a>Denominazione delle chiavi primarie nei database del modulo di unione

I nomi delle chiavi primarie di un database del modulo unione devono essere conformi a una convenzione di denominazione standard. Lo scopo di questa convenzione di denominazione è ridurre la possibilità di creare un conflitto di nomi tra le colonne della tabella nel modulo di unione e il pacchetto di installazione di destinazione. La convenzione di denominazione non può essere applicata alle tabelle in cui la chiave primaria è dati installabili. Non applicare la convenzione di denominazione alle tabelle seguenti:

-   [Tabella MIME](mime-table.md)
-   [Tabella delle estensioni](extension-table.md)
-   [Tabella delle icone](icon-table.md)
-   [Tabella verbi](verb-table.md)
-   [Tabella ProgId](progid-table.md)

Ad esempio, non utilizzare per la chiave primaria della tabella MIME perché si tratta del tipo MIME e l'applicazione della procedura di denominazione ne modifica il significato. In questi casi, i conflitti di nomi dipendono dal significato dei dati univoci tra i moduli.

Il nome di una chiave primaria in un modulo di unione deve essere costituito da un nome leggibile accodato a una stringa costituita dal GUID del modulo di merge. Ogni modulo unione deve avere il proprio [*GUID*](g-gly.md). Il GUID del modulo unione deve essere creato anche nella proprietà [**Riepilogo numero**](revision-number-summary.md) revisione del modulo unione. Gli sviluppatori possono creare GUID usando un'utilità come GUIDGEN.

Nella procedura seguente viene descritto come generare una chiave del database primario conforme alla convenzione di denominazione standard. Applicare la procedura seguente solo alle tabelle in cui la chiave primaria non è in fase di installazione.

**Per assegnare un nome a una chiave primaria di un record di tabella in un modulo unione**

1.  Creare la parte leggibile del nome per la chiave primaria. Selezionare un nome leggibile che identifichi questo record, ad esempio MyRowEntry.
2.  Generare o ottenere il GUID del modulo di merge. Si noti che tutti i GUID devono essere creati in maiuscolo. Per altre informazioni sui GUID, vedere [GUID](guid.md). Di seguito è riportato un esempio di GUID: {880DE2F0-CDD8-11D1-A849-006097ABDE17}. Nei passaggi seguenti viene modificato in una stringa di caratteri che deve essere aggiunta a ogni nome di chiave primaria nel modulo di unione.
3.  Rimuovere le parentesi graffe dall'inizio e dalla fine del GUID.
4.  Modificare tutti i trattini in caratteri di sottolineatura.
5.  Aggiungere il risultato alla fine della parte leggibile del nome della chiave primaria. Separare il nome leggibile dal GUID modificato da un punto. Il nome della chiave primaria per il GUID di esempio indicato in precedenza diventa MyRowEntry.880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.
6.  Ripetere questa operazione per assegnare un nome a tutte le chiavi primarie di tutte le tabelle nel modulo di unione.

 

 



