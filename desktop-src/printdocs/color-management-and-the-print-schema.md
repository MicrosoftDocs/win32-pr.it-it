---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 296255b8-fe5c-46dd-b717-487aaae0db80
title: Gestione dei colori e dello schema di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134a598466fd52c66d632a28c750840d4123f529
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "103886054"
---
# <a name="color-management-and-the-print-schema"></a>Gestione dei colori e dello schema di stampa

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Le parole chiave degli elementi configurabili dall'utente possono essere specifiche di XPS o non XPS. Nel caso in cui non siano specifiche di XPS, la parola chiave può essere usata per la stampa basata su GDI legacy. Se un'applicazione decide di impostare queste parole chiave in un oggetto PrintTicket, spetta al driver determinare l'azione e il comportamento corretti da eseguire in base alle definizioni presentate nello schema di stampa. Ognuna di queste parole chiave può essere usata nel contesto di ICM. Per ulteriori informazioni, consultare Windows Vista SDK.



| Parola chiave configurabile dell'utente dello schema di stampa       | DEVMODE equivalente     | Specifiche XPS   |
|----------------------------------------------|------------------------|----------------|
| PageColorManagement<br/>               | dmICMMethod<br/> | No<br/>  |
| PageBlackGenerationProcessing<br/>     | nessuno<br/>        | Sì<br/> |
| PageBlendColorSpace<br/>               | nessuno<br/>        | Sì<br/> |
| PageSourceColorProfile<br/>            | nessuno<br/>        | No<br/>  |
| PageDestinationColorProfile<br/>       | nessuno<br/>        | No<br/>  |
| PageICMRenderingIntent<br/>            | dmICMIntent<br/> | No<br/>  |
| JobOptimalDestinationColorProfile<br/> | nessuno<br/>        | No<br/>  |
| PageDeviceColorSpaceUsage<br/>         | nessuno<br/>        | Sì<br/> |



 

## <a name="pagecolormanagement-system-handling"></a>Gestione del sistema PageColorManagement

Per PageColorManagement, il sistema fornisce la gestione automatica di PrintTicket a DEVMODE o DEVMODE alla conversione PrintTicket, se necessario. Dipende dal percorso di stampa specifico tra l'applicazione (Win32 o WPF) e il driver (basato su GDI o XPSDrv). Nel caso di stampa da un'applicazione Windows Presentation Foundation a un driver di stampa Microsoft XPSDrv, un'opzione pubblica PageColorManagement del sistema non deve essere annunciata nel documento PrintTicket o PrintCapabilities; in questo caso, la gestione dei colori non può essere gestita automaticamente dal sistema. La stampa da un'applicazione Win32 a un driver di stampa Microsoft XPSDrv può causare la gestione dei colori tra l'applicazione e GDI, tuttavia, dopo la conversione in formato XPS, non vi sarà alcuna gestione automatica del sistema della gestione dei colori tra il documento XPS e il driver e/o il dispositivo, perché XPS-Format contrassegna ogni elemento con informazioni complete sui colori e spetta al driver o al dispositivo per elaborare queste informazioni.



| Opzioni pubbliche PageColorManagement | Valore DEVMODE                  |
|------------------------------------|--------------------------------|
| nessuno<br/>                    | DMICMMETHOD \_ None<br/>   |
| Dispositivo<br/>                  | \_dispositivo DMICMMETHOD<br/> |
| Driver<br/>                  | \_driver DMICMMETHOD<br/> |
| Sistema<br/>                  | \_sistema DMICMMETHOD<br/> |



 

## <a name="pageicmrenderingintent-system-handling"></a>Gestione del sistema PageICMRenderingIntent

Per PageICMRenderingIntent, il sistema fornisce la gestione automatica di PrintTicket a DEVMODE o DEVMODE alla conversione PrintTicket, se necessario. Dipende dal percorso di stampa specifico tra l'applicazione (Win32 o Windows Presentation Foundation) e il driver (basato su GDI o XPSDrv).



| Opzioni pubbliche PageICMRenderingIntent | Valore DEVMODE                       |
|---------------------------------------|-------------------------------------|
| AbsoluteColorimetric<br/>       | \_colorimetrico DMICM ABS \_<br/> |
| RelativeColorimetric<br/>       | \_colorimetrico DMICM<br/>      |
| Fotografie<br/>                | \_contrasto DMICM<br/>          |
| BusinessGraphics<br/>           | \_saturazione DMICM<br/>          |



 

