---
description: La tabella ServiceControl viene usata per controllare i servizi installati o disinstallati. Nota I servizi che si basano sulla presenza di un assembly nella Global Assembly Cache (GAC) non possono essere installati o avviati usando le tabelle ServiceInstall e ServiceControl.
ms.assetid: c51cd9bd-3c55-4eec-ab67-172765adc51c
title: Tabella ServiceControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b0c360991ce4a72698ac1b667d82a98ba64b7a0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885685"
---
# <a name="servicecontrol-table"></a>Tabella ServiceControl

La tabella ServiceControl viene usata per controllare i servizi installati o disinstallati.

> [!Note]  
> I servizi che si basano sulla presenza di un [assembly](assemblies.md) nella Global Assembly Cache (GAC) non possono essere installati o avviati usando le tabelle [ServiceInstall](serviceinstall-table.md) e ServiceControl. Se è necessario avviare un servizio che dipende da un assembly nella GAC, è necessario usare un'azione personalizzata sequenziata dopo l'azione [InstallFinalize](installfinalize-action.md) o un'azione [personalizzata commit](commit-custom-actions.md). Per informazioni sull'installazione di assembly nella GAC, vedere Installazione di [assembly nella Global Assembly Cache.](installation-of-assemblies-to-the-global-assembly-cache.md)

 

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

Si tratta della chiave primaria di questa tabella.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Questa colonna è la stringa che denomina il servizio. Questa colonna può essere utilizzata per controllare un servizio non installato.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Evento
</dt> <dd>

Questa colonna contiene le operazioni da eseguire sul servizio denominato. Si noti che quando si arresta un servizio, vengono arrestati anche tutti i servizi che dipendono da tale servizio. Quando si elimina un servizio in esecuzione, il programma di installazione lo arresta.

I valori in questo campo sono campi di bit che possono essere combinati in un singolo valore che rappresenta diverse operazioni.

I valori seguenti vengono usati solo durante un'installazione di .



| Costante                           | Valore esadecimale | Decimal | Descrizione                                                                        |
|------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| **msidbServiceControlEventStart**  | 0x001       | 1       | Avvia il servizio durante [l'azione StartServices](startservices-action.md).    |
| **msidbServiceControlEventStop**   | 0x002       | 2       | Arresta il servizio durante [l'azione StopServices](stopservices-action.md).       |
| (nessuna)                             | 0x004       | 4       | &lt;reserved&gt;                                                                   |
| **msidbServiceControlEventDelete** | 0x008       | 8       | Elimina il servizio durante [l'azione DeleteServices](deleteservices-action.md). |



 

I valori seguenti vengono usati solo durante una disinstallazione.



| Costante                                    | Valore esadecimale | Decimal | Descrizione                                                                        |
|---------------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| **msidbServiceControlEventUninstallStart**  | 0x010       | 16      | Avvia il servizio durante [l'azione StartServices](startservices-action.md).    |
| **msidbServiceControlEventUninstallStop**   | 0x020       | 32      | Arresta il servizio durante [l'azione StopServices](stopservices-action.md).       |
| (nessuna)                                      | 0x040       | 64      | &lt;reserved&gt;                                                                   |
| **msidbServiceControlEventUninstallDelete** | 0x080       | 128     | Elimina il servizio durante [l'azione DeleteServices](deleteservices-action.md). |



 

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argomenti
</dt> <dd>

Elenco di argomenti per l'avvio dei servizi. Gli argomenti sono separati da caratteri Null \[ ~ \] . Ad esempio, l'elenco di argomenti One, Two e Three sono elencati come: One \[ ~ \] Two \[ ~ \] Three.

</dd> <dt>

<span id="Wait"></span><span id="wait"></span><span id="WAIT"></span>Aspettare
</dt> <dd>

Se si lascia null questo campo o si immette un valore pari a 1, il programma di installazione attende un massimo di 30 secondi per il completamento del servizio prima di procedere. L'attesa può essere usata per consentire un tempo aggiuntivo per la restituzione di un errore da parte di un evento critico. Il valore 0 in questo campo indica di attendere solo fino a quando Gestione controllo servizi segnala che il servizio è in sospeso prima di continuare con l'installazione.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna alla colonna uno della [tabella dei componenti](component-table.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Le [azioni StartServices](startservices-action.md), [StopServices](stopservices-action.md)e [DeleteServices](deleteservices-action.md) nelle tabelle [*di sequenza*](s-gly.md) elaborano le informazioni contenute in questa tabella. Per informazioni sull'uso *delle tabelle di sequenza,* vedere [Using a Sequence Table](using-a-sequence-table.md).

Usare la colonna Nome per avviare, arrestare o eliminare i servizi che vengono sostituiti dall'installazione o che dipendono da un nuovo servizio installato. Ad esempio, l'immissione di MyService nella colonna ServiceControl può collegare questo servizio a MyComponent nella colonna \_ Componente. Se il campo di bit nella colonna Event è impostato per l'avvio durante l'installazione, il programma di installazione avvia MyService durante l'installazione di MyComponent.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



