---
description: Dopo la convalida, un PrintTicket può essere usato per creare uno snapshot di PrintCapabilities.
ms.assetid: b49e20b7-bd9e-4b8f-bb4a-bb1e99b0c417
title: Creazione di un documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96ea51cef9dfd0f351704b3b71a7f6163737736
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409514"
---
# <a name="creating-a-printcapabilities-document"></a>Creazione di un documento PrintCapabilities

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Dopo la convalida, un PrintTicket può essere usato per creare uno snapshot di PrintCapabilities. Il provider deve avere una rappresentazione interna per qualsiasi property il cui valore dipende dalla configurazione del dispositivo. Ad esempio, se SpotDiameter è una proprietà dipendente dalle funzionalità Resolution e MediaType, una rappresentazione interna di SpotDiameter in relazione ai vari valori per Resolution e MediaType potrebbe essere visualizzata come nella tabella seguente:



| Soluzione      | MediaType         | SpotDiameter   |
|-----------------|-------------------|----------------|
| 300<br/>  | Legame<br/>   | 520<br/> |
| 300<br/>  | Lucido<br/> | 350<br/> |
| 600<br/>  | Legame<br/>   | 330<br/> |
| 600<br/>  | Lucido<br/> | 180<br/> |
| 1200<br/> | Legame<br/>   | 250<br/> |
| 1200<br/> | Lucido<br/> | 100<br/> |



 

Per questo esempio, il provider PrintCapabilities deve usare il PrintTicket fornito per selezionare la voce appropriata dalla tabella interna e segnalare tale voce come Valore per la proprietà SpotDiameter. Questo processo viene ripetuto per ogni proprietà multivalore (per ogni proprietà il cui valore dipende dalla configurazione). La [sezione Schema PrintCapabilities e Costruzione di](printcapabilities-schema-and-document-construction.md) documenti descrive gli altri passaggi necessari per creare uno snapshot di PrintCapabilities.

Per creare uno snapshot del documento PrintCapabilities predefinito, fornire un PrintTicket predefinito (anziché un PrintTicket arbitrario) al metodo che crea documenti PrintCapabilities.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