Tutte le altre parole chiave correlate alla gestione dei colori, oltre a PageColorManagement o PageICMRenderingIntent, non hanno una gestione automatica di questo tipo.

## <a name="joboptimaldestinationcolorprofile-and-pagedestinationcolorprofile-usage"></a>Utilizzo di JobOptimalDestinationColorProfile e PageDestinationColorProfile

Un'applicazione può decidere di eseguire una query sul documento PrintCapabilities per JobOptimalDestinationColorProfile. In questo modo è possibile assegnare a un'applicazione il profilo colori ottimale in base alla configurazione corrente del dispositivo come definito nel documento PrintCapabilities. Se l'applicazione decide che il driver deve eseguire la gestione dei colori nel profilo colori di destinazione specificato da JobOptimalDestinationColorProfile, PageColorManagement e PageDestinationColorProfile verrebbero impostati rispettivamente su driver e DriverConfiguration nell'oggetto PrintTicket. Se l'applicazione non desidera utilizzare JobOptionalDestinationColorProfile e sceglie di utilizzarne una propria, deve impostare PageColorManagement su None e impostare PageDestinationColorProfile su Application nel PrintTicket per indicare che l'applicazione ha già eseguito la gestione dei colori nel profilo colori di destinazione specificato. Un altro scenario può verificarsi quando l'applicazione sceglie di usare il profilo di colore di destinazione ottimale restituito dai driver PrintCapabilities, ma decide di eseguire autonomamente la gestione dei colori. In questo caso, PageColorManagement è impostato su None e PageDestinationColorProfile viene impostato su Application.

## <a name="pagesourcecolorprofile-usage"></a>Utilizzo di PageSourceColorProfile

Per PageSourceColorProfile, un'applicazione può specificare un profilo dei colori di origine per ogni pagina nell'oggetto PrintTicket, indipendentemente dall'opzione selezionata per PageColorManagement. Se è presente o meno, spetta al driver decidere il comportamento per ogni case in base alle definizioni presentate nello schema di stampa. Ad esempio, un'applicazione può impostare PageColorManagement su None e quindi non impostare PageSourceColorProfile nel PrintTicket. È anche possibile che un'applicazione imposti PageColorManagement sul driver, quindi impostare PageSourceColorProfile nel PrintTicket; il driver in questo caso è responsabile della determinazione del comportamento all'interno delle linee guida del PrintSchema.

## <a name="pagedevicecolorspaceusage"></a>PageDeviceColorSpaceUsage

PageDeviceColorSpaceUsage è un elemento configurabile dell'utente specifico di XPS impostato dall'applicazione. Vengono fornite istruzioni per il dispositivo impostando l'opzione appropriata nell'oggetto PrintTicket, per la gestione del profilo dello spazio colore associata all'interno di un documento XPS. L'applicazione e/o PrintTicket esistente può specificare questa parola chiave in un oggetto PrintTicket inviato al dispositivo. Se è presente o meno, spetta al driver decidere il comportamento per ogni case, in base alle definizioni presentate nello schema di stampa.

## <a name="print-schema-color-management-example-flow"></a>Flusso di esempio di gestione colori dello schema di stampa

Il diagramma seguente illustra Flow per gli scenari più probabili per l'uso della gestione dei colori e dello schema di stampa. Per semplicità e leggibilità, per illustrare l'utilizzo sono state usate solo le parole chiave dello schema di stampa configurabili per l'utente seguenti: PageColorManagement, JobOptimalDestinaionColorProfile, PageSourceColorProfile e PageDestinationColorProfile. Una linea a tinta unita rappresenta un'azione che deve verificarsi e una linea tratteggiata rappresenta un'azione che può verificarsi. Lo scenario seguente non è l'interazione garantita che verrà generata tra l'applicazione, il driver e il sistema, tuttavia, rappresenta il caso d'uso più comune che si verificherà.

![diagramma che illustra come vengono elaborate le impostazioni di gestione dei colori](images/local-1992284846-colormanagementtest3.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




