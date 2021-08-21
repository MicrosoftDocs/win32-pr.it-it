---
description: La tabella MsiServiceConfig configura un servizio installato o installato dal pacchetto corrente.
ms.assetid: 0d9fd005-9326-4a18-8496-35b5d1927f47
title: Tabella MsiServiceConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b72e21fdfecd59780b862d3bfe7d68ef829b59b847dbceb0e9c13befae9d4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828591"
---
# <a name="msiserviceconfig-table"></a>Tabella MsiServiceConfig

La tabella MsiServiceConfig configura un servizio installato o installato dal pacchetto corrente.

**[Windows Installer 4.5 o versioni precedenti:](not-supported-in-windows-installer-4-5.md)** Non supportato. Questa tabella è disponibile a partire da Windows Installer 5.0.

La tabella MsiServiceConfig include le colonne seguenti.



| Colonna           | Tipo                         | Chiave | Nullable |
|------------------|------------------------------|-----|----------|
| MsiServiceConfig | [Identificatore](identifier.md) | S   | N        |
| Nome             | [Formattato](formatted.md)   | N   | N        |
| Evento            | [Integer](integer.md)       | N   | N        |
| TipoConfigurazione       | [Integer](integer.md)       | N   | N        |
| Argomento         | [Formattato](formatted.md)   | N   | S        |
| Componente\_      | [Identificatore](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="MsiServiceConfig"></span><span id="msiserviceconfig"></span><span id="MSISERVICECONFIG"></span>MsiServiceConfig
</dt> <dd>

Si tratta della chiave primaria di questa tabella.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Questa colonna contiene il nome di un servizio che fa parte di questo pacchetto o che è già installato.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Evento
</dt> <dd>

Questa colonna specifica quando modificare la configurazione del servizio. I valori seguenti possono essere combinati per rappresentare più operazioni. Tutti i valori inclusi diversi da questi vengono ignorati.



| Costante                                         | Descrizione                                              |
|--------------------------------------------------|----------------------------------------------------------|
| **msidbServiceConfigEventInstall** 1<br/>   | Consente di eseguire l'azione durante l'installazione del componente.   |
| **msidbServiceConfigEventUninstall** 2<br/> | Consente di eseguire l'azione durante la disinstallazione del componente. |
| **msidbServiceConfigEventReinstall** 4<br/> | Esegue l'azione durante la reinstallazione del componente. |



 

</dd> <dt>

<span id="ConfigType"></span><span id="configtype"></span><span id="CONFIGTYPE"></span>ConfigType
</dt> <dd>

Il valore in questo campo, combinato con il valore nel campo Argomenti, specifica la modifica da apportare alla configurazione del servizio. La modifica specificata viene apportata al successivo avvio del sistema.



| File di configurazione                                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SERVIZIO \_ CONFIG \_ DELAYED \_ AUTO \_ START** 3<br/>       | Configurare il ritardo di un servizio [di avvio automatico.](../services/automatically-starting-services.md) <br/> Immettere 1 nel campo Argomento per avviare il servizio dopo altri servizi di avvio automatico più un ritardo di tempo. <br/> Immettere 0 nel campo Argomento per disattivare il ritardo dell'avvio automatico del servizio.<br/> Si applica solo ai servizi o ai servizi di avvio automatico installati da questo pacchetto con **SERVICE \_ AUTO \_ START** nel campo StartType della [tabella ServiceInstall](serviceinstall-table.md).<br/>                                                                         |
| **SERVIZIO \_ INFORMAZIONI \_ SUI PRIVILEGI NECESSARI DI \_ \_ CONFIGURAZIONE** 6<br/> | Modificare l'elenco dei privilegi richiesti dal servizio.<br/> Immettere un elenco di privilegi richiesti nel campo Argomento. Il [valore stringa](formatted.md) formattata nel campo Argomento elenca le costanti dei [**privilegi**](../secauthz/privilege-constants.md) per i privilegi richiesti. È possibile usare la \[ ~ \] sintassi della [stringa formattata](formatted.md) per inserire un carattere Null. Separare le costanti dei privilegi nell'elenco con \[ ~ \] .<br/>                                                                                                                              |
| **SERVIZIO \_ INFORMAZIONI \_ SUL \_ SID DEL SERVIZIO DI \_ CONFIGURAZIONE** 5<br/>         | Aggiungere un tipo di SID del servizio al token di processo contenente questo servizio.<br/> Immettere nel campo Argomento un tipo DI SID del servizio valido per la struttura [**SERVICE \_ SID \_ INFO:**](/windows/win32/api/winsvc/ns-winsvc-service_sid_info) **SERVICE \_ SID TYPE \_ \_ NONE** (0x00), **SERVICE \_ SID TYPE \_ \_ RESTRICTED** (0x03) o **SERVICE \_ SID TYPE \_ \_ UNRESTRICTED** (0x01). <br/>                                                                                                                                                                                                                                              |
| **SERVIZIO \_ CONFIG \_ PRESHUTDOWN \_ INFO** 7<br/>          | Configurare la durata dell'attesa di Gestione controllo [servizi](../services/service-control-manager.md) prima di procedere con altre operazioni di arresto. Gestione controllo servizi attende questo periodo di tempo dopo l'invio della notifica **\_ SERVICE CONTROL \_ PRESHUTDOWN** al servizio. <br/> Immettere la lunghezza del ritardo temporale, in millisecondi, nel campo Argomento. Lasciare vuoto il campo Argomento per reimpostare il ritardo temporale sul valore predefinito di 3 minuti. <br/>                                                                                                                               |
| **SERVIZIO \_ FLAG \_ DI AZIONI DI ERRORE DI \_ \_ CONFIGURAZIONE** 4<br/>     | Configurare quando eseguire le azioni di errore per questo servizio. Questa impostazione viene ignorata se il servizio non ha azioni di errore configurate.<br/> Immettere 0 per eseguire le azioni solo se il servizio termina senza segnalare **SERVICE \_ STOPPED**.<br/> Immettere 1 per eseguire le azioni se il servizio termina la segnalazione **SERVICE \_ STOPPED** e il membro **dwWin32ExitCode** della struttura [**SERVICE \_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) non è **ERROR \_ SUCCESS**. Le azioni di errore configurate vengono eseguite anche se il servizio termina senza segnalare **SERVICE \_ STOPPED.**<br/> |



 

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>discussione
</dt> <dd>

Il valore in questo campo, combinato con il valore nel campo ConfigType, specifica la modifica da apportare alla configurazione del servizio. La modifica specificata viene apportata al successivo avvio del sistema.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna alla colonna Componente della [tabella dei componenti](component-table.md).

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

 

 
