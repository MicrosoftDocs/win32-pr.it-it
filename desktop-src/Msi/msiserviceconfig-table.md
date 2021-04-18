---
description: La tabella MsiServiceConfig configura un servizio installato o installato dal pacchetto corrente.
ms.assetid: 0d9fd005-9326-4a18-8496-35b5d1927f47
title: Tabella MsiServiceConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357b6787e56d52a893dd1a118a3e2fcbc13379e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316263"
---
# <a name="msiserviceconfig-table"></a>Tabella MsiServiceConfig

La tabella MsiServiceConfig configura un servizio installato o installato dal pacchetto corrente.

**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato. Questa tabella è disponibile a partire da Windows Installer 5,0.

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

Si tratta della chiave primaria della tabella.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Questa colonna contiene il nome di un servizio che fa parte di questo pacchetto o che è già installato.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Evento
</dt> <dd>

In questa colonna viene specificato quando modificare la configurazione del servizio. È possibile combinare i valori seguenti per rappresentare più operazioni. Tutti i valori inclusi non vengono ignorati.



| Costante                                         | Descrizione                                              |
|--------------------------------------------------|----------------------------------------------------------|
| **msidbServiceConfigEventInstall** 1<br/>   | Esegue l'azione durante l'installazione del componente.   |
| **msidbServiceConfigEventUninstall** 2<br/> | Esegue l'azione durante la disinstallazione del componente. |
| **msidbServiceConfigEventReinstall** 4<br/> | Esegue l'azione durante la reinstallazione del componente. |



 

</dd> <dt>

<span id="ConfigType"></span><span id="configtype"></span><span id="CONFIGTYPE"></span>ConfigType
</dt> <dd>

Il valore in questo campo, combinato con il valore nel campo arguments, specifica la modifica da apportare alla configurazione del servizio. La modifica specificata viene applicata alla successiva avvio del sistema.



| File di configurazione                                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Servizio \_ di CONFIGURAZIONE \_ \_ \_ avvio automatico ritardato** 3<br/>       | Configurare il tempo di attesa di un [servizio di avvio automatico](../services/automatically-starting-services.md). <br/> Immettere 1 nel campo argument per avviare il servizio dopo altri servizi di avvio automatico, oltre a un ritardo di tempo. <br/> Immettere 0 nel campo argument per disattivare il ritardo del servizio di avvio automatico.<br/> Si applica solo ai servizi o ai servizi di avvio automatico installati da questo pacchetto **con \_ \_ avvio automatico del servizio** nel campo StartType della [tabella ServiceInstall](serviceinstall-table.md).<br/>                                                                         |
| **Servizio \_ di CONFIGURARE \_ i \_ privilegi richiesti \_ informazioni** 6<br/> | Modificare l'elenco dei privilegi richiesti dal servizio.<br/> Immettere un elenco di privilegi richiesti nel campo argomento. Il valore stringa [formattato](formatted.md) nel campo argument elenca le [**costanti Privilege**](../secauthz/privilege-constants.md) per i privilegi richiesti. È possibile utilizzare la \[ ~ \] sintassi della stringa [formattata](formatted.md) per inserire un carattere null. Separare le costanti Privilege nell'elenco in base a \[ ~ \] .<br/>                                                                                                                              |
| **Servizio \_ di \_ \_ \_ Informazioni SID servizio di configurazione** 5<br/>         | Aggiungere un tipo di SID del servizio al token di processo che contiene il servizio.<br/> Immettere nel campo argomento un tipo di SID del servizio valido per la struttura delle [**\_ \_ informazioni del SID**](/windows/win32/api/winsvc/ns-winsvc-service_sid_info) del servizio: tipo di SID del servizio **\_ \_ \_ None** (0x00), **tipo di SID del servizio con \_ \_ \_ restrizioni** (0x03) o **tipo di SID del servizio senza \_ \_ \_ restrizioni** (0x01). <br/>                                                                                                                                                                                                                                              |
| **Servizio \_ di \_ \_ Informazioni di prespegnimento configurazione** 7<br/>          | Configurare la durata di attesa di [Gestione controllo servizi](../services/service-control-manager.md) prima di procedere con altre operazioni di arresto. Il servizio SCM attende questo periodo di tempo dopo l'invio della notifica di **\_ \_ prechiusura del controllo del servizio** al servizio. <br/> Immettere la lunghezza del ritardo di tempo, in millisecondi, nel campo argomento. Lasciare vuoto il campo argomento per reimpostare il ritardo di tempo sul valore predefinito di 3 minuti. <br/>                                                                                                                               |
| **Servizio \_ di \_ \_ \_ Flag azioni errore configurazione** 4<br/>     | Configurare quando eseguire le azioni di errore per il servizio. Questa impostazione viene ignorata se il servizio non dispone di azioni di errore configurate.<br/> Immettere 0 per eseguire le azioni solo se il servizio termina senza Reporting **Service \_ interrotto**.<br/> Immettere 1 per eseguire le azioni se il servizio termina il servizio di Reporting **\_ interrotto** e il membro **dwWin32ExitCode** della struttura [**\_ dello stato del servizio**](/windows/win32/api/winsvc/ns-winsvc-service_status) non ha **\_ esito positivo**. Le azioni di errore configurate vengono inoltre eseguite se il servizio termina senza Reporting **Service \_ interrotto**.<br/> |



 

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argomento
</dt> <dd>

Il valore in questo campo, combinato con il valore nel campo ConfigType, specifica la modifica da apportare alla configurazione del servizio. La modifica specificata viene applicata alla successiva avvio del sistema.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna per la colonna componente della [tabella dei componenti](component-table.md).

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

 

 
