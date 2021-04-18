---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: f1b94241-5376-423f-b10a-336dc47f3d59
title: Nota per gli autori di GPD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 942bd1e8725428ee49bb937f3978622413160476
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320932"
---
# <a name="note-to-gpd-authors"></a>Nota per gli autori di GPD

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Per gli autori dei documenti PrintCapabilities che hanno familiarità con i file GPD, alcune parole chiave GPD non hanno equivalenti nel documento PrintCapabilities. La tabella seguente contiene le parole chiave GPD senza un documento PrintCapabilities equivalente e il motivo per cui non esiste alcun equivalente.



| Parola chiave GPD                                                                            | Spiegazione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*Vincoli<br/> \*InvalidCombination<br/> \*ConflictPriority<br/> | I vincoli non sono definiti nel documento PrintCapabilities perché i client PrintCapabilities non sono previsti per l'elaborazione, l'applicazione o la risoluzione. Queste attività restano disponibili affinché il provider PrintTicket esegua la convalida PrintTicket. I plug-in Unidrv possono fornire il proprio codice di convalida PrintTicket oppure possono basarsi su Unidrv per eseguire la convalida. Nel secondo caso, Unidrv impone tutti i vincoli definiti nel file GPD.<br/> I driver monolitici devono fornire il proprio codice di convalida PrintTicket e devono fornire il proprio metodo per esprimere e applicare vincoli.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \*DefaultOption<br/>                                                             | È presente un metodo PrintTicket che restituisce un oggetto PrintTicket predefinito, che per definizione include tutte le impostazioni predefinite per ogni funzionalità.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \*FeatureType<br/>                                                               | Una funzionalità può essere divisa in tre categorie diverse:<br/> Funzionalità le cui impostazioni sono definite in un oggetto PrintTicket. Questo tipo di funzionalità è denominato document-Sticky perché queste impostazioni determinano direttamente il modo in cui un documento viene elaborato.<br/> Funzionalità le cui impostazioni riflettono gli attributi del dispositivo fisico che non sono controllati dall'utente, ad esempio la quantità di memoria nel dispositivo, o che indicano la presenza di componenti aggiuntivi facoltativi, ad esempio gli alimentatori di carta o i duplex. Questo tipo di funzionalità è denominato Device-Sticky o Printer-Sticky. Lo stato di questo tipo di funzionalità è importante perché può vincolare un'opzione che appartiene a una funzionalità di documento-Sticky.<br/> Una funzionalità di dispositivo-appiccicoso o di stampa può essere ulteriormente categorizzata come funzionalità di una stampante (UI) della stampante o una funzionalità di stampa automatica-appiccicosa. In un'interfaccia utente che può essere impostata da un amministratore è necessario che venga visualizzata una funzionalità di stampa dell'interfaccia utente. Il dispositivo rileva automaticamente una funzionalità di stampa automatica-Sticky.<br/> |
| \*Passa a... \* Caso<br/>                                                         | Un provider PrintCapabilities deve implementare un metodo per la creazione di un documento PrintCapabilities che enumera le funzionalità della stampante o del documento appiccicoso, a seconda del tipo specificato dal chiamante. Per questo motivo non è necessario presentare le stesse informazioni tramite il documento PrintCapabilities.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




