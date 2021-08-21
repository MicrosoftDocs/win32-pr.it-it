---
description: Informazioni sui parametri nel documento PrintCapabilities. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: d317d052-c207-412a-896e-09cb57b0dd5f
title: Parametri nel documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a2d88e75372cfc2f1301c630116c12510b37c91aadbf94a04ac07a3f4906cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117867993"
---
# <a name="parameters-in-the-printcapabilities-document"></a>Parametri nel documento PrintCapabilities

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Come illustrato in [Elementi di riferimento](parameter-reference-elements.md)ai parametri, è possibile fare riferimento agli elementi ParameterInit dall'interno di istanze Option, ma anche il costrutto di parametro ha un uso indipendente da questo tipo di elemento.

Un esempio di attributo di configurazione del dispositivo adatto per la rappresentazione dei parametri è CopyCount. I valori consentiti per questo attributo di configurazione del dispositivo possono essere definiti in modo semplice e conciso senza elencarli in modo esplicito. Anche se sarebbe possibile, anche se noioso, elencare ogni valore CopyCount nella propria opzione, alcuni attributi di configurazione del dispositivo semplicemente non possono essere rappresentati usando un costrutto Feature/Option. Si consideri ad esempio un dispositivo che accetta una stringa di testo che viene quindi usata per produrre una filigrana virtuale in ogni pagina di output. Il set di tutte le stringhe di testo possibili non può essere enumerato in modo esplicito, ma la stringa di testo può essere descritta facilmente usando un elemento ParameterDef.

Il documento Parole chiave dello schema di stampa definisce una serie di costrutti di parametro di uso comune, ma i provider PrintCapabilities sono liberi di definire altri costrutti personalizzati. Tuttavia, questi costrutti di parametro definiti privatamente non sono portabili ad altri dispositivi, a causa del fatto che un documento PrintCapabilities fornito da un'altra parte non definisce tale costrutto di parametro. Indipendentemente dal fatto che lo schema venga definito o definito privatamente, l'istanza ParameterDef deve essere presente nel documento PrintCapabilities prima che il parametro venga riconosciuto e usato dai client. Questi parametri vengono definiti *parametri designati*.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



