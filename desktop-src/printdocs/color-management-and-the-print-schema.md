---
description: Informazioni sulle parole chiave configurabili dall'utente nello schema di stampa per la gestione dei colori, ad esempio PageColorManagement e PageBlackGenerationProcessing.
ms.assetid: 296255b8-fe5c-46dd-b717-487aaae0db80
title: Gestione colori e schema di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3e7e5a86b9f598183a4b3765e1cc38836b4ee7bb62e1835e06575392771dc5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846387"
---
# <a name="color-management-and-the-print-schema"></a>Gestione colori e schema di stampa

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Le parole chiave degli elementi configurabili dall'utente possono essere specifiche di XPS o non XPS. Nel caso in cui non siano specifiche di XPS, la parola chiave può essere usata per la stampa legacy basata su GDI. Se un'applicazione decide di impostare queste parole chiave in un PrintTicket, è il driver a determinare l'azione e il comportamento corretto da intraprendere in base alle definizioni presentate nello schema di stampa. Una di queste parole chiave può essere usata nel contesto di ICM. Per altre informazioni, vedere l'SDK Windows Vista.



| Parola chiave configurabile dall'utente dello schema di stampa       | DevMODE equivalente     | Specifico di XPS   |
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

Per PageColorManagement, il sistema fornisce la gestione automatica di PrintTicket per la conversione da DEVMODE a DEVMODE a PrintTicket, se necessario. Ciò dipende dal percorso di stampa specifico tra l'applicazione (Win32 o WPF) e il driver (basato su GDI o XPSDrv). Nel caso di stampa da un'applicazione Windows Presentation Foundation a un driver di stampa Microsoft XPSDrv, un'opzione pubblica PageColorManagement di System SHOULD NOT essere annunciata nel documento PrintTicket o PrintCapabilities; In questo caso, la gestione dei colori non può essere gestita automaticamente dal sistema. La stampa da un'applicazione Win32 a un driver di stampa Microsoft XPSDrv può comportare la gestione dei colori tra l'applicazione e GDI, tuttavia dopo la conversione in formato XPS, non sarà possibile gestire automaticamente la gestione dei colori tra il documento XPS e il driver e/o il dispositivo, perché il formato XPS contrassegna ogni elemento con informazioni complete sul colore e deve essere il driver o il dispositivo a elaborare queste informazioni.



| Opzioni pubbliche di PageColorManagement | Valore DEVMODE                  |
|------------------------------------|--------------------------------|
| Nessuno<br/>                    | DMICMMETHOD \_ NONE<br/>   |
| Dispositivo<br/>                  | DISPOSITIVO \_ DMICMMETHOD<br/> |
| Driver<br/>                  | DMICMMETHOD \_ DRIVER<br/> |
| Sistema<br/>                  | SISTEMA \_ DMICMMETHOD<br/> |



 

## <a name="pageicmrenderingintent-system-handling"></a>PageICMRenderingIntent System Handling

Per PageICMRenderingIntent, il sistema fornisce la gestione automatica di PrintTicket per la conversione da DEVMODE a PrintTicket, se necessario. Questo dipende dal percorso di stampa specifico tra l'applicazione (Win32 o Windows Presentation Foundation) e il driver (basato su GDI o XPSDrv).



| PageICMRenderingIntent Public Options | Valore DEVMODE                       |
|---------------------------------------|-------------------------------------|
| AbsoluteColorimetric<br/>       | DMICM \_ ABS \_ COLORIMETRIC<br/> |
| RelativeColorimetric<br/>       | COLORIMETRIC DI DMICM \_<br/>      |
| Fotografie<br/>                | CONTRASTO \_ DMICM<br/>          |
| BusinessGraphics<br/>           | \_SATURAZIONE DMICM<br/>          |



 

Tutte le altre parole chiave correlate a Gestione colori (oltre a PageColorManagement o PageICMRenderingIntent) non hanno tale gestione automatica.

