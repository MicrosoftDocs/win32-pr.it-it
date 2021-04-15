---
description: Definisce il tipo di endpoint che possono essere utilizzati per connettersi a un servizio.
ms.assetid: 50397D25-7C71-4AA2-89BF-F90CBDCFFA91
title: Enumerazione UpdateEndpointType (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointType
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: 942bcb5275c6a4f39d6e2828025e5b9a40e52c46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525074"
---
# <a name="updateendpointtype-enumeration"></a>Enumerazione UpdateEndpointType

Definisce il tipo di endpoint che possono essere utilizzati per connettersi a un servizio.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagEndpointType { 
  uetClientServer          = 0,
  uetReporting             = ( uetClientServer + 1 ),
  uetWuaSelfUpdate         = ( uetReporting + 1 ),
  uetRegulation            = ( uetWuaSelfUpdate + 1 ),
  uetSimpleTargeting       = ( uetRegulation + 1 ),
  uetSecuredClientServer   = ( uetSimpleTargeting + 1 ),
  uetSecondaryServiceAuth  = ( uetSecuredClientServer + 1 )
} UpdateEndpointType;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**
</dt> <dd>

Un endpoint client-server usato per connettersi al servizio di aggiornamento, ad esempio Windows Update, Microsoft Update e server WSUS in un ambiente aziendale, per trovare informazioni sugli aggiornamenti che potrebbero essere applicabili al computer.

Il servizio di aggiornamento restituisce informazioni sugli aggiornamenti che sono stati pubblicati, modificati o ritirati a partire dall'ultima volta in cui il client ha eseguito una sincronizzazione con il server.

</dd> <dt>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**
</dt> <dd>

Un endpoint di Reporting utilizzato quando il client segnala i risultati di analisi, download e installazioni di nuovo nel servizio di aggiornamento.

Nel caso di servizi pubblici (Windows Update e Microsoft Update), questa operazione viene eseguita per finalità di monitoraggio della qualità.

Nel caso di servizi privati, ad esempio un server WSUS aziendale, il tipo di endpoint Thhis consente anche al server di raccogliere l'inventario e altre informazioni sui computer client gestiti.

</dd> <dt>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**
</dt> <dd>

Un endpoint di aggiornamento automatico utilizzato quando il computer client contatta un servizio di aggiornamento per verificare se è presente una nuova versione del software client agente Windows Update.

L'endpoint di aggiornamento automatico usa un protocollo diverso, quindi l'endpoint Client-Server in modo che gli aggiornamenti automatici possano essere distribuiti anche se si verifica una condizione di errore che potrebbe impedire la normale sincronizzazione del client-server di lavorare su un computer client specifico.

</dd> <dt>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**
</dt> <dd>

Un endpoint del regolamento utilizzato quando il computer client contatta il servizio di regolamentazione per agire su un particolare aggiornamento applicabile al computer di destinazione.

Il servizio del regolamento può indicare se l'aggiornamento è "regolato" (anche noto come "limitato"). in altre parole, il servizio di regolamentazione può indicare al computer client che non deve agire su un particolare aggiornamento, anche se tale aggiornamento sembra essere applicabile.

</dd> <dt>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**
</dt> <dd>

Un endpoint di destinazione semplice utilizzato solo con servizi privati (server WSUS negli ambienti aziendali). In un ambiente aziendale, i computer client possono essere assegnati a determinati gruppi di destinazione e gli aggiornamenti possono essere approvati per l'installazione in computer in alcuni gruppi, ma non altri.

Ad esempio, l'amministratore di WSUS può creare un gruppo di "test" per i computer utilizzati per testare nuovi aggiornamenti e l'amministratore può approvare gli aggiornamenti appena rilasciati per l'installazione nei computer del gruppo di test senza approvarli per l'installazione in altri computer dell'organizzazione. Lo scambio di destinazione semplice viene utilizzato per consentire a un computer client di registrarsi con il server WSUS e per consentire al server di indicare al computer client il gruppo in cui si trova.

</dd> <dt>

<span id="uetSecuredClientServer"></span><span id="uetsecuredclientserver"></span><span id="UETSECUREDCLIENTSERVER"></span>**uetSecuredClientServer**
</dt> <dd>

Un endpoint client-server protetto che consente a un client di ottenere informazioni sulle app che richiedono licenze, in modo che possano essere usate in un computer client. Questo framework di licenze è attualmente utilizzato solo da Windows 8 per distribuire le app e gli aggiornamenti ottenuti tramite Windows Store. L'endpoint client-server protetto non è attualmente utilizzato da Windows Update, Microsoft Update o WSUS.

</dd> <dt>

<span id="uetSecondaryServiceAuth"></span><span id="uetsecondaryserviceauth"></span><span id="UETSECONDARYSERVICEAUTH"></span>**uetSecondaryServiceAuth**
</dt> <dd>

L'endpoint di autenticazione del servizio secondario viene usato da un client per fornire l'autenticazione prima di ottenere informazioni sulle app che richiedono licenze, in modo che possano essere usate in un computer client. Questo framework di licenze è attualmente utilizzato solo da Windows 8 per distribuire le app e gli aggiornamenti ottenuti tramite Windows Store. L'endpoint di autenticazione del servizio secondario non è attualmente utilizzato da Windows Update, Microsoft Update o WSUS.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                              |
| Intestazione<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |



 

 




