---
description: La tabella MsiServiceConfigFailureActions elenca le operazioni da eseguire in caso di errore di un servizio. Le operazioni specificate in questa tabella vengono eseguite al successivo avvio del sistema.
ms.assetid: 7c450b74-1f91-4a1c-beee-646a407eb8a8
title: Tabella MsiServiceConfigFailureActions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 907c0feb2e331c1e19ff4292d11cc58b65340a7543d9af5d0a1ccf23d2e80a48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944418"
---
# <a name="msiserviceconfigfailureactions-table"></a>Tabella MsiServiceConfigFailureActions

La tabella MsiServiceConfigFailureActions elenca le operazioni da eseguire in caso di errore di un servizio. Le operazioni specificate in questa tabella vengono eseguite al successivo avvio del sistema.

**[Windows Installer 4.5 o versioni precedenti:](not-supported-in-windows-installer-4-5.md)** Non supportato. Questa tabella è disponibile a partire da Windows Installer 5.0.

La tabella MsiServiceConfigFailureActions include le colonne seguenti.



| Colonna                         | Tipo                         | Chiave | Nullable |
|--------------------------------|------------------------------|-----|----------|
| MsiServiceConfigFailureActions | [Identificatore](identifier.md) | S   | N        |
| Nome                           | [Formattato](formatted.md)   | N   | N        |
| Event                          | [Integer](integer.md)       | N   | N        |
| ResetPeriod                    | [Integer](integer.md)       | N   | S        |
| RebootMessage                  | [Formattato](formatted.md)   | N   | Y        |
| Comando                        | [Formattato](formatted.md)   | N   | S        |
| Azioni                        | [Text](text.md)             | N   | S        |
| DelayActions                   | [Text](text.md)             | N   | S        |
| Componente\_                    | [Identificatore](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="MsiServiceConfigFailureActions"></span><span id="msiserviceconfigfailureactions"></span><span id="MSISERVICECONFIGFAILUREACTIONS"></span>MsiServiceConfigFailureActions
</dt> <dd>

Si tratta della chiave primaria di questa tabella che identifica un'azione di errore.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Questa colonna contiene il nome di un servizio che fa parte di questo pacchetto o che è già installato.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Evento
</dt> <dd>

Questa colonna specifica quando modificare la configurazione del servizio. I valori seguenti sono campi di bit che possono essere combinati per rappresentare più operazioni. Tutti gli altri valori dei campi di bit vengono ignorati.



| Costante                                         | Descrizione                                     |
|--------------------------------------------------|-------------------------------------------------|
| **msidbServiceConfigEventInstall** 1<br/>   | Modifica durante l'installazione del componente.    |
| **msidbServiceConfigEventUninstall** 2<br/> | Modifica durante la disinstallazione del componente.  |
| **msidbServiceConfigEventReinstall** 4<br/> | Modifica durante la riinstallazione del componente. |



 

</dd> <dt>

<span id="ResetPeriod"></span><span id="resetperiod"></span><span id="RESETPERIOD"></span>ResetPeriod
</dt> <dd>

Periodo di reimpostazione in secondi del numero di errori del servizio. Gestione [controllo servizi](../services/service-control-manager.md) (SCM) conta il numero di volte in cui ogni servizio ha avuto esito negativo dall'ultimo riavvio del sistema. Il conteggio viene reimpostato su zero se il servizio non ha esito negativo per il periodo di reimpostazione. Quando il servizio ha esito negativo per l'ora N, il sistema esegue l'azione specificata \[ nell'elemento N-1 della \] matrice specificata nel campo Azioni.

Lasciare vuoto il campo ResetPeriod per indicare che il conteggio degli errori non deve mai essere reimpostato.

</dd> <dt>

<span id="RebootMessage"></span><span id="rebootmessage"></span><span id="REBOOTMESSAGE"></span>RebootMessage
</dt> <dd>

Messaggio inviato agli utenti prima del riavvio del computer in risposta a **un'azione SC \_ ACTION \_ REBOOT** specificata nella colonna Azioni. È possibile usare una stringa vuota, "", per inviare il messaggio corrente senza modifiche. È possibile usare \[ ~ \] la sintassi del tipo di dati [Formattato](formatted.md) per eliminare il messaggio corrente e non inviare alcun messaggio.

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Comando
</dt> <dd>

Riga di comando eseguita dal processo creato dalla funzione [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) in risposta a **un'azione SC ACTION RUN \_ \_ \_ COMMAND** specificata nella colonna Azioni. Il nuovo processo viene eseguito nello stesso account del servizio e solo se il campo Azione è **SC \_ ACTION RUN \_ \_ COMMAND**. È possibile usare una stringa vuota, "", per usare la riga di comando corrente invariata. È possibile usare la sintassi del tipo di dati Formattato per eliminare la riga di comando corrente e non eseguire alcuna operazione in caso di errore \[ ~ \] del servizio. [](formatted.md)

</dd> <dt>

<span id="Actions"></span><span id="actions"></span><span id="ACTIONS"></span>Azioni
</dt> <dd>

Questo campo contiene una matrice di valori integer che specificano le azioni eseguite da Gestione controllo servizi in caso di errore del servizio. Separare i valori nella matrice con \[ ~ \] . Il valore intero nell'elemento Nth della matrice specifica l'azione eseguita quando il servizio ha esito negativo per l'Esima volta. Ogni membro della matrice è uno dei valori integer seguenti.



| Costante                                 | Descrizione           |
|------------------------------------------|-----------------------|
| **SC \_ AZIONE \_ NESSUNO 0**<br/>         | Nessuna azione.            |
| **SC \_ AZIONE \_ REBOOT** 2<br/>       | Riavviare il computer. |
| **SC \_ AZIONE \_ RESTART** 1<br/>      | Riavviare il servizio.  |
| **SC \_ AZIONE \_ ESEGUI \_ COMANDO** 3<br/> | Eseguire un comando.        |



 

</dd> <dt>

<span id="DelayActions"></span><span id="delayactions"></span><span id="DELAYACTIONS"></span>DelayActions
</dt> <dd>

Questo campo contiene una matrice di valori integer che specificano il tempo in millisecondi di attesa prima di eseguire l'azione specificata nella colonna Azione. Separare i valori nella matrice con \[ ~ \] . Il numero di elementi nella matrice DelayActions deve essere uguale al numero di elementi nella matrice Actions. L'n°elemento della matrice DelayActions specifica il ritardo temporale per l'e ultimo elemento della matrice Actions.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna alla colonna uno della [tabella dei componenti](component-table.md).

</dd> </dl>

## <a name="validation"></a>Convalida

<dl>

[ICE102](ice-102.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 
