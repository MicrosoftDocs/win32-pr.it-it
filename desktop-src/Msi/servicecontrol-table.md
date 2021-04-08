---
description: La tabella ServiceControl viene utilizzata per controllare i servizi installati o disinstallati. Nota i servizi che si basano sulla presenza di un assembly nella global assembly cache (GAC) non possono essere installati o avviati utilizzando le tabelle ServiceInstall e ServiceControl.
ms.assetid: c51cd9bd-3c55-4eec-ab67-172765adc51c
title: Tabella ServiceControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2abd123e937673694dffd53773a16fcbd704c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757625"
---
# <a name="servicecontrol-table"></a>Tabella ServiceControl

La tabella ServiceControl viene utilizzata per controllare i servizi installati o disinstallati.

> [!Note]  
> I servizi che si basano sulla presenza di un [assembly](assemblies.md) nella global assembly cache (GAC) non possono essere installati o avviati utilizzando le tabelle [ServiceInstall](serviceinstall-table.md) e ServiceControl. Se è necessario avviare un servizio che dipende da un assembly nella GAC, è necessario utilizzare un'azione personalizzata sequenziata dopo l' [azione InstallFinalize](installfinalize-action.md) o un' [azione personalizzata di commit](commit-custom-actions.md). Per informazioni sull'installazione degli assembly nella GAC, vedere [installazione degli assembly nella global assembly cache](installation-of-assemblies-to-the-global-assembly-cache.md).

 

La tabella ServiceControl include le colonne seguenti.



| Colonna         | Tipo                         | Chiave | Nullable |
|----------------|------------------------------|-----|----------|
| ServiceControl | [Identificatore](identifier.md) | S   | N        |
| Nome           | [Formattato](formatted.md)   | N   | N        |
| Evento          | [Integer](integer.md)       | N   | N        |
| Argomenti      | [Formattato](formatted.md)   | N   | S        |
| Attesa           | [Integer](integer.md)       | N   | S        |
| Componente\_    | [Identificatore](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="ServiceControl"></span><span id="servicecontrol"></span><span id="SERVICECONTROL"></span>ServiceControl
</dt> <dd>

Si tratta della chiave primaria della tabella.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Questa colonna è la stringa che denomina il servizio. Questa colonna può essere utilizzata per controllare un servizio non installato.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Evento
</dt> <dd>

Questa colonna contiene le operazioni da eseguire sul servizio denominato. Si noti che quando si arresta un servizio, vengono arrestati anche tutti i servizi che dipendono da tale servizio. Quando si elimina un servizio che esegue, il programma di installazione interrompe il servizio.

I valori in questo campo sono campi di bit che possono essere combinati in un singolo valore che rappresenta diverse operazioni.

I valori seguenti vengono utilizzati solo durante un'installazione.



| Costante                           | Valore esadecimale | Decimal | Descrizione                                                                        |
|------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| **msidbServiceControlEventStart**  | 0x001       | 1       | Avvia il servizio durante l' [azione StartServices](startservices-action.md).    |
| **msidbServiceControlEventStop**   | 0x002       | 2       | Arresta il servizio durante l' [azione StopServices](stopservices-action.md).       |
| (nessuna)                             | 0x004       | 4       | <reserved>                                                                   |
| **msidbServiceControlEventDelete** | 0x008       | 8       | Elimina il servizio durante l' [azione DeleteServices](deleteservices-action.md). |



 

I valori seguenti vengono utilizzati solo durante una disinstallazione.



| Costante                                    | Valore esadecimale | Decimal | Descrizione                                                                        |
|---------------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| **msidbServiceControlEventUninstallStart**  | 0x010       | 16      | Avvia il servizio durante l' [azione StartServices](startservices-action.md).    |
| **msidbServiceControlEventUninstallStop**   | 0x020       | 32      | Arresta il servizio durante l' [azione StopServices](stopservices-action.md).       |
| (nessuna)                                      | 0x040       | 64      | <reserved>                                                                   |
| **msidbServiceControlEventUninstallDelete** | 0x080       | 128     | Elimina il servizio durante l' [azione DeleteServices](deleteservices-action.md). |



 

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argomenti
</dt> <dd>

Elenco di argomenti per l'avvio dei servizi. Gli argomenti sono separati da caratteri null \[ ~ \] . Ad esempio, l'elenco di argomenti uno, due e tre è elencato come: uno \[ ~ \] due \[ ~ \] tre.

</dd> <dt>

<span id="Wait"></span><span id="wait"></span><span id="WAIT"></span>Attendere
</dt> <dd>

Se si lascia il campo null o si immette un valore pari a 1, il programma di installazione attenderà un massimo di 30 secondi per il completamento del servizio prima di procedere. L'attesa può essere usata per consentire un ulteriore tempo a un evento critico per restituire un errore di errore. Il valore 0 in questo campo significa attendere solo che il gestore di controllo del servizio (SCM) segnali che questo servizio è in uno stato in sospeso prima di continuare con l'installazione.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna per la colonna uno della [tabella dei componenti](component-table.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Le azioni [StartServices](startservices-action.md), [StopServices](stopservices-action.md)e [DeleteServices](deleteservices-action.md) nelle [*tabelle di sequenza*](s-gly.md) elaborano le informazioni contenute in questa tabella. Per informazioni sull'utilizzo di *tabelle di sequenza*, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).

Utilizzare la colonna nome per avviare, arrestare o eliminare i servizi che vengono sostituiti dall'installazione di o che dipendono da un nuovo servizio installato. Ad esempio, l'immissione di un servizio nella colonna ServiceControl può associare il servizio a un componente nella \_ colonna Component. Se il campo di bit nella colonna evento è impostato su Avvia durante l'installazione, il programma di installazione avvia il servizio durante l'installazione di componente.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



