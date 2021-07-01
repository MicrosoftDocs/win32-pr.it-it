---
description: Esaminare le parole chiave GPD senza equivalenti di documenti PrintCapabilities. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: f1b94241-5376-423f-b10a-336dc47f3d59
title: Nota per gli autori gpd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52fe9d0c4ce36cf603d492688f4faa426e3050b9
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119816"
---
# <a name="note-to-gpd-authors"></a>Nota per gli autori gpd

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Per gli autori di documenti PrintCapabilities che hanno familiarità con i file GPD, alcune parole chiave GPD non hanno equivalenti nel documento PrintCapabilities. La tabella seguente contiene le parole chiave GPD senza un documento PrintCapabilities equivalente e il motivo per cui non esiste alcun equivalente.



| Parola chiave GPD                                                                            | Spiegazione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*Vincoli<br/> \*InvalidCombination<br/> \*ConflictPriority<br/> | I vincoli non sono definiti nel documento PrintCapabilities perché i client PrintCapabilities non devono elaborarli, applicarli o risolverli. Queste attività vengono eseguite dal provider PrintTicket durante la convalida di PrintTicket. I plug-in Unidrv possono fornire il proprio codice di convalida PrintTicket oppure possono fare affidamento su Unidrv per eseguire questa convalida. In quest'ultimo caso, Unidrv applica tutti i vincoli definiti nel file GPD.<br/> I driver monolitici devono fornire il proprio codice di convalida PrintTicket e devono fornire il proprio metodo di espressione e applicazione dei vincoli.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \*DefaultOption<br/>                                                             | Esiste un metodo PrintTicket che restituisce un oggetto PrintTicket predefinito, che per definizione ha tutte le impostazioni predefinite per ogni funzionalità.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \*FeatureType<br/>                                                               | Una funzionalità può essere suddivisa in tre categorie diverse:<br/> Funzionalità le cui impostazioni sono definite in un oggetto PrintTicket. Questo tipo di funzionalità è detto appiccicoso per i documenti perché queste impostazioni determinano direttamente il modo in cui viene elaborato un documento.<br/> Funzionalità le cui impostazioni riflettono gli attributi del dispositivo fisico non controllati dall'utente, ad esempio la quantità di memoria nel dispositivo, o che indicano la presenza di componenti aggiuntivi facoltativi, ad esempio alimentatori di carta o duplex. Questo tipo di funzionalità è denominato device-sticky o printer-sticky. Lo stato di questo tipo di funzionalità è importante perché può vincolare un'opzione appartenente a una funzionalità appiccicoso del documento.<br/> Una funzionalità appiccicoso o appiccicoso del dispositivo può essere ulteriormente categorizzata come funzionalità sticky della stampante dell'interfaccia utente o come funzionalità auto-sticky della stampante. Una funzionalità di sticky della stampante dell'interfaccia utente deve essere visualizzata in un'interfaccia utente che può essere impostata da un amministratore. Il dispositivo rileva automaticamente una funzionalità auto-sticky della stampante.<br/> |
| \*Opzione ... \* Caso<br/>                                                         | Un provider PrintCapabilities deve implementare un metodo che crea un documento PrintCapabilities che enumera le funzionalità di tipo printer-sticky o document-sticky, a seconda del tipo specificato dal chiamante. Per questo motivo non è necessario presentare le stesse informazioni tramite il documento PrintCapabilities stesso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