## <a name="joboptimaldestinationcolorprofile-and-pagedestinationcolorprofile-usage"></a>Utilizzo di JobOptimalDestinationColorProfile e PageDestinationColorProfile

Un'applicazione PUÒ decidere di eseguire una query sul documento PrintCapabilities per JobOptimalDestinationColorProfile. Ciò potrebbe fornire a un'applicazione il profilo colore ottimale in base alla configurazione corrente del dispositivo, come definito nel documento PrintCapabilities. Se l'applicazione decide che il driver deve eseguire la gestione dei colori nel profilo colori di destinazione specificato da JobOptimalDestinationColorProfile, PageColorManagement e PageDestinationColorProfile verranno impostati rispettivamente su Driver e DriverConfiguration in PrintTicket. Se l'applicazione non vuole usare JobOptionalDestinationColorProfile e sceglie di usarne uno proprio, deve impostare PageColorManagement su None e impostare anche PageDestinationColorProfile su Application in printTicket per comunicare che l'applicazione ha già eseguito la gestione del colore sul profilo colore di destinazione specificato. Un altro scenario può verificarsi quando l'applicazione sceglie di usare il profilo colori di destinazione ottimale restituito dai driver PrintCapabilities, ma decide di eseguire la gestione del colore in modo proprio. In questo caso, PageColorManagement verrebbe impostato su None e PageDestinationColorProfile verrebbe impostato su Application.

## <a name="pagesourcecolorprofile-usage"></a>Utilizzo di PageSourceColorProfile

Per PageSourceColorProfile, un'applicazione PUÒ specificare un profilo colore di origine per ogni pagina in PrintTicket, indipendentemente dall'opzione selezionata per PageColorManagement. Indipendentemente dal fatto che sia presente o meno, è il driver a decidere il comportamento per ogni caso in base alle definizioni presentate nello schema di stampa. Ad esempio, un'applicazione può impostare PageColorManagement su None e quindi non impostare PageSourceColorProfile in PrintTicket. È anche possibile per un'applicazione impostare PageColorManagement su Driver e quindi impostare PageSourceColorProfile in PrintTicket. Il driver in questo caso è responsabile della determinazione del comportamento all'interno delle linee guida di PrintSchema.

## <a name="pagedevicecolorspaceusage"></a>PageDeviceColorSpaceUsage

PageDeviceColorSpaceUsage è un elemento configurabile dall'utente specifico di XPS impostato dall'applicazione. Fornisce istruzioni per il dispositivo impostando l'opzione appropriata in PrintTicket, per la gestione del profilo dello spazio colore associata all'interno di un documento XPS. L'applicazione e/o printTicket esistente possono specificare questa parola chiave in un PrintTicket inviato al dispositivo. Indipendentemente dal fatto che sia presente o meno, è il driver a decidere il comportamento per ogni caso, in base alle definizioni presentate nello schema di stampa.

## <a name="print-schema-color-management-example-flow"></a>Esempio di gestione colori dello schema di stampa Flow

Il diagramma seguente illustra il flusso per gli scenari più probabili per l'uso di Gestione colori e dello schema di stampa. Per semplicità e leggibilità, sono state usate solo le parole chiave dello schema di stampa configurabili dall'utente seguenti per illustrarne l'utilizzo: PageColorManagement, JobOptimalDestinaionColorProfile, PageSourceColorProfile e PageDestinationColorProfile. Una linea continua rappresenta un'azione che dovrebbe verificarsi e una linea tratteggiata rappresenta un'azione che può verificarsi. Lo scenario seguente non è l'interazione garantita che si verificherà tra l'applicazione, il driver e il sistema, ma rappresenta il caso di utilizzo più comune che si verificherà.

![diagramma che illustra come vengono elaborate le impostazioni di gestione dei colori](images/local-1992284846-colormanagementtest3.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




