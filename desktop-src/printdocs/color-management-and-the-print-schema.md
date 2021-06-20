---
description: Informazioni sulle parole chiave configurabili dall'utente in Schema di stampa per la gestione dei colori, ad esempio PageColorManagement e PageBlackGenerationProcessing.
ms.assetid: 296255b8-fe5c-46dd-b717-487aaae0db80
title: Gestione colori e schema di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9258d9dcc59ab24f9cfca8e170bf3f3f62841b21
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409674"
---
# <a name="color-management-and-the-print-schema"></a>Gestione colori e schema di stampa

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Le parole chiave dell'elemento configurabile dall'utente possono essere specifiche di XPS o non XPS. Nel caso in cui non siano specifici di XPS, la parola chiave può essere usata per la stampa basata su GDI legacy. Se un'applicazione decide di impostare queste parole chiave in un PrintTicket, è il driver a determinare l'azione e il comportamento corretto da intraprendere in base alle definizioni presentate nello schema di stampa. Una qualsiasi di queste parole chiave può essere usata nel contesto di ICM. Per altre informazioni, vedere Windows Vista SDK.



| Parola chiave configurabile dall'utente dello schema di stampa       | DevMODE Equivalente     | Specifico di XPS   |
|----------------------------------------------|------------------------|----------------|
| PageColorManagement<br/>               | dmICMMethod<br/> | No<br/>  |
| PageBlackGenerationProcessing<br/>     | Nessuno<br/>        | Sì<br/> |
| PageBlendColorSpace<br/>               | Nessuno<br/>        | Sì<br/> |
| PageSourceColorProfile<br/>            | Nessuno<br/>        | No<br/>  |
| PageDestinationColorProfile<br/>       | Nessuno<br/>        | No<br/>  |
| PageICMRenderingIntent<br/>            | dmICMIntent<br/> | No<br/>  |
| JobOptimalDestinationColorProfile<br/> | Nessuno<br/>        | No<br/>  |
| PageDeviceColorSpaceUsage<br/>         | Nessuno<br/>        | Sì<br/> |



 

## <a name="pagecolormanagement-system-handling"></a>Gestione del sistema PageColorManagement

Per PageColorManagement, il sistema fornisce la gestione automatica di PrintTicket alla conversione da DEVMODE a DEVMODE a PrintTicket, se necessario. Dipende dal percorso di stampa specifico tra l'applicazione (Win32 o WPF) e il driver (basato su GDI o XPSDrv). Nel caso della stampa da un'applicazione Windows Presentation Foundation a un driver di stampa XPSDrv Microsoft, nel documento PrintTicket o PrintCapabilities non deve essere annunciata l'opzione pubblica PageColorManagement di System SHOULD NOT; In questo caso, la gestione del colore non può essere gestita automaticamente dal sistema. La stampa da un'applicazione Win32 a un driver di stampa XPSDrv Microsoft può comportare la gestione del colore tra l'applicazione e GDI, tuttavia dopo la conversione in formato XPS, non sarà possibile gestire automaticamente la gestione del colore tra il documento XPS e il driver e/o il dispositivo, perché il formato XPS contrassegna ogni elemento con informazioni complete sul colore e sta al driver o al dispositivo elaborare queste informazioni.



| Opzioni pubbliche di PageColorManagement | Valore DEVMODE                  |
|------------------------------------|--------------------------------|
| Nessuno<br/>                    | DMICMMETHOD \_ NONE<br/>   |
| Dispositivo<br/>                  | DISPOSITIVO \_ DMICMMETHOD<br/> |
| Driver<br/>                  | DMICMMETHOD \_ DRIVER<br/> |
| Sistema<br/>                  | SISTEMA \_ DMICMMETHOD<br/> |



 

## <a name="pageicmrenderingintent-system-handling"></a>Gestione del sistema PageICMRenderingIntent

Per PageICMRenderingIntent, il sistema fornisce la gestione automatica di PrintTicket alla conversione da DEVMODE a PrintTicket, se necessario. Dipende dal percorso di stampa specifico tra l'applicazione (Win32 o Windows Presentation Foundation) e il driver (basato su GDI o XPSDrv).



