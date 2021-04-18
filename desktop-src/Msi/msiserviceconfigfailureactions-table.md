---
description: La tabella MsiServiceConfigFailureActions elenca le operazioni da eseguire in seguito a un errore del servizio. Le operazioni specificate in questa tabella vengono eseguite la volta successiva che il sistema viene avviato.
ms.assetid: 7c450b74-1f91-4a1c-beee-646a407eb8a8
title: Tabella MsiServiceConfigFailureActions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae55d095e227611271de35d673289fc9eb5b174e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316262"
---
# <a name="msiserviceconfigfailureactions-table"></a>Tabella MsiServiceConfigFailureActions

La tabella MsiServiceConfigFailureActions elenca le operazioni da eseguire in seguito a un errore del servizio. Le operazioni specificate in questa tabella vengono eseguite la volta successiva che il sistema viene avviato.

**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato. Questa tabella è disponibile a partire da Windows Installer 5,0.

La tabella MsiServiceConfigFailureActions include le colonne seguenti.



| Colonna                         | Tipo                         | Chiave | Nullable |
|--------------------------------|------------------------------|-----|----------|
| MsiServiceConfigFailureActions | [Identificatore](identifier.md) | S   | N        |
| Nome                           | [Formattato](formatted.md)   | N   | N        |
| Evento                          | [Integer](integer.md)       | N   | N        |
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

Si tratta della chiave primaria di questa tabella che identifica un'azione non riuscita.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Questa colonna contiene il nome di un servizio che fa parte di questo pacchetto o che è già installato.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Evento
</dt> <dd>

In questa colonna viene specificato quando modificare la configurazione del servizio. I valori seguenti sono campi di bit che possono essere combinati per rappresentare più operazioni. Qualsiasi altro valore di campo di bit viene ignorato.



| Costante                                         | Descrizione                                     |
|--------------------------------------------------|-------------------------------------------------|
| **msidbServiceConfigEventInstall** 1<br/>   | Modificare durante l'installazione del componente.    |
| **msidbServiceConfigEventUninstall** 2<br/> | Modifica durante la disinstallazione del componente.  |
| **msidbServiceConfigEventReinstall** 4<br/> | Modificare durante la riinstallazione del componente. |



 

</dd> <dt>

<span id="ResetPeriod"></span><span id="resetperiod"></span><span id="RESETPERIOD"></span>ResetPeriod
</dt> <dd>

Periodo di reimpostazione in secondi del conteggio degli errori del servizio. [Gestione controllo servizi](../services/service-control-manager.md) conta il numero di volte in cui ogni servizio ha avuto esito negativo dal momento dell'ultimo riavvio del sistema. Il conteggio viene reimpostato su zero se il servizio non ha esito negativo per il periodo di ripristino. Quando il servizio non riesce per l'ennesima volta, il sistema esegue l'azione specificata nell'elemento \[ N-1 \] della matrice specificata nel campo Actions.

Lasciare vuoto il campo ResetPeriod per indicare che il numero di errori non deve mai essere reimpostato.

</dd> <dt>

<span id="RebootMessage"></span><span id="rebootmessage"></span><span id="REBOOTMESSAGE"></span>RebootMessage
</dt> <dd>

Il messaggio viene inviato agli utenti prima di riavviare il computer in risposta a un'azione di **\_ \_ riavvio dell'azione SC** specificata nella colonna azioni. È possibile utilizzare una stringa vuota "" per inviare il messaggio corrente invariato. È possibile utilizzare \[ ~ \] la sintassi del tipo di dati [formattato](formatted.md) per eliminare il messaggio corrente e non inviare alcun messaggio.

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Comando
</dt> <dd>

La riga di comando eseguita dal processo creato dalla funzione [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) in risposta a un'azione **del \_ \_ \_ comando di esecuzione di un'azione SC** specificata nella colonna azioni. Il nuovo processo viene eseguito con lo stesso account del servizio e solo se il campo dell'azione è **SC \_ Action \_ Run \_ Command**. È possibile usare una stringa vuota, "", per usare la riga di comando corrente senza modifiche. È possibile utilizzare la \[ ~ \] sintassi del tipo di dati [formattato](formatted.md) per eliminare la riga di comando corrente ed eseguire nessuna operazione quando il servizio ha esito negativo.

</dd> <dt>

<span id="Actions"></span><span id="actions"></span><span id="ACTIONS"></span>Azioni
</dt> <dd>

Questo campo contiene una matrice di valori integer che specificano le azioni eseguite da SCM se il servizio ha esito negativo. Separare i valori nella matrice in base a \[ ~ \] . Il valore integer nell'ennesimo elemento della matrice specifica l'azione eseguita quando il servizio ha esito negativo per l'ennesimo tempo. Ogni membro della matrice è uno dei valori interi seguenti.



| Costante                                 | Descrizione           |
|------------------------------------------|-----------------------|
| **SC \_ \_Nessuna azione** 0<br/>         | Nessuna azione.            |
| **SC \_ AZIONE \_ riavvio** 2<br/>       | Riavviare il computer. |
| **SC \_ \_Riavvio azione** 1<br/>      | Riavviare il servizio.  |
| **SC \_ \_ \_ Comando Esegui azione** 3<br/> | Eseguire un comando.        |



 

</dd> <dt>

<span id="DelayActions"></span><span id="delayactions"></span><span id="DELAYACTIONS"></span>DelayActions
</dt> <dd>

Questo campo contiene una matrice di valori integer che specifica il tempo in millisecondi di attesa prima di eseguire l'azione specificata nella colonna azione. Separare i valori nella matrice in base a \[ ~ \] . Il numero di elementi nella matrice DelayActions deve essere uguale al numero di elementi nella matrice actions. L'ennesimo elemento della matrice DelayActions specifica il ritardo di tempo per l'ennesimo elemento della matrice di azioni.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna per la colonna uno della [tabella dei componenti](component-table.md).

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

 

 
