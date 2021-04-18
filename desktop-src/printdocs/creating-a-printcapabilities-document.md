---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: b49e20b7-bd9e-4b8f-bb4a-bb1e99b0c417
title: Creazione di un documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ccb1adf4626254ba9f71c706ad7d4556a23aeb6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320870"
---
# <a name="creating-a-printcapabilities-document"></a>Creazione di un documento PrintCapabilities

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Una volta convalidata, un oggetto PrintTicket può essere utilizzato per creare uno snapshot dell'oggetto PrintCapabilities. Il provider deve avere una rappresentazione interna per qualsiasi proprietà il cui valore dipende dalla configurazione del dispositivo. Se, ad esempio, SpotDiameter è una proprietà che dipende dalle funzionalità di risoluzione e di MediaType, una rappresentazione interna di SpotDiameter in relazione ai vari valori per la risoluzione e MediaType potrebbe apparire come indicato nella tabella seguente:



| Soluzione      | MediaType         | SpotDiameter   |
|-----------------|-------------------|----------------|
| 300<br/>  | Legame<br/>   | 520<br/> |
| 300<br/>  | Lucido<br/> | 350<br/> |
| 600<br/>  | Legame<br/>   | 330<br/> |
| 600<br/>  | Lucido<br/> | 180<br/> |
| 1200<br/> | Legame<br/>   | 250<br/> |
| 1200<br/> | Lucido<br/> | 100<br/> |



 

Per questo esempio, il provider PrintCapabilities deve usare l'oggetto PrintTicket fornito per selezionare la voce appropriata della tabella interna e segnalarla come valore per la proprietà SpotDiameter. Questo processo viene ripetuto per ogni proprietà multivalore (per ogni proprietà il cui valore dipende dalla configurazione). Nella sezione relativa alla creazione di [schemi e documenti di PrintCapabilities](printcapabilities-schema-and-document-construction.md) vengono descritti gli altri passaggi necessari per la creazione di uno snapshot dell'oggetto PrintCapabilities.

Per creare uno snapshot del documento PrintCapabilities predefinito, fornire un oggetto PrintTicket predefinito (anziché un oggetto PrintTicket arbitrario) al metodo che crea documenti PrintCapabilities.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