| Opzioni pubbliche PageICMRenderingIntent | Valore DEVMODE                       |
|---------------------------------------|-------------------------------------|
| AbsoluteColorimetric<br/>       | COLORIMETRICA \_ DMICM ABS \_<br/> |
| RelativeColorimetric<br/>       | DMICM \_ COLORIMETRIC<br/>      |
| Fotografie<br/>                | CONTRASTO \_ DMICM<br/>          |
| BusinessGraphics<br/>           | \_SATURAZIONE DMICM<br/>          |



 

Tutte le altre parole chiave correlate a Gestione colori (oltre a PageColorManagement o PageICMRenderingIntent) non hanno tale gestione automatica.

## <a name="joboptimaldestinationcolorprofile-and-pagedestinationcolorprofile-usage"></a>Utilizzo di JobOptimalDestinationColorProfile e PageDestinationColorProfile

Un'applicazione PUÒ decidere di eseguire una query sul documento PrintCapabilities per JobOptimalDestinationColorProfile. Ciò potrebbe offrire a un'applicazione il profilo colori ottimale in base alla configurazione del dispositivo corrente, come definito nel documento PrintCapabilities. Se l'applicazione decide che il driver deve eseguire la gestione del colore nel profilo colori di destinazione specificato da JobOptimalDestinationColorProfile, PageColorManagement e PageDestinationColorProfile verranno impostati rispettivamente su Driver e DriverConfiguration in PrintTicket. Se l'applicazione non vuole usare JobOptionalDestinationColorProfile e sceglie di usarla, deve impostare PageColorManagement su Nessuno e impostare anche PageDestinationColorProfile su Application in PrintTicket per comunicare che l'applicazione ha già eseguito la gestione del colore sul profilo colori di destinazione specificato. Un altro scenario può verificarsi quando l'applicazione sceglie di usare il profilo colori di destinazione ottimale restituito dai driver PrintCapabilities, ma decide di eseguire la gestione del colore da sola. In questo caso, PageColorManagement verrebbe impostato su None e PageDestinationColorProfile verrebbe impostato su Application.

## <a name="pagesourcecolorprofile-usage"></a>Utilizzo di PageSourceColorProfile

Per PageSourceColorProfile, un'applicazione PUÒ specificare un profilo colori di origine per ogni pagina in PrintTicket, indipendentemente dall'opzione selezionata per PageColorManagement. Indipendentemente dal fatto che sia presente o meno, è il driver a decidere il comportamento per ogni caso in base alle definizioni presentate nello schema di stampa. Ad esempio, un'applicazione può impostare PageColorManagement su Nessuno e quindi non impostare PageSourceColorProfile in PrintTicket. È anche possibile per un'applicazione impostare PageColorManagement su Driver e quindi impostare PageSourceColorProfile in PrintTicket. il driver in questo caso è responsabile della determinazione del comportamento all'interno delle linee guida di PrintSchema.

## <a name="pagedevicecolorspaceusage"></a>PageDeviceColorSpaceUsage

PageDeviceColorSpaceUsage è un elemento configurabile dall'utente specifico di XPS impostato dall'applicazione. Fornisce istruzioni per il dispositivo impostando l'opzione appropriata in PrintTicket, per la gestione del profilo dello spazio colori associato all'interno di un documento XPS. L'applicazione e/o printTicket esistente possono specificare questa parola chiave in un PrintTicket inviato al dispositivo. Indipendentemente dal fatto che sia presente o meno, è il driver a decidere il comportamento per ogni caso, in base alle definizioni presentate nello schema di stampa.

## <a name="print-schema-color-management-example-flow"></a>Flusso di esempio di Gestione colori dello schema di stampa

Il diagramma seguente illustra il flusso per gli scenari più probabili per l'uso di Gestione colori e dello schema di stampa. Per semplicità e leggibilità, sono state usate solo le parole chiave dello schema di stampa configurabili dall'utente seguenti per illustrarne l'utilizzo: PageColorManagement, JobOptimalDestinaionColorProfile, PageSourceColorProfile e PageDestinationColorProfile. Una linea continua rappresenta un'azione che dovrebbe verificarsi e una linea tratteggiata rappresenta un'azione che può verificarsi. Lo scenario seguente non è l'interazione garantita che si verificherà tra l'applicazione, il driver e il sistema, ma rappresenta il caso di utilizzo più comune che si verificherà.

![diagramma che illustra come vengono elaborate le impostazioni di gestione dei colori](images/local-1992284846-colormanagementtest3.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




