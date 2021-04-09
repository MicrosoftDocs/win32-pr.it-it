---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: ea75a7ac-d4d7-42b6-91e9-e28607fd684c
title: Utilizzi dell'oggetto PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63dda5b21d1472ec8d4162c8d7229ff47264fb55
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "103969005"
---
# <a name="uses-of-the-printcapabilities"></a>Utilizzi dell'oggetto PrintCapabilities

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Il PrintCapabilities è progettato per rappresentare gli attributi di dispositivo configurabili come costrutti di funzionalità o di opzione o costrutti di parametro. Queste informazioni definiscono lo spazio di configurazione del dispositivo e possono essere usate da un client dell'interfaccia utente per costruire un'interfaccia utente. Le parole chiave dello schema di stampa definiscono un set di istanze di funzionalità standard, le istanze delle opzioni per le istanze della funzionalità standard e le istanze ParameterDef.

I costrutti di funzione, opzione o parametro nell'elemento PrintCapabilities sono destinati a ospitare istanze di proprietà o ScoredProperty che descrivono un dispositivo e che sono supportate dal sottosistema spooler. Queste istanze di proprietà e ScoredProperty sono di interesse generale per i client del dispositivo e contengono le informazioni fornite dalle funzioni DevCaps Win32. Le parole chiave Print Schema definiscono un set di proprietà standard e istanze ScoredProperty.

È opportuno sottolineare che il documento PrintCapabilities è destinato a rappresentare solo dati a valore singolo, ovvero dati che non dipendono da una particolare configurazione del dispositivo. Il documento PrintCapabilities fornisce solo uno snapshot dei dati dipendenti dalla configurazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



