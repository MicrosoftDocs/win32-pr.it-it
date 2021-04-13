---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: d317d052-c207-412a-896e-09cb57b0dd5f
title: Parametri nel documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ecfcfee581014bdb57ff70adebaf5f4c8b6fedc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351831"
---
# <a name="parameters-in-the-printcapabilities-document"></a>Parametri nel documento PrintCapabilities

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Come illustrato negli [elementi di riferimento ai parametri](parameter-reference-elements.md), è possibile fare riferimento agli elementi ParameterInit all'interno di istanze di opzioni, ma anche il costrutto di parametro ha un uso indipendente da questo tipo di elemento.

Un esempio di attributo di configurazione del dispositivo particolarmente adatto per la rappresentazione del parametro è CopyCount. I valori consentiti per questo attributo di configurazione del dispositivo possono essere definiti in modo semplice e conciso senza elencarli singolarmente. Sebbene sarebbe possibile, sebbene noioso, elencare ogni valore CopyCount nella propria opzione, alcuni attributi di configurazione del dispositivo semplicemente non possono essere rappresentati usando un costrutto di funzionalità o opzione. Ad esempio, si consideri un dispositivo che accetta una stringa di testo che viene quindi usata per produrre una filigrana virtuale in ogni pagina di output. Il set di tutte le stringhe di testo possibili non può essere facilmente enumerato in modo esplicito, ma la stringa di testo può essere facilmente descritta utilizzando un elemento ParameterDef.

Il documento parole chiave dello schema di stampa definisce un numero di costrutti di parametri comunemente utilizzati, ma i provider PrintCapabilities sono liberi di definire quelli più comuni. Tuttavia, questi costrutti di parametro definiti privatamente non sono portabili ad altri dispositivi, a causa del fatto che un documento PrintCapabilities fornito da un'altra parte non definisce tale costrutto di parametro. Se definito dallo schema o privato, l'istanza di ParameterDef deve essere presente nel documento PrintCapabilities prima che il parametro venga riconosciuto e utilizzato dai client. Questi parametri sono detti *parametri designati*.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



